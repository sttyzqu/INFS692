# DATA SCIENCE FINAL PROJECT

## Objective

The objective of this project is to develop different models to predict failure (endpoint)
of the radiomics signature based from MRI, PET and CT scans.

## Dataset

radiomics.csv contains 197 rows and 498 columns:
Failure.binary: binary property to predict

## About the file

In **model1.rmd**, we will perform 3 types of Ensemble Classification Model such as:

1. **Bagging** -The advantage of using bagging in machine learning  reduces the variance, minimizes the overfitting of data and and improves the model's accuracy.

2. **Random forests** - are built using the same fundamental principles as decision trees and bagging. Random forests help to reduce tree correlation by injecting more randomness into the tree-growing process. 

3. **Support Vector Machine** - is capable of handling any number of classes and observations of any dimension. SVM can perform linear, radial, and polynomial and other classifier.

Every classification model will split the data into training (80%) and testing (20%). we print the AUC values during training and testing data. Using AUC-ROC curve helps us visualize how well our machine learning classifier is performing for testing data. We will compute the top 20 important features during Training.

In **model2.rmd**, we will perform neural network-based classification model. In this model, we will create five hidden layers with 256, 128, 128, 64 and 64 neurons, respectively
with activation functions of Sigmoid. we will create an output layer with ten neurons respectively with activation functions
of Softmax. Every layer is followed by a dropout to avoid overfitting. we will do backpropagation compiler approach and model compiler approach. We will train the model with epoch = 10, batch size = 128 and validation split = 0.15. We will evaluate the trained model using the testing dataset and get the model prediction.

In **model3.rmd**, without considering the binary output and categorical variables in the dataset, we will compare the following clustering technique results such as **K-Means, Hierarchical and Model Based**.

## Data Pre-Processing

Before running these models, we perform **data pre-processing** such as we check for null and missing values, check for normality, if not, normalized the data and get the correlation of the whole data expect the categorical variables.




