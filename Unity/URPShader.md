# URP Shaders

## Questions

1. What the diffrence between Cg/HLSL
2. Diffrence between shader types Surface Shader, Unlit Shader, Image Effect Shader, Computer Shader.
3. `CGPROGRAM` and `ENDCG`
4. `HLSLPROGRAM` and `ENDHLSL`
5. What is `Pass` and `SubShader`?
6. `Varyings` and `Attributes` what is the diffrence
7. ComputeBuffs ?
8. Shadow Caster Pass - is it a shader or a pass?


## Basics

### Links

- [Examples by Unity](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@12.0/manual/writing-shaders-urp-basic-unlit-structure.html)
- 
### Input

#### Terms

- `Properties` - block of variables that can be changed in the editor
- `SubShader` - block of code that can be used in different render pipelines (actually code that is rendered into shader)
- `Pass` - block of code that can be used in different render pipelines
- `Fragment Shader` - code that is executed for each pixel of the mesh
- `Vertex Shader` - code that is executed for each vertex of the mesh
  - Determines final pixel colors and positions.
- `CGPROGRAM` - block of code that is executed in Cg
- `HLSLPROGRAM` - block of code that is executed in HLSL
- `ComputeBuffs` - block of code that is executed in Compute Shader
- Compute shader - is a shader that is executed on GPU
- `Shader_Caster_Pass` - is a pass that is executed for each object in the scene to generate shadow maps


**HLSL** - is a low-level language that is used to write shaders. It is a superset of Cg, which is a superset of GLSL. HLSL is used in DirectX, Cg is used in OpenGL, and GLSL is used in WebGL.

**Cg** - is a high-level language that is used to write shaders. It is a superset of GLSL. Cg is used in OpenGL, and GLSL is used in WebGL.

**Fragment** shader vs **Vertex** shader - the **fragment** shader is executed for each *pixel* of the mesh, while the **vertex** shader is executed for each *vertex* of the *mesh/*.

#### Computer Buffers

> C# Example of creating a ComputeBuffer   
 
```csharp
_buffer = new ComputeBuffer(size, sizeof(float) * 3); // size is the number of Vector3's you want to store, and sizeof(float) * 3 because Vector3 has 3 float values (x, y, z).
```

#### Universal Render Pipeline Shader Libraries

- `Core.hlsl`: This package contains core HLSL functions and definitions that are essential for the Universal Render Pipeline (URP). It includes common math operations, utility functions, and macros that are used across various shader libraries in URP.

- `UnityInput.hlsl`: This package provides functions and structures for handling Unity's input data, such as vertex attributes, interpolators, and uniforms. It simplifies the process of accessing data from meshes and other input sources within shaders.

- `UnityInstancing.hlsl`: This package contains helper functions and definitions for handling GPU instancing in the Universal Render Pipeline. It provides macros and utilities for working with per-instance data and efficiently rendering large numbers of objects with minimal draw calls.

- `UnityLighting.hlsl`: This package includes functions and definitions for working with lighting in the Universal Render Pipeline. It provides support for various lighting models, such as Lambertian (diffuse), Blinn-Phong (specular), and physically-based rendering (PBR), as well as utilities for working with shadows and reflections.

- `UnityPacking.hlsl`: This package contains functions and macros for packing and unpacking data in shaders, such as encoding and decoding normal vectors, colors, and other attributes. These utilities help to optimize memory usage and performance in the Universal Render Pipeline.

- `CommonMaterial.hlsl`: This package, part of the core render pipeline, provides common material properties and functions used across different render pipelines. It includes functions for handling smoothness, metallic, occlusion, and other material properties that are shared between different shading models and pipelines.

- `SurfaceInput.hlsl`: This package defines the SurfaceInput structure, which is used to pass data between the vertex and fragment shaders in URP's surface shaders. It includes fields for vertex attributes such as position, normal, tangent, color, and texture coordinates.

- `ShadowCasterPass.hlsl`: This package contains the shader code for the shadow caster pass in the Universal Render Pipeline. It is responsible for generating shadow maps by rendering objects from the point of view of the light source, taking into account the object's opacity and other shadow-related properties.
 

##### Example
```shaderlab
            #include "Packages/com.unity.render-pipelines.core/ShaderLibrary/CommonMaterial.hlsl"
			#include "Packages/com.unity.render-pipelines.universal/ShaderLibrary/SurfaceInput.hlsl"
			#include "Packages/com.unity.render-pipelines.universal/Shaders/ShadowCasterPass.hlsl"
```
 
#### Top List

Easy applience of custom variables

1. Incide `Properties`
```shaderlab

Properties
{
    [MainColor] _BaseColor("Base Color", Color) = (1, 1, 1, 1)
}
```

2. Incide **HLSL** block 

```shaderlab
            CBUFFER_START(UnityPerMaterial)
                half4 _BaseColor;
            CBUFFER_END 
```

3. Inside `frag()`

```shaderlab
half4 frag() : SV_Target
{
    return _BaseColor;
}
```

### Simple Shader

```shaderlab
// This shader fills the mesh shape with a color predefined in the code.
Shader "Example/URPUnlitShaderBasic"
{
    // The properties block of the Unity shader. In this example this block is empty
    // because the output color is predefined in the fragment shader code.
    Properties
    { }

    // The SubShader block containing the Shader code.
    SubShader
    {
        // SubShader Tags define when and under which conditions a SubShader block or
        // a pass is executed.
        Tags { "RenderType" = "Opaque" "RenderPipeline" = "UniversalPipeline" }

        Pass
        {
            // The HLSL code block. Unity SRP uses the HLSL language.
            HLSLPROGRAM
            // This line defines the name of the vertex shader.
            #pragma vertex vert
            // This line defines the name of the fragment shader.
            #pragma fragment frag

            // The Core.hlsl file contains definitions of frequently used HLSL
            // macros and functions, and also contains #include references to other
            // HLSL files (for example, Common.hlsl, SpaceTransforms.hlsl, etc.).
            #include "Packages/com.unity.render-pipelines.universal/ShaderLibrary/Core.hlsl"

            // The structure definition defines which variables it contains.
            // This example uses the Attributes structure as an input structure in
            // the vertex shader.
            struct Attributes
            {
                // The positionOS variable contains the vertex positions in object
                // space.
                float4 positionOS   : POSITION;
            };

            struct Varyings
            {
                // The positions in this struct must have the SV_POSITION semantic.
                float4 positionHCS  : SV_POSITION;
            };

            // The vertex shader definition with properties defined in the Varyings
            // structure. The type of the vert function must match the type (struct)
            // that it returns.
            Varyings vert(Attributes IN)
            {
                // Declaring the output object (OUT) with the Varyings struct.
                Varyings OUT;
                // The TransformObjectToHClip function transforms vertex positions
                // from object space to homogenous clip space.
                OUT.positionHCS = TransformObjectToHClip(IN.positionOS.xyz);
                // Returning the output.
                return OUT;
            }

            // The fragment shader definition.
            half4 frag() : SV_Target
            {
                // Defining the color variable and returning it.
                half4 customColor = half4(0.5, 0, 0, 1);
                return customColor;
            }
            ENDHLSL
        }
    }
}
```
