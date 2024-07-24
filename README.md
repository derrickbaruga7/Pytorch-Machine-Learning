# Pytorch-Machine-Learning

This PyTorch project predicts sales using historical purchase data. It includes data cleaning, feature engineering, and model training with a neural network. The model uses mean squared error loss and mini-batch processing via `DataLoader`. The final test set MSE is approximately 0.9664. Full code and instructions are provided.

### PyTorch Purchase History Prediction Model

This GitHub project showcases a PyTorch-based machine learning model designed to predict sales based on historical purchase data. The project begins with importing essential libraries, including PyTorch for deep learning, Scikit-learn for preprocessing, and Matplotlib for data visualization. 

The dataset, sourced from 'Sales Data.csv', contains detailed purchase records, including order details, product categories, and sales information. The initial steps involve loading the dataset, performing data cleaning, and feature engineering. Categorical variables are converted to dummy variables, and time-based features are extracted from the 'Order Date' column. The dataset is then standardized and split into training and testing sets.

The core of the project is a neural network model built using PyTorch. The model architecture includes three fully connected layers with ReLU activations, designed to predict sales from the processed features. Training and evaluation are carried out with the help of PyTorch's `DataLoader` for mini-batch processing.

The training loop involves minimizing the mean squared error loss over 100 epochs, with periodic loss reporting. The final evaluation on the test set provides insights into the model's performance, with a mean squared error of approximately 0.9664.

This repository includes all code and instructions necessary to replicate and extend the sales prediction model, offering a robust framework for applying deep learning to sales forecasting.
