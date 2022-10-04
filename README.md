<p align="center"><img alt="logo" width="150px" src="./src/images/AI-PNG-Picture.png"></p>
<h1 align="center">HAM10000: Skin Cancer MNIST</h1>

## Table of Contents

- [About the Project](#about-the-project)
- [Introduction](#Introduction)
- [Progress so far]()
  - [Data](#Data)
  - [Data Preprocessing](#Data-Augmentation)
  - [Classification Models](#Classification-Models)
  - [Result Analysis](#Result-Analysis)
- [Future Work](#future-work)

## About the Project

It aims at building machine learning based model which will predict the type of skin cancer one has, as well as segment the part of the skin which is infected or cancerous in nature.

## Introduction

Skin problems are really frequent in nature hence easily ignored but sometimes they are fatal in nature and become cancerous in nature and goes undiagnosed leading to permanent disfigurement and even death. Skin cancer, the abnormal growth of skin cells, most often develops on skin exposed to the sun. But this common form of cancer can also ocur on aeas of your skin not ordinarily exposed to sunlight.

There are various types of skin cancers in the realm of pigmented lesions are:
- Actinic keratoses and intraepithelial carcinoma / Bowen's disease
- basal cell carcinoma
- benign keratosis-like lesions (solar lentigines / seborrheic keratoses and lichen-planus like keratoses)
- dermatofibroma
- melanoma
- melanocytic nevi
- vascular lesions (angiomas, angiokeratomas, pyogenic granulomas and hemorrhage)

They are structurally really similar and causes simple irritation with mild to severe pain. We aim at developing models which can be used by different platforms which will takes images of the skin and predict if the growth in skin is cancerous or healthy, and also classify the type of cancer it is. 

## Progress so far

#### Data

The Data that we have used here is like the MNIST for Skin cancer classification. It contains dermatoscopic images from different populations, acquired and stored by different modalities. The final dataset consists of 10015 dermatoscopic images which can serve as a training set for academic machine learning purposes.

- The original Challenge - [ISIC 2018 Challenge](https://challenge.isic-archive.com/landing/2018/)
- The Original way to access it - [Havard's Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)
- Kaggle Link to Access it - [MNIST : HAM10000](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)

#### Data Pre-processing

The data comprises of Images and the CSV files represent the labels in an one-hot encoded manner with the respective image names to match with. As ImageDataGenerator's flow from directory can't accept one hot encoded labels, a label column with labels annoted to them was created.

The labels are :

- AKIEC : Actinic keratoses and intraepithelial carcinoma / Bowen's disease
- BCC   : basal cell carcinoma
- BKL   : benign keratosis-like lesions (solar lentigines / seborrheic keratoses and lichen-planus like keratoses)
- DF    : dermatofibroma
- MEL   : melanoma
- NV    : melanocytic nevi
- VASC  : vascular lesions (angiomas, angiokeratomas, pyogenic granulomas and hemorrhage)

The samples distribution is as follows:

    NV       6384
    MEL      1053
    BKL      1035
    BCC       488
    AKIEC     309
    VASC      138
    DF        107

For simplification the data is undersampled to 300 samples or less.

#### Building Model

As two classes, VASC and DF are having samples less than 300, so we are gonna initialize the weights to compensate the imbalance.

            Class              Samples   Weight  
            AKIEC               300.0    1.00000 
             BCC                300.0    1.00000 
             BKL                300.0    1.00000 
              DF                115.0    2.60870 
             MEL                300.0    1.00000 
              NV                300.0    1.00000 
             VASC               142.0    2.11268 
             
For starters we have used three methods to check the accuracy one can get with undersampled images. They are

- NAS : Neural Architecture Search 
This is an autoML technique which finds it's own best suited architecture but surprisingly it yielded a very poor accuracy of around 25% at max but could not complete it's operation due to lack of hardware.

- EfficientNet B0
This is a transfer learning technique which showed the worst result of only 3%.

- VGG16
So far this has shown the best result of 57% which is still really less when compared to human level efficiency.

#### Result Analysis

EfficientNet B0
<p align="center"><img alt="Accuracy = 3%" src="./Result Analysis/EfficientnetB0 classification report.png"></p>

VGG16
<p align="center"><img alt="Accuracy = 57%" src="./Result Analysis/vgg16 classification report.png"></p>

## Future Work
- Instead of undersampling we must use some synthetic data generation techniques to increase the sample number of minority class.
- We have to use some sort of feature extraction technique before using NN based feature extraction on it.
- The NAS must be deployed with proper space to function and reach it's best architecture
- Different types of architectures must be tried after studying NAS results or by some trial and error method.
- After we are able to classify the data properly we must attempt the segmentation model as well.
