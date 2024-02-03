# Artificial Neural Network for Customer Churn Prediction
This repository contains code for a simple Artificial Neural Network (ANN) implemented in Google Colab to predict customer churn based on various features. The dataset used includes the following features: RowNumber, CustomerId, Surname, CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary.

## Structure
The neural network architecture consists of four layers:

### Input Layer:

Units: 11 (corresponding to the number of features)
Activation Function: ReLU (Rectified Linear Unit)

### 1st Hidden Layer:
Units: 7
Activation Function: ReLU

### 2nd Hidden Layer:
Units: 5
Activation Function: ReLU

### Output Layer:
Units: 1
Activation Function: Sigmoid (since it's a binary classification problem)

## Compilation
The model is compiled using the following configurations:

Optimizer: Adam
Loss Function: Binary Crossentropy
Metrics: Accuracy

## Early Stopping
The code incorporates early stopping to prevent overfitting. This is achieved using the EarlyStopping callback from the TensorFlow library.
```
early_stopping = EarlyStopping(monitor='val_loss', patience=3, restore_best_weights=True)
```

## Libraries Used
The implementation relies on the following libraries:

TensorFlow: For building and training the neural network.
Scikit-Learn: For data preprocessing and evaluation.
