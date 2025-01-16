# Cat vs Dog Classification using Transfer Learning
# Theories
- **Transfer Learning** is a Deep Learning technique where we use a pre-trained model. This pre-trained model is trained for one task and can be re-trained for a similar task with a smaller dataset. 
  - Transfer Learning gives higher accuracy compared to training models from scratch.
- Example:
  - VGG-16
  - ResNet50
  - Inceptionv3
  - MobileNet v2
- We are using MobileNet for this project
# Workflow
- Collect the data (from Kaggle) [Kaggle](https://www.kaggle.com/c/dogs-vs-cats/data)
- Image processing
- Train test split
- Pretrained MobileNet Model on Dog and Cat dataset
- Prediction when input a dog or cat image
 