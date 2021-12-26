# ECS

## Unity ECS 

### Create enity

```csharp
_entityManager = World.DefaultGameObjectInjectionWorld.EntityManager;
var entity = _entityManager.CreateEntity(typeof(LevelComponent));
_entityManager.SetComponentData(entity, new LevelComponent(){Level = 10});
```

### Process System

```csharp
public class LevelUpSystem:ComponentSystem
    {
        protected override void OnUpdate()
        {
            Entities.ForEach(( LevelComponent lc) =>
            {
                lc.Level += 1f+Time.DeltaTime; 
            });
        }
    }
```

### My Unity ECS example

![My ecs in Unity](res\MyECSinUnity.gif)

> RotationCubeBehaviour.cs
```csharp
public class RotateCubeBehaviour : MonoBehaviour,IConvertGameObjectToEntity
{

    public float RotSpeed=15;
    public void Convert(Entity entity, EntityManager dstManager, GameObjectConversionSystem conversionSystem)
    {
        var data = default(RotationComponent);
        data.Degree = RotSpeed;
        dstManager.AddComponentData(entity, data);
    }
}
```

> RotationComponent.cs
```csharp
public struct RotationComponent: IComponentData
    {
        public float Degree;
    }
```

> RotationSystem.cs
```csharp
public class RotationSystem:ComponentSystem
    {
        protected override void OnUpdate()
        {
            Entities.With(_cubes) .ForEach(
                    (ref RotationComponent rc, ref Rotation r) =>
                    {
                        r.Value = math.mul(r.Value,
                            quaternion.RotateY( math.radians(
                                    rc.Degree * Time.fixedDeltaTime
                                ))); 
                    });
        }

        private EntityQuery _cubes;
        protected override void OnCreate()
        {
            _cubes = Entities.WithAll<RotationComponent, Rotation>().ToEntityQuery();
        }
```

## ECS Solution list

- ECS.ME
- Morpeh
- LeoECS
- LeoLite
