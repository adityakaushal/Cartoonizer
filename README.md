# Toon-it

This is a web app to make real world images to cartoon like artist drawn images. This work is based on 2020 CVPR paper: Learning to Cartoonize Using White-box Cartoon Representations and is Licensed under the [CC BY-NC-SA 4.0 license](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode), due to use of citated code of original research.

**Technologies used: Tensorflow, Flask, HTML**

## Installation

```
python3 -m pip install -r requirements.txt
python3 main.py
(tada webapp is running in =>

localhost:5000/)
```

You can look at your [demo here](https://github.com/Toon-It/Cartoonizer/blob/master/demo.md).

This webapp was featured in top 5 📈  trending projects in [MadeWithML](https://madewithml.com/projects/2125/toonit-now/)

<img src='paper/shinjuku.jpg' align="left" width=1000>

<br><br><br>

# [CVPR2020]Learning to Cartoonize Using White-box Cartoon Representations
[project page](https://systemerrorwang.github.io/White-box-Cartoonization/) |   [paper](https://github.com/SystemErrorWang/White-box-Cartoonization/blob/master/paper/06791.pdf) |   [twitter](https://twitter.com/IlIIlIIIllIllII/status/1243108510423896065) |   [zhihu](https://zhuanlan.zhihu.com/p/117422157) |   [bilibili](https://www.bilibili.com/video/av56708333)

Tensorflow implementation for CVPR2020 paper “Learning to Cartoonize Using White-box Cartoon Representations”.

<img src="images/method.jpg" width="1000px"/>
<img src="images/use_cases.jpg" width="1000px"/>

## Use cases

### Scenery
<img src="images/city1.jpg" width="1000px"/>
<img src="images/city2.jpg" width="1000px"/>

### Food
<img src="images/food.jpg" width="1000px"/>

### Indoor Scenes
<img src="images/home.jpg" width="1000px"/>

### People
<img src="images/person1.jpg" width="1000px"/>
<img src="images/person2.jpg" width="1000px"/>

### More Images Are Shown In The Supplementary Materials

## Prerequisites

- Training code: Linux or Windows
- NVIDIA GPU + CUDA CuDNN for performance
- Inference code: Linux, Windows and MacOS


## How To Use

### Installation

- Assume you already have NVIDIA GPU and CUDA CuDNN installed 
- Install tensorflow-gpu, we tested 1.12.0 and 1.13.0rc0 
- Install scikit-image==0.14.5, other versions may cause problems


### Inference with Pre-trained Model

- Store test images in /test_code/test_images
- Run /test_code/cartoonize.py
- Results will be saved in /test_code/cartoonized_images


### Train

- Place your training data in corresponding folders in /dataset 
- Run pretrain.py, results will be saved in /pretrain folder
- Run train.py, results will be saved in /train_cartoon folder
- Codes are cleaned from production environment and untested
- There may be minor problems but should be easy to resolve
- Pretrained VGG_19 model can be found at following url:
https://drive.google.com/file/d/1j0jDENjdwxCDb36meP6-u5xDBzmKBOjJ/view?usp=sharing



### Datasets

- Due to copyright issues, we cannot provide cartoon images used for training
- However, these training datasets are easy to prepare
- Scenery images are collected from Shinkai Makoto, Miyazaki Hayao and Hosoda Mamoru films
- Clip films into frames and random crop and resize to 256x256
- Portrait images are from Kyoto animations and PA Works
- We use this repo(https://github.com/nagadomi/lbpcascade_animeface) to detect facial areas
- Manual data cleaning will greatly increace both datasets quality

## Acknowledgement

We are grateful for the help from Lvmin Zhang and Style2Paints Research

- [Creating tflite model](https://colab.research.google.com/github/margaretmz/CartoonGAN-e2e-tflite-tutorial/blob/master/ml/CartoonGAN_TFLite_Fixed_Shaped.ipynb)

## License
This project is Licensed under the CC BY-NC-SA 4.0 license (https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode), due to use of citated code for our research.

## Citation

If you use this code for your research, please cite our [paper](https://systemerrorwang.github.io/White-box-Cartoonization/):

@InProceedings{Wang_2020_CVPR,
author = {Wang, Xinrui and Yu, Jinze},
title = {Learning to Cartoonize Using White-Box Cartoon Representations},
booktitle = {IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
month = {June},
year = {2020}
}

