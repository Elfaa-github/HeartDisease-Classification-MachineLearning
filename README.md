# Heart Disease Classification Using Machine Learning

## Overview

This project implements a **binary classification model using Logistic Regression from scratch** to classify heart disease status based on selected clinical features. The model is trained using gradient descent and evaluated using performance metrics and 5-fold cross-validation.

The project demonstrates the fundamental steps of a machine learning workflow, from data preparation and feature scaling to model training, prediction, and evaluation.

## Objectives

- Explore and prepare the heart disease dataset.
- Select relevant clinical features for classification.
- Implement Logistic Regression using NumPy.
- Train the model using gradient descent and the binary cross-entropy loss function.
- Evaluate model performance using classification metrics.
- Assess model consistency using 5-fold cross-validation.

## Dataset

The dataset is obtained from the **UCI Machine Learning Repository**, specifically the Heart Disease dataset.

- **Dataset ID:** 45
- **Source:** [UCI Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)
- **Selected features:**
  - `age`: Age of the patient.
  - `trestbps`: Resting blood pressure.
  - `chol`: Serum cholesterol level.
  - `thalach`: Maximum heart rate achieved.
- **Target variable:** Heart disease status, converted into a binary classification target.

The original target values are converted as follows:

- `0`: No heart disease indicated by the dataset.
- `1`: Heart disease indicated by the dataset.

Any original target value greater than zero is classified as `1`.

## Technologies Used

- **Python** — Programming language
- **NumPy** — Numerical computation and model implementation
- **Pandas** — Data handling and exploration
- **Matplotlib** — Data visualization
- **ucimlrepo** — Retrieving the dataset from the UCI Machine Learning Repository

## Methodology

### 1. Data Loading and Exploration
Retrieve the dataset using `ucimlrepo`, inspect the selected features, calculate descriptive statistics, and check for missing values.

### 2. Feature Selection
Use four clinical features: age, resting blood pressure, cholesterol, and maximum heart rate achieved.

### 3. Target Preparation
Convert the original target into a binary variable for heart disease classification.

### 4. Train-Test Split
Randomly divide the data into:
- **80% training data**
- **20% testing data**

A random seed of `42` is used to make the initial data split reproducible.

### 5. Feature Scaling
Apply manual Min-Max scaling based on the minimum and maximum values of the training data. Use the same scaling parameters to transform the test data to help prevent data leakage.

### 6. Logistic Regression Implementation
Implement Logistic Regression from scratch using NumPy, including:
- Sigmoid activation function
- Binary cross-entropy loss
- Gradient descent
- Weight and bias updates
- Probability-based classification with a threshold of `0.5`

The initial training uses a learning rate of `0.01` and `7,000` iterations.

### 7. Model Evaluation
Evaluate the predictions on the test set using:
- **Accuracy:** Overall proportion of correct predictions.
- **Precision:** Proportion of positive predictions that are correct.
- **Recall:** Proportion of actual positive cases correctly identified.
- **F1-Score:** Harmonic mean of precision and recall.

A confusion matrix is also calculated manually using true positives, true negatives, false positives, and false negatives.

### 8. 5-Fold Cross-Validation
Perform 5-fold cross-validation to evaluate the model across multiple data splits. The dataset is divided into five folds, with each fold used for testing once while the remaining folds are used for training.

The accuracy of each fold and the average accuracy are calculated and visualized using a bar chart.

## Project Structure

```text
.
└── Heart_Disease_Classification_Machine_Learning.ipynb
```

The notebook contains the complete implementation, including data exploration, preprocessing, model training, evaluation, and visualization.

## Installation

Make sure Python is installed, then install the required libraries:

```bash
pip install numpy pandas matplotlib ucimlrepo jupyter
```

## How to Run

1. Clone or download this repository.
2. Open a terminal in the project directory.
3. Launch Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `Heart_Disease_Classification_Machine_Learning.ipynb`.
5. Run the notebook cells sequentially.
6. Ensure you have an internet connection to retrieve the dataset from the UCI repository.

You can also open the notebook in Google Colab by uploading the `.ipynb` file.

## Results and Visualization

The notebook produces the following outputs:

- Selected feature data and descriptive statistics.
- Missing-value checks and target class distribution.
- Trained model weights and bias.
- Training loss history plot.
- Sample predictions compared with actual labels.
- Accuracy, precision, recall, and F1-score.
- Accuracy results for each cross-validation fold.
- A bar chart showing the 5-fold cross-validation results and average accuracy.

The numerical results are generated when the notebook is executed. No fixed performance values are reported in this README.

## Learning Resources

For additional guidance and learning material, watch the following video:

[**Heart Disease Classification — Machine Learning Tutorial**](https://youtu.be/8sxo-AGWAOs?si=_fIjjBAGEn2o8br8)

## Limitations

- The model uses only four selected clinical features.
- Performance depends on the dataset, selected features, and training configuration.
- The cross-validation procedure uses accuracy as its evaluation metric.
- The implementation is intended for educational purposes and is not a validated clinical diagnostic tool.

**Disclaimer:** This project is for educational and research purposes only. Its predictions must not be used as a substitute for professional medical advice, diagnosis, or treatment.

## Authors

- Putri Tajudin
- Zahra Elfatima

## License

No license has been specified for this project. Add a `LICENSE` file if you intend to distribute or reuse the code under a particular license.

