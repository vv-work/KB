# OpenCV


## Materials

### Books

- 9.5/10 OpenCV Learning Path Theory+Examples
- 8/10 TenserFlow 2.0

- 7.5 openCv Cookbook
  - C++ based.

- 7.5 OpenCV ProProcessing
  - Java based.

- 7/10 Hands-on ML Kera ch14 CNN CV.
- 7/10 Rabbit algos AI

- Learning OpenCV 3 Big and detailed
  - C+++ 
  - More like ditailed catalog.

- Numerical for  CV to deep into math
  - Really ditailed on the Math behind.

- CV Algos and Applience Szelinsky to deep into math

- Ml for OpenCV a bit dig down
 - Just Theory No practice:

### Libs

- TenserFlkow CV on google
- OpenCV Library for Unity
- OpenCV Library for Python

### course
- 7.5/10 ML TenserFlow Keras
- 7.5/10 ML TenserFlow Keras


### Code examples

- OpenCV for Unity
- Books by examples
- Github Repos
- ML.NET full of great things

### Ml.NET

-[Taco vs Burito](https://github.com/sethjuarez/TacosML)

- [Object Detection ONNX Article](https://docs.microsoft.com/en-us/dotnet/machine-learning/tutorials/object-detection-onnx)
- [Object Detection](https://github.com/dotnet/machinelearning-samples/tree/main/samples/csharp/getting-started/DeepLearning_ObjectDetection_Onnx)
- [Image classifification Model API](https://github.com/dotnet/machinelearning-samples/tree/main/samples/csharp/getting-started/DeepLearning_ImageClassification_Training)
- [Image classifing scoring ](https://github.com/dotnet/machinelearning-samples/tree/main/samples/csharp/getting-started/DeepLearning_ImageClassification_TensorFlow)
- [ Image classification training](https://github.com/dotnet/machinelearning-samples/tree/main/samples/csharp/getting-started/DeepLearning_TensorFlowEstimator)


## Basics

Basic import

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt 
```

### Channels
```python
img=cv2.imread('image.jpg',1)

g,b,r = cv2.split(img)
gbr_img = cv2.merge((g,b,r))
rbr_img = cv2.merge((r,b,r))
```

### Scaling
```python
scale = 0.25
img_scaled = cv2.resize(img,None,fx=scale, fy=slale, interpolation = cv2.INTER_LINEAR)
```

```python
img = cv2.imread('image.jpg')

laplacian = cv2.Laplacian(img,cv2.CV_64F)

sobelx = cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)

edges= cv2.Canny(img,500,500)

cv2.imshow('laplacia',laplacian)
cv2.imshow('soblx', sobelx)
cv2.imshow('soboly',sobely)
cv2.imshow('edges',edges)
```
### Shzelinski Model
[](/AI/Res/Szhelinski.png       )

### Todo

- [x] What usefull materials I have ?
- [ ] Examples with for Unit Tests.
- [ ] Haar cascade in deep
- [ ] Learning by examples?