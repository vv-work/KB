# XR


## Top links

- [XR Interactive Toolkit Examples Unity Technology](https://github.com/Unity-Technologies/XR-Interaction-Toolkit-Examples) 


## ARKit Face Tracking
 
 Streaming from ARKIt to the heands  https://github.com/asus4/ARKitStreamer;

> Extra notes that dosen't really metter
 

[LeanTouch](http://gameprogrammingpatterns.com/contents.html)
>Best way according to unity to add touches to AR app.

## Features

1. Face Anchor
2. Face Mesh
3. Face expression coefficient
4. Face BlendShapes
    - SkinRenderer 51 BlendShapes  vertices


```csharp
public void RunWithConfig(ARKitFaceTrackingConfiguration config);

public delegate void ARFaceAnchorAdded(ARFaceAnchor anchorData);

public delegate void ARFaceAnchorUpdated(ARFaceAnchor anchorData);

public delegate void ARFaceAnchorRemoved(ARFaceAnchor anchorData);
```

![Mesh](.\Images\ArKitMesh.png)
![Mouth](\Images\ArKitMouth.png)
![Anchor](\Images\ArKitAnchor.png)

## Links

 - [AppleBlendShapes](https://developer.apple.com/documentation/arkit/arfaceanchor/blendshapelocation)
 - [Apple Light Source](https://developer.apple.com/documentation/arkit/ardirectionallightestimate)
 -[Apple BlendShapes](hdeveloper.apple.com/documentation/arkit/arfacegeometry)

### Unity Blog
- [ARKit present](https://blogs.unity3d.com/2017/11/03/arkit-face-tracking-on-iphone-x/)
- [Custom emojis](https://blogs.unity3d.com/2017/12/03/create-your-own-animated-emojis-with-unity/)
- [Remote plugin](logs.unity3d.com/2018/01/16/arkit-remote-now-with-face-tracking/)
- [HQ Remote]   ()



Afater
0. Check videos
1. Check AR Fundion examples
2. Check time
3. Speed reating
4. Windup unity project
5. Check Eye tracking and my s

## VISP

As far as I discovered there
is no reason to continue using the 
Vuforia whatsoever.

https://github.com/lagadic/visp_unity/wiki/Unity-AR-demo-using-ViSP
April tag is super asses

## VR 

### Mock

## Ouclus	

### Specs Quest 2 

- [Unity setup](https://developer.oculus.com/unity/)
- [link Andorid Setup](https://developer.oculus.com/documentation/native/android/mobile-studio-setup-android/)

- API Level 26
- Android 8 Oreo 
- Use Oculus XR Plusing not OpenXR plugin


### Questions

- New Unity Input system ?
- Oculus link

### URP

- [Github Repo Best Quest preformance](https://github.com/smitdylan2001/ApplicationSpaceWarp/tree/2021.3)

### Multipass	

- [Multi passes part 1](https://developer.oculus.com/documentation/unity/po-advanced-gpu-pipelines/)

`Single-pass`- is like awesom and e.t.c
but bitch I have like two options 

1. `Multiview` - Single pass instancing rendering
2. `Multi Pass` - Multi rundering


Pass 1 doesn’t get FFR as it’s not rendering to the VrApi swapchain.
Pass 2 doesn’t get FFR as although it is rendering to the VrApi swapchain, it’s no-depth-buffer full-screen-pass executes as Direct Mode, deactivating FFR.

On the tools side, it’s simple to figure out if something is rendering as Direct Mode. The entire surface will render as a “single tile:”

```MarkDown
Surface 1 | 1216x1344 | color 32bit, depth 0bit, stencil 0 bit, MSAA 1 | 1 1216x1344 bins | 2.01 ms | 1 stages : Render 2.01ms
Multiple Passes: Part 2 - Subpass Theory
```

Vulkan has introduced a more tile-friendly way to execute multipass rendering: subpasses. Some extensions try to simulate that behavior on OpenGL ES, such as ARM_framebuffer_fetch, but especially with MSAA, their use is not encouraged.


Surface1 (Pass1)
render
store
render
store

Surface2 (Pass2)
render
store
render
store

to:

Surface1
render
render
store
render
render
store

```
```

### URP build


- It's better to use OepnGL ES now

*Issue: * if using **URP** MSAA level to 4x dosen't see

### Links

- [Oficial Documentation](https://developer.oculus.com/quest/)

### Oculus Link
 
It's to make it work like a desktop headset

### Passthrouh

Allows to work in the XR requires some setting

First of all OpenAR on backednd


1. Color Space Linear 
2. **IL2CPP**
3. **ARM64**
4. XR-Plugin Manger -> Oculus
5. Oculus->Tools->OVR Utilities Plugin


## MRTK

### Installation 

- Mixed Reaality Feature Tool for Unity

` D:\DevTools\MixedReality\MixedRealityFeatureTool.exe` 

Banch of shinanigans


### Hololens 2

- [Microsoft Getting Started Hololsnes](https://docs.microsoft.com/en-us/learn/paths/beginner-hololens-2-tutorials/)
- [HoloLens Learning portal](https://docs.microsoft.com/en-us/hololens/?WT.mc_id=mixedreality_product)
- [Hololens Emulator Archive](https://docs.microsoft.com/en-us/windows/mixed-reality/develop/advanced-concepts/hololens-emulator-archive)

#### Build UWP

- Windows SDK

### MRTK on Oculus Quest 2

Banch of shinanigans
I was trying to make Oculus Quest 2 to work with. 

## Unity Packages

### List

- XR Plugin managment
- XR Interactive Toolkit
- Open XR Plugin
- Oculus XR Plugin

- Widnows XR Plugin
- Magic Leap XR Plguing

#### AR

- AR Foundation
- ARKit XR Plugin
- ARKit Face Tracking
- ARCore XR Plugin

### Questions

- Should I install both OpenXR and OculusXR plugin

## HoloLens2

### Emulator 

**Location:**
> C:\Program Files (x86)\Windows Kits\10\Emulation

#### Fixing NAT Swithch

[Stack overFlow Link](https://superuser.com/questions/1445288/port-forwarding-with-hyper-v-virtual-machine-on-windows-10)

```powershell
New-VMSwitch  -SwitchName "NAT Switch"  -SwitchType Internal
```
