# Report: Kaggle "Dogs vs. Cats" Dataset Analysis and Model Development

## 1. Introduction
- This project focuses on developing a machine learning workflow for classifying images of dogs and cats, leveraging the Kaggle "Dogs vs. Cats" dataset.
- We are using Transfer Learning method, which is a model trained on massive dataset (E.g: ImageNet) before fitting the model. This helps reduce the need for a large labeled dataset and saves computation time
- The workflow encompasses data import, preprocessing, modeling, and evaluation.

## 2. Workflow Overview

### 2.1 Data Import
A total of 7 cells are dedicated to downloading and extracting the dataset. The steps include:
- Utilizing the Kaggle API to download the competition data.
- Extracting the contents of the dataset (training and testing sets) into structured directories for further use.
- **Note:** Importing process requires the user to join the [Cats vs Dogs Competition](https://www.kaggle.com/c/dogs-vs-cats/data) as well as generate a User API from the Kaggle profile as a `kaggle.json`

Key tools and libraries:
- **Kaggle API**: For seamless access to competition data.
- **ZipFile**: To handle data extraction from `.zip` archives.

### 2.2 Data Preprocessing
Two cells are allocated to preprocessing, which likely includes:
- Resizing or normalizing image data.
- Splitting the dataset into training and validation subsets.
- Preparing data generators for efficient loading during model training.

### 2.3 Modeling
The core of the notebook lies in this section, with 15 cells detailing:
- Uses **Pre-trained MobileNetV2 Imagenet model** which takes the input of a **color picture** in `224 x 224 pixel`
- Uses **a GlobalAveragesPooling2D layer** to reduces the spatial dimension of the MobileNetV2 from `(None, 7,7,1280)` to `(None,1280)` which help reduces the trainable parameters and help prevents overfitting.
- Final **Dense Layer**: Returns a binary ouput with **Softmax Activation function** 
- **Note:** If your Local Machine can't run the model, consider uploading the notebook on **Google Colab** and start over.

### 2.4 Evaluation
A single cell focuses on evaluating the trained model, possibly measuring metrics such as:
- Optimizer: Adam
- Metrics: Accuracy
- Loss: Sparse Categorical Crossentropy

### 2.5 Visualization
- Examples of correctly and incorrectly classified images.
- Examples of resized image.
