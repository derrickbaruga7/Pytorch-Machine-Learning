# Pytorch-Machine-Learning

This PyTorch project is designed to predict sales based on historical purchase data. It encompasses data cleaning, feature engineering, and model training using a neural network. The neural network employs mean squared error (MSE) as the loss function and leverages mini-batch processing through DataLoader. The final MSE on the test set is approximately 0.1400. Complete code and instructions are available for replication and further experimentation.

### PyTorch Purchase Prediction Model

### Overview

This GitHub project demonstrates a PyTorch-based machine learning model for predicting sales from historical purchase data. It includes:

### 1. Data Preparation:
- Importing necessary libraries such as PyTorch for deep learning, Scikit-learn for data preprocessing, and Matplotlib for data visualization.
- Loading and inspecting the dataset (Sales Data.csv), which contains detailed purchase records.
- Performing data cleaning and feature engineering, including converting categorical variables to dummy variables and standardizing features.
- Splitting the dataset into training and testing sets.

### 2. Model Architecture:
- Building a neural network with three fully connected layers and ReLU activations using PyTorch.
- Training the model using mini-batch processing with DataLoader and optimizing with Adam.

### 3. Training and Evaluation:
- Training the model for 100 epochs while monitoring the mean squared error loss.
- Evaluating the model's performance on the test set, reporting the mean squared error.

### 5. Code and Instructions:
- The repository includes all necessary code and instructions to reproduce and extend the sales prediction model.
