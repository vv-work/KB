# DOTS

**DOTS**(**D**ata,**O**riented,**T**echonology,**S**tack)

## Questions

0. SIMD Vecotrization ?
1. ECS without Unity in VisualStudio?
2. Async Await with ECS?


## Links

- [Intel Dots Tutorial](https://software.intel.com/content/www/us/en/develop/articles/get-started-with-the-unity-entity-component-system-ecs-c-sharp-job-system-and-burst-compiler.html)

- [DOTS water Brust](https://www.raywenderlich.com/7880445-unity-job-system-and-burst-compiler-getting-started)

- [ECS non Unity](http://aras-p.info/texts/files/2018Academy%20-%20ECS-DoD.pdf)

## ECS

**ECS**(**E**ntitiy,**C**omponents,**S**ystems):

- Entity - Identity 
- Components - Data
- System - Behaviour is where is logic.

### Archetypes

`EntityArchetype`  - is combination of entities if we remove `Renderer`.
Then archetype will be **dynamically** changed.

![archetypes](res/ArchetypeDiagram.png)

### Memory Chunks

`ArchetypeChunk` - allocated memory by chunk.
When **dynamic** changed entity archetype it will be move to new chunk.

![chunk](res/ArchetypeChunkDiagram.png)

## Impoartnat

### WebGL

```c#
using UnityEditor;
using UnityEngine;

[InitializeOnLoad]
class EnableThreads
{
    static EnableThreads()
    {
        PlayerSettings.WebGL.linkerTarget = WebGLLinkerTarget.Wasm;
        PlayerSettings.WebGL.threadsSupport = true;
        PlayerSettings.WebGL.memorySize = 512;
    }
}

```


## Job System

Not ECS can be use **separetely**.

### Safety System

**Race Condition** - When one part of code depends on another.


**Safety System** - Prevent that by sanding data to potential race conditions only **blittable data types**

**Interoperability** - sharing data with blittable types unmanaged and managed .Net code.

**Managed code** - that executes only under **CLI** (Virtual machine)

### Native Container

Sort of shared memory to be able to accress location not a copy

**KeyPoints:**

- DifferentType
- ReadOnly                   - to avoid DisposalSentinel
- Container Allocator   - for best performance
#### Types:
```c#
//In Job System
class  NativeArray {}
class  NativeSlice {}//Get slice of NativeArray

//Extended in Unity ECS
class  NativeList {}
class  NativeHashMap {}
class  NativeMultiHashMap {} //multi values per key
class  NativeQueue {}
 
 [ReadOnly]
public NativeArray<int> input; // If my task need read only to avoid DisposalSentinel


NativeArray<float> result = new NativeArray<float>(1, Allocator.TempJob);

Allocator.Temp 
    // FAST  one Frame 
    // Not for passing to NativeContainer
    // Call Dispose before going to MonoBehaviour.Update

Allocator.TempJob 
    // 4 frames don't Depose 

Allocator.Presistent 
    // Slow but long living 
```

### Jobs

[IJob](interface)

- [Execute()](Method)

```c#
public struct MyJob : IJob
{
    public int a;
    public NativeArray<int> result;

    public void Execute()
    {
        result[a] = a++;
    }
}

```

### Jab Schedule

```c#
NativeArray<float> result = new NativeArray<float>(1, Allocator.TempJob);
MyJob jobData = new MyJob();
jobData.result = result;

static class IJobExtensions{ 
    static void Schedule();}
// Schedule the job
JobHandle handle = jobData.Schedule();  

// Wait for the job to complete
handle.Complete();
float aPlusB = result[0];
result.Dispose();
```

### JobHandle

```c#
JobHandle firstJobHandle = firstJob.Schedule();
JobHandle secondJobHandle = secondJob.Schedule(firstJobHandle);
secondJobHandle.Complete()

// Combine multiple job Handle
int numJobs = 10;
NativeArray<JobHandle> handles = new NativeArray<JobHandle>(numJobs, Allocator.TempJob);
JobHandle jh = JobHandle.CombineDependencies(handles);

// Doing a lot of jobs at once
public static void ScheduleBatchedJobs(); 
```

### IJobParallelFor

You need to set the size of array and it's endex before running;

```c#
struct IncrementByDeltaTimeJob: IJobParallelFor
{
    public NativeArray<float> values;
    public float deltaTime;

    public void Execute (int index)
    {
        float temp = values[index];
        temp += deltaTime;
        values[index] = temp;
    }
}
IJobParallelFor jobData = new IncrementByDeltaTimeJob();
jobData.value = value;
jobData.deltaTime = Time.deltaTime;

//Make sense execute multiple jobs per batch from 1 to 64
JobHandle handle = jobData.Schedule(result.Length, 32);

```

**Example**

```c#
using UnityEngine;
using Unity.Collections;
using Unity.Jobs;

class ApplyVelocityParallelForSample : MonoBehaviour
{
    struct VelocityJob : IJobParallelFor
    {
        // Jobs declare all data that will be accessed in the job
        // By declaring it as read only, multiple jobs are allowed to access the data in parallel
        [ReadOnly]
        public NativeArray<Vector3> velocity;

        public NativeArray<Vector3> position;

        public float deltaTime;

        public void Execute(int i)
        {
            // Move the positions based on delta time and velocity
            position[i] = position[i] + velocity[i] * deltaTime;
        }
    }

    public void Update()
    {
        var position = new NativeArray<Vector3>(500, Allocator.Persistent);

        var velocity = new NativeArray<Vector3>(500, Allocator.Persistent);
        for (var i = 0; i < velocity.Length; i++)
            velocity[i] = new Vector3(0, 10, 0);

        var job = new VelocityJob()
        {
            deltaTime = Time.deltaTime,
            position = position,
            velocity = velocity
        };

        // When there is very little work values of 32 or 64 can make sense.
        JobHandle jobHandle = job.Schedule(position.Length, 64);

        // Ensure the job has completed.
        jobHandle.Complete();

        Debug.Log(job.position[0]);

        // Native arrays must be disposed manually.
        position.Dispose();
        velocity.Dispose();
    }
}
```

### ITransformParallel

### ECS has ScheduleBatchedJobs implemented

### Tips and Tricks

0. Don't be stupid
1. Do not access static data from job (don't be stupid)
2. Flush scheduled batches (don't be stupid)
3. Don't try to update data from NativeContainer
``` c# 
 nativeArray[0]++; 
 //The same as
var temp = nativeArray[0]; temp++; 
```
4. Call JobHandle.Complete to regain ownership.
5. Don't call Complete right after Schaduale(don't be stupid)
6. Use [ReadOnly] (don't be stupid)
7. Do not allocate managed memory in jobs (don't be stupid)



## Algos

![](res/simd.jpeg)