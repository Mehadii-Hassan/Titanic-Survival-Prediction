# Titanic Survival Prediction

A machine learning project that predicts passenger survival on the Titanic using logistic regression.

## Overview

This project analyzes the famous Titanic dataset to predict which passengers survived the sinking of the RMS Titanic. It includes data exploration, cleaning, feature engineering, and model training.

## Dataset

- **Source**: `titanic.csv`
- **Observations**: 891 passengers
- **Features**: 12 variables

## Project Structure

### 1. Data Exploration
- Loaded and examined the dataset
- Analyzed data shape, columns, and sample records
- Calculated missing values and duplicates
- Identified numerical and categorical features

### 2. Data Visualization
- Distribution plots for numerical features
- Count plots for categorical features
- Correlation heatmap

### 3. Data Cleaning & Preprocessing
- **Missing Values**:
  - `Age`: Imputed with median (177 missing - 19.87%)
  - `Embarked`: Imputed with mode (2 missing)
  - `Cabin`: Dropped (too many missing values)
- **Dropped Columns**: PassengerId, Name, Ticket

### 4. Feature Engineering
- Converted `Sex` to binary (`is_male`)
- One-hot encoded `Pclass` and `Embarked`
- Created `FamilySize` from `SibSp` and `Parch`
- Applied StandardScaler to `Age`, `Fare`, `FamilySize`

### 5. Model Training
- **Algorithm**: Logistic Regression
- **Train/Test Split**: 80/20
- **Evaluation Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1 Score
  - F-beta Score

## Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
```

## Usage

Run the notebook in Jupyter or any compatible environment:

```bash
jupyter notebook Titanic_Survival_Prediction.ipynb
```

## Results

The model uses logistic regression to predict survival with the following features:
- Age (scaled)
- Fare (scaled)
- FamilySize (scaled)
- is_male
- Pclass (one-hot encoded)
- Embarked (one-hot encoded)

## License

MIT License
