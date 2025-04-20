# Dataset Analysis Report

## Overview

This report presents a basic analysis of the [Dry Bean Dataset](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset) (UCI ML Repository ID: 602).

## Methodology

1. **Data Loading**: Load the Dry Bean Dataset using the UCI ML Repository API.
2. **Data Preprocessing**: Split the dataset into features (X) and target (y). Perform train-test split for model evaluation.
3. **Model Selection**: Use a Nu-Support Vector Classifier (NuSVC) with Bayesian Optimization to optimize hyperparameters.
4. **Model Evaluation**: Evaluate the model's accuracy using cross-validation and convergence plots.
5. **Result Analysis**: Analyze the best hyperparameters and accuracy obtained.

## Dataset Description

The Dry Bean Dataset contains various attributes of dry beans, including geometric, shape, and texture attributes, which are used to classify the beans into different classes.

### Features

The dataset contains the following features:

- **Area**: Area of the dry bean.
- **Perimeter**: Perimeter of the dry bean.
- **MajorAxisLength**: Major axis length of the dry bean.
- **MinorAxisLength**: Minor axis length of the dry bean.
- **AspectRatio**: Aspect ratio of the dry bean.
- **Eccentricity**: Eccentricity of the dry bean.
- **ConvexArea**: Convex area of the dry bean.
- **EquivDiameter**: Equivalent diameter of the dry bean.
- **Extent**: Extent of the dry bean.
- **Solidity**: Solidity of the dry bean.
- **Roundness**: Roundness of the dry bean.
- **Compactness**: Compactness of the dry bean.
- **ShapeFactor1**: Shape factor 1 of the dry bean.
- **ShapeFactor2**: Shape factor 2 of the dry bean.
- **ShapeFactor3**: Shape factor 3 of the dry bean.
- **ShapeFactor4**: Shape factor 4 of the dry bean.

### Target

The target variable is the class of the dry bean.

## Data Exploration

Let's perform some basic exploratory data analysis:

### Summary Statistics

```python
# Summary statistics of the dataset
summary_statistics = X.describe()
print(summary_statistics)
```

```python
# Class distribution
class_distribution = y['Class'].value_counts()
print(class_distribution)
```

```python
import seaborn as sns
# Calculate correlation matrix
correlation_matrix = X.corr()
# Plot heatmap
plt.figure(figsize=(12, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm', fmt=".2f")
plt.title('Correlation Heatmap')
plt.show()
```

