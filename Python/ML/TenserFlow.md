# TensorFlow

Author
>Vadim Kaprsenko

## Materials 

## Terminology

### CNN

**CNN** - **C**onvolusional **N**eruro **N**etword
Text prediction

### RNN

**RNN** - **R**reocoring **N**eruro **N**etword
Sequency analyzer like sound.

## TenserFlow Object Detection API

## DeepMac

[NoteBook on WildCam](https://www.kaggle.com/vighneshbgoogle/iwildcam-visualize-instance-masks) I
[DeepMac Class Segmentation](https://github.com/tensorflow/models/blob/master/research/object_detection/colab_tutorials/deepmac_colab.ipynb)
[DeepMac research](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/deepmac.md)

### DeepMAC architecture


We have released our new architecture, DeepMAC, desgined for partially supervised instance segmentation. DeepMAC stands for Deep Mask-heads Above CenterNet, and is based on our CenterNet implementation. In our paper we show that DeepMAC achieves state-of-the-art results for the partially supervised instance segmentation task without using any specialty modules or losses; just better mask-head architectures. The findings from our paper are not specific to CenterNet and can also be applied to Mask R-CNN or without any detector at all. Please see links below for more details

#### DeepMAC documentation

Mask RCNN code in TF Model garden code base.
DeepMAC Colab that lets you run a pre-trained DeepMAC model on user-specified boxes. Note that you are not restricted to COCO classes!
Project website - git.io/deepmac

### TensorFlow 2 Support

We are happy to announce that the TF OD API officially supports TF2! Our release includes:
New binaries for train/eval/export that are designed to run in eager mode.
A suite of TF2 compatible (Keras-based) models; this includes migrations of our most popular TF1.x models (e.g., SSD with MobileNet, RetinaNet, Faster R-CNN, Mask R-CNN), as well as a few new architectures for which we will only maintain TF2 implementations:

### CenterNet

 a simple and effective anchor-free architecture based on the recent Objects as Points paper.

### EfficientDet

a recent family of SOTA models discovered with the help of Neural Architecture Search.
COCO pre-trained weights for all of the models provided as TF2 style object-based checkpoints.

### MobileDet GPU

We have released SSDLite with MobileDet GPU backbone, which achieves 17% mAP higher than the MobileNetV2 SSDLite (27.5 mAP vs 23.5 mAP) on a NVIDIA Jetson Xavier at comparable latency (3.2ms vs 3.3ms).

Along with the model definition, we are also releasing model checkpoints trained on the COCO dataset.

### Context R-CNN

We have released Context R-CNN, a model that uses attention to incorporate contextual information images (e.g. from temporally nearby frames taken by a static camera) in order to improve accuracy. Importantly, these contextual images need not be labeled.

R-CNN outperforms
single-frame baseline by 17.9% mAP,
and outperforms **S3D** (3d convolution based baseline) by 11.2% mAP