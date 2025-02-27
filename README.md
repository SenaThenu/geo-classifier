<div align="center">
  <a href="https://github.com/SenaThenu/geo-classifier">
    <img src="https://github.com//SenaThenu/geo-classifier/blob/main/assets/logo.png?raw=true" alt="Repo Logo" height="170">
  </a>
</div>

<h3 align="center">
  <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Rocket.png" alt="Rocket" width="25" height="25" />
  Geo Classifier
  <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Rocket.png" alt="Rocket" width="25" height="25" />
</h3>

<div align="center">
  <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Activities/Sparkles.png" alt="Sparkles" width="25" height="25" />
  machine learning model to classify geographic landscapes
  <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Activities/Sparkles.png" alt="Sparkles" width="25" height="25" />
</div>

<div align="center">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg?labelColor=003694&color=ffffff" alt="License">
  <img src="https://img.shields.io/github/contributors/SenaThenu/geo-classifier?labelColor=003694&color=ffffff" alt="GitHub contributors" >
  <img src="https://img.shields.io/github/stars/SenaThenu/geo-classifier.svg?labelColor=003694&color=ffffff" alt="Stars">
  <img src="https://img.shields.io/github/forks/SenaThenu/geo-classifier.svg?labelColor=003694&color=ffffff" alt="Forks">
  <img src="https://img.shields.io/github/issues/SenaThenu/geo-classifier.svg?labelColor=003694&color=ffffff" alt="Issues">
</div>

<div align="center">
  
  <strong>Share</strong>

  <a href="https://x.com/intent/tweet?url=https%3A%2F%2Fgithub.com%2FSenaThenu%2Fgeo-classifier&text=check%20out%20this%20cool%20machine%20learning%20project.%20it%20can%20classify%20geogrpahic%20landscapes!&hashtags=opensource%2Cmachinelearning%2Cml%2Ctensorflow">
    <img src="https://img.shields.io/badge/Share_on_X-%23000000.svg?logo=X&logoColor=white" alt="Share on X" />
  </a>
  
</div>

<details>

<summary><strong>Table of Contents 📜</strong></summary>

  - [Purpose 🤔](#purpose-)
  - [Data 📊](#data-)
  - [Built With 🔧](#built-with-)
  - [Modelling Summary 📄](#modelling-summary-)
    - [1. Vanilla CNN Model 💡](#1-vanilla-cnn-model-)
      - [Classification Report ℹ️](#classification-report-)
      - [Error Analysis ⚠️](#error-analysis-)
    - [2. ResNet Model 🥅](#2-resnet-model-)
      - [Classification Report ℹ️](#classification-report-)
      - [Error Analysis ⚠️](#error-analysis-)
    - [3. CNN Ensemble 🤝](#3-cnn-ensemble-)
      - [Classification Report ℹ️](#classification-report-)
      - [Error Analysis ⚠️](#error-analysis-)
  - [Acknowledgments 💝](#acknowledgments-)

</details>

## Purpose 🤔

Classify images of natural scenes into 6 categories: Buildings, Forests, Glaciers, Mountains, Seas, or Streets.


## Data 📊

Data needed to train the machine learning model was extracted from the [Intel Image Classification Dataset on Kaggle](https://www.kaggle.com/datasets/puneet6060/intel-image-classification/data).

## Built With 🔧

[![Python](https://img.shields.io/badge/Python-blue?style=for-the-badge&logo=python&logoColor=FFD43B)](https://www.python.org/)
[![Tensorflow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://colab.research.google.com/)
[![Kaggle](	https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)](https://kaggle.com/)

## Modelling Summary 📄

### 1. Vanilla CNN Model 💡

#### Classification Report ℹ️
```
Classification Report:
              precision    recall  f1-score   support

   buildings       0.31      0.07      0.12       364
      forest       0.28      0.99      0.44       374
     glacier       0.54      0.44      0.49       440
    mountain       0.51      0.29      0.37       413
         sea       0.55      0.12      0.20       423
      street       0.28      0.24      0.26       386

    accuracy                           0.36      2400
   macro avg       0.41      0.36      0.31      2400
weighted avg       0.42      0.36      0.32      2400
```

#### Error Analysis ⚠️

<img src="https://github.com//SenaThenu/geo-classifier/blob/main/assets/vanilla_cnn_performance.png?raw=true" alt="Error analysis illustration of the vanilla CNN model" width="100%">


### 2. ResNet Model 🥅

#### Classification Report ℹ️
```
Classification Report:
              precision    recall  f1-score   support

   buildings       0.88      0.96      0.92       364
      forest       0.99      0.99      0.99       374
     glacier       0.88      0.83      0.86       440
    mountain       0.86      0.84      0.85       413
         sea       0.91      0.97      0.94       423
      street       0.96      0.89      0.92       386

    accuracy                           0.91      2400
   macro avg       0.91      0.92      0.91      2400
weighted avg       0.91      0.91      0.91      2400
```

#### Error Analysis ⚠️

<img src="https://github.com//SenaThenu/geo-classifier/blob/main/assets/resnet_model_performance.png?raw=true" alt="Error analysis illustration of the ResNet model" width="100%">


### 3. CNN Ensemble 🤝

The best-performing CNN model from a CNN model ensemble is chosen. The following statistics are based on that!

#### Classification Report ℹ️
```
Classification Report:
              precision    recall  f1-score   support

   buildings       0.43      0.77      0.55       364
      forest       0.78      0.89      0.83       374
     glacier       0.71      0.58      0.64       440
    mountain       0.58      0.62      0.60       413
         sea       0.70      0.46      0.55       423
      street       0.81      0.53      0.64       386

    accuracy                           0.63      2400
   macro avg       0.67      0.64      0.64      2400
weighted avg       0.67      0.63      0.63      2400
```

#### Error Analysis ⚠️

<img src="https://github.com//SenaThenu/geo-classifier/blob/main/assets/best_cnn_performance.png?raw=true" alt="Repo Logo" width="100%">

## Acknowledgments 💝

- [Readme Forge](https://readme-forge.github.io) - Creating README.md


