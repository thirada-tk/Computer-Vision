# 🖼️ Convolutional Neural Networks for Food101 Dataset 🥘
_Author: Thirada Tiamklang_

## ✔️Project Overview

This project explores the application of __Convolutional Neural Networks (CNNs) for food image classification using the Food101 dataset__. Three pre-trained _models—GoogLeNet, MobileNetV3, and NASNet—_ were evaluated using transfer learning. MobileNetV3 was selected for fine-tuning due to its balance between performance and computational efficiency.

## 📁 Dataset Description

The Food101 dataset consists of 101 food categories with a total of 101,000 images. The dataset was processed as follows:
1. __Sampled 6%__ of the dataset (6,060 images)
2. __Split__ into training (70%), validation (15%), and test (15%) sets
3. __Image resizing__ based on model requirements:
* __GoogLeNet__: 229x229 pixels
* __MobileNetV3__: 224x224 pixels
* __NASNet__: 331x331 pixels

## 🧰 Model Architectures & Training

#### 1. GoogLeNet
* Uses Inception modules for efficient computation.
* Pre-trained layers frozen, with a new classification head.
* Test Accuracy: _68.1%_
#### 2. MobileNetV3
* Optimized for efficiency with inverted residual blocks.
* Pre-trained layers frozen, with a new classification head.
* Test Accuracy: _73.27%_
#### 3. NASNet
* Designed using Neural Architecture Search (NAS).
* More complex but computationally intensive.
* Test Accuracy: _77.12%_
  
## 🔊Fine-Tuning MobileNetV3
* Due to GPU constraints, __MobileNetV3__ was selected for fine-tuning instead of NASNet.
* Unfroze specific layers (Layer 12 & 14) and retrained.
* ✅ Final Test Accuracy after fine-tuning: _86.58% (13% improvement)_

---
## Limitations & Future Work

* __GPU Constraints__: NASNet fine-tuning was not feasible due to long training times.
* __Overfitting__: Needs further tuning and regularization techniques.
* __Dataset Expansion__: Using more images could enhance generalization.
* Alternative Architectures: Exploring newer CNN models could yield better results.
