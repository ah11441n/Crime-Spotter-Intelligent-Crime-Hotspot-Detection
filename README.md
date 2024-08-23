# Crime Spotter: Intelligent Crime Hotspot Detection

**Capstone Project by Aishwarya Hiremath**

## Introduction

In modern urban environments, predicting and preventing crime are paramount challenges for law enforcement agencies. This project leverages machine learning (ML) techniques to address these challenges by developing robust models for crime hotspot detection and spatial-temporal analysis using the NYPD arrest dataset from NYC Open Data. The hypothesis is that advanced ML techniques can predict crime hotspots with greater accuracy than traditional methods. The significance of this project lies in its potential to revolutionize crime prevention strategies, enabling law enforcement to allocate resources more effectively, enhance public safety measures, and potentially reduce crime rates.

## Methodology

### 1. Data Collection and Loading
- **Dataset**: NYPD arrest dataset from NYC Open Data, comprising 63,621 rows and 20 columns of arrest-related information.
- **Initial Analysis**: Inspected for missing values, data discrepancies, and structure.

### 2. Data Preprocessing
- **Renaming Columns**: Columns were renamed for clarity.
- **Deleting Unwanted Columns**: Non-contributory columns were removed.
- **Feature Creation**:
  - **Temporal Features**: Year, month, day of the week, etc.
  - **Description and Class**: Standardized offense descriptions, categorized by severity.
  - **Target Variable "Indicator"**: Marked crimes by severity and recency.

### 3. Handling Duplicates and Outliers
- Ensured no duplicates and all values were within desired ranges.

### 4. Exploratory Data Analysis (EDA)
- Explored distributions, correlations, and trends within the dataset.
- Visualized findings through histograms, maps, and temporal analysis.

### 5. Stratified K-Fold Cross-Validation
- Employed Stratified K-Fold to maintain class distribution across folds for unbiased model evaluation.

### 6. Model Selection and Training
- **ML Models**: K-Nearest Neighbor (KNN), Support Vector Machine (SVM), Naive Bayes (NB), Gradient Boosting Classifier, Logistic Regression.

### 7. Model Evaluation and Optimization
- Evaluated models using metrics like accuracy, precision, recall, F1-score, and confusion matrix.
- Applied regularization to SVM and Gradient Boosting to prevent overfitting.

### 8. Model Comparison and Selection
- Compared models based on performance metrics to select the most effective model for crime hotspot prediction.

## Results

### Model Performance
- **Gaussian Naive Bayes**: 0.77 average validation accuracy.
- **Support Vector Machine (SVM)**: 0.91 average validation accuracy after regularization.
- **K-Nearest Neighbors (KNN)**: 0.97 average validation accuracy.
- **Gradient Boosting Classifier**: 1.00 average validation accuracy (signs of overfitting).
- **Logistic Regression**: 0.97 average validation accuracy.

### Classification Reports and Confusion Matrices
- Detailed analysis of each model's classification performance, including precision, recall, and F1-scores for different crime severity indicators.

## Limitations
- **Overfitting**: The Gradient Boosting Classifier showed signs of overfitting, even after regularization.
- **Dependence on Historical Data**: The reliance on historical arrest data may limit the models' ability to predict emerging crime patterns.

## Conclusion
KNN and Logistic Regression models demonstrated high accuracy and minimal misclassification, making them reliable choices for crime hotspot detection. However, overfitting in the Gradient Boosting Classifier highlighted the need for further refinement. Future work could involve exploring additional features, integrating more diverse data sources, and enhancing model generalization.

---

**Repository Content:**
- `README.md`: Overview and project summary.
- `Data`: Folder containing the dataset (if permissible).
- `Code`: Python scripts for data preprocessing, EDA, and model implementation.
- `Reports`: Detailed analysis, including model performance metrics and visualizations.


---
