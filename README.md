[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![Made withJupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)](https://jupyter.org/try)
# Pneumonia-Detection-X-Ray-CNN

In this project, I am going to create a conventional network for classifying x-ray images as normal or pneumonia.

## Introduction for dataset

The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).

![image](https://user-images.githubusercontent.com/55941654/134182083-8057f086-38f9-4298-a8c7-fd45219b8903.png)


Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

For the analysis of chest x-ray images, all chest radiographs were initially screened for quality control by removing all low quality or unreadable scans. The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert.

URL: https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

## Data visualization

As it is evident, we have imbalanced data in both training and validating set some we should solve this problem by creating new data with data augmentation.

![image](https://user-images.githubusercontent.com/55941654/134185617-2ef897b6-c65a-4ecc-a047-7117921790dd.png)

## Preview sample images

![image](https://user-images.githubusercontent.com/55941654/134184814-31a0ced4-ba21-4f81-9a36-3d345dc90c7a.png)


## ConvNet Architecture

Simple sequential model is used, starting with 2 convolutional networks of kernel size (7,7) and max pooling with pool size (3,3), followed by 2 convolutional networks of kernel size (7,7) and same pool size and finalized by several repeating sets of 2 convolutional networks of kernel size (3,3) with max pooling and pool size (2,2).

### Summary of model
![image](https://user-images.githubusercontent.com/55941654/134191450-c48f8226-ffa8-463d-becc-92daf1bf3077.png)

## Result

I ran the model for ten epochs and got bellow results ( we can get a better result at higher epochs).

### loss and accuracy

![image](https://user-images.githubusercontent.com/55941654/134185649-29c85f70-b569-4b47-bc63-4170ecc5eaa0.png)

### confusion matrix

![image](https://user-images.githubusercontent.com/55941654/134191126-532d470d-384e-4444-aced-27fabddc1c86.png)

## Test
![image](https://user-images.githubusercontent.com/55941654/134191234-ecd671f3-e907-4a6b-b33c-060596f98a48.png)

