<h1 align="center">HAM10000: Skin Cancer MNIST</h1>

## Table of Contents

- [About the Project](#about-the-project)
- [Introduction](#Introduction)
- [Progress so far]()
  - [Data](#Data)
  - [Data Augmentation](#Data-Augmentation)
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

### Data

The Data that we have used here is like the MNIST for Skin cancer classification. It contains dermatoscopic images from different populations, acquired and stored by different modalities. The final dataset consists of 10015 dermatoscopic images which can serve as a training set for academic machine learning purposes.

- The original Challenge - [ISIC 2018 Challenge](https://challenge.isic-archive.com/landing/2018/)
- The Original way to access it - [Havard's Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)
- Kaggle Link to Access it - [MNIST : HAM10000](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)
