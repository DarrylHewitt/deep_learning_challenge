# deep_learning_challenge

# Project Overview

## Goal
The goal of this project was to develop a binary classification model using machine learning and neural networks to predict the success of organizations funded by the nonprofit foundation Alphabet Soup. The model aimed to assist in selecting applicants with the best chance of success in their ventures.

## Dependencies
- pandas
- scikit-learn
- TensorFlow
- Keras

## Usage
1. Uploaded the starter file, "charity_data.csv," to Google Colab.
2. Followed the instructions in "AlphabetSoupCharity.ipynb" for data preprocessing, model compilation, training, and evaluation.
3. Optionally explored model optimization in "AlphabetSoupCharity_Optimization.ipynb."
4. Reviewed the README file for detailed project information, instructions, and dependencies.

## Steps

### Step 1: Data Preprocessing
1. Read the provided CSV file, "charity_data.csv," into a Pandas DataFrame.
2. Identified the target variable(s) and feature(s) for the model, dropping the "EIN" and "NAME" columns.
3. Determined the number of unique values for each column.
4. Binned rare categorical variables, combining them into a new value, "Other."
5. Used `pd.get_dummies()` to encode categorical variables.
6. Split the preprocessed data into features (X) and target (y), and further split it into training and testing datasets.
7. Scaled the training and testing features using `StandardScaler()`.

### Step 2: Model Compilation, Training, and Evaluation
1. Designed a neural network model using TensorFlow and Keras.
2. Created hidden layers with appropriate activation functions.
3. Compiled and trained the model, implementing a callback to save weights every five epochs.
4. Evaluated the model using the test data to calculate loss and accuracy.
5. Saved the model results to an HDF5 file named "AlphabetSoupCharity.h5."

### Step 3: Model Optimization
1. Experimented with various model optimizations:
   - Adjusted input data (dropped columns, created more bins, etc.).
   - Modified hidden layers (added neurons, added layers, changed activation functions).
   - Adjusted training parameters (epochs, batch size).
2. Created a new Colab file, "AlphabetSoupCharity_Optimization.ipynb."
3. Imported dependencies, read in the data, and preprocessed it based on optimization modifications.
4. Designed a new neural network model optimized for higher than 75% accuracy.
5. Saved and exported the optimized model results to an HDF5 file named "AlphabetSoupCharity_Optimization.h5."

### Step 4: Report Writing

# Analysis Overview

## Purpose
The purpose of this analysis is to develop a neural network model for predicting the success of charity organizations based on various input features. The target variable is "IS_SUCCESSFUL," representing the outcome of the charity.

## Data Preprocessing

### Target Variable
- **IS_SUCCESSFUL:** Represents the outcome of the charity (successful or not).

### Features
- All other columns in the dataset, excluding redundant variables.

### Variables Removed
- **EIN:** Removed as it is redundant and could lead to overfitting and computational inefficiencies.

## Compiling, Training, and Evaluating the Model

### Model Architecture
- Three layers with 80, 30, and 20 units respectively.
- Activation functions: ReLU for the first three layers and Sigmoid for the output layer.

### Model Performance
- Achieved a 5% improvement in model performance.

### Steps to Increase Performance
- Experimented with keeping the "NAME" feature.
- Adjusted bin sizes for names.
- Modified the number of nodes and layers in the neural network.

## Summary

The analysis involved developing a neural network model to predict charity success. The removal of the redundant EIN variable was crucial for model efficiency. Experimenting with the inclusion of the "NAME" feature and adjusting bin sizes for names, along with tuning the model architecture, resulted in a 5% improvement.

## Recommendation

Considering the nature of the problem, alternative models such as decision trees, random forests, or gradient boosting could be explored. These models often perform well in classification tasks and can provide insights into feature importance. Additionally, ensemble methods like random forests may offer robustness against overfitting and improve interpretability.

## Conclusion

The neural network model showed promising results with the implemented changes. However, exploring alternative models like decision trees or ensemble methods could offer additional insights and potentially enhance the overall predictive performance of the classification problem.


