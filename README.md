# CNN for Diabetic Retinopathy

## Data Used
The data used in this project is the Asia Pacific Tele-Ophthalmology Society (APTOS) 2019 Blindness Detection dataset taken from:
https://www.kaggle.com/datasets/mariaherrerot/aptos2019

This dataset contains images belonging to 5 classes
- 0 - no diabetic retinopathy
- 1 - mild
- 2 - moderate
- 3 - severe
- 4 - proliferative

## Data Preprocessing

The data has been divided into training, testing, and validation set using a 80-10-10 split.

The preprocessors in this repo process adn divide the data into a directory structure such that it can be used with TensorFlow's ImageDataGenerator. The images are also scaled to 224x224 size so that it can be used with imagenet weights.

There are 2 preprocessors:
- Multi-class
- Binary

## The Models

There are 2 preprocessors:
- Multi-class
- Binary

The models are identical except the last layer (softmax layer).

The models use VGG16 architecture with imagenet weights and implement transfer learning by training the last block (block 5) of the VGG16 CNN and also training the fully connected layers using the APTOS data.