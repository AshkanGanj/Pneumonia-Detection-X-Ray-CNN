# Pneumonia-Detection-X-Ray-CNN

In this project, I am going to create a conventional network for classifying x-ray images as normal or pneumonia.

## Introduction for dataset

The dataset is organized into 3 folders (train, test, val) and contains subfolders for each image category (Pneumonia/Normal). There are 5,863 X-Ray images (JPEG) and 2 categories (Pneumonia/Normal).

![image](https://user-images.githubusercontent.com/55941654/134182083-8057f086-38f9-4298-a8c7-fd45219b8903.png)


Chest X-ray images (anterior-posterior) were selected from retrospective cohorts of pediatric patients of one to five years old from Guangzhou Women and Children’s Medical Center, Guangzhou. All chest X-ray imaging was performed as part of patients’ routine clinical care.

For the analysis of chest x-ray images, all chest radiographs were initially screened for quality control by removing all low quality or unreadable scans. The diagnoses for the images were then graded by two expert physicians before being cleared for training the AI system. In order to account for any grading errors, the evaluation set was also checked by a third expert.

URL: https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

## ConvNet Architecture

Simple sequential model is used, starting with 2 convolutional networks of kernel size (7,7) and max pooling with pool size (3,3), followed by 2 convolutional networks of kernel size (7,7) and same pool size and finalized by several repeating sets of 2 convolutional networks of kernel size (3,3) with max pooling and pool size (2,2).

### Summary of model

I ran the model for ten epochs and got bellow results ( we can get a better result at higher epochs).

![image](https://user-images.githubusercontent.com/55941654/134182996-1bfbe7e7-36d4-405c-b558-867f4e9ea980.png)

### loss and accuracy

![image](https://user-images.githubusercontent.com/55941654/134183586-ad548d52-562e-41ef-8114-c3de454d04d4.png)

### confusion matrix
