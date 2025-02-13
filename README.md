# RandomForest-Comparison

## Project Overview
This project implements Random Forest classification models to analyze two distinct datasets:
1. A smaller wine quality dataset (~1,000 samples, few features)
2. A larger forest cover type dataset (>100,000 samples, 50+ features)

## Datasets

### Wine Quality Dataset
Contains physical and chemical properties of wine samples including:
- Fixed and volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free and total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol
- Quality (target variable)

### Forest Cover Dataset
Contains cartographic variables from the Roosevelt National Forest in Colorado:

Numerical features:
- Elevation
- Aspect
- Slope
- Horizontal and Vertical Distances (4 distances)
- Hillshade (3 measurements)

Categorical features:
- Wilderness Areas (4 areas)
- Soil Types (38 types)

Target: Cover Type

## Implementation Details

### Data Preprocessing
- Train-test split (70-30)
- SMOTE oversampling for handling class imbalance
- Label encoding for target variables
- Standardization of numerical features

### Model Architecture
Random Forest Classifier with optimized hyperparameters:
- Wine Dataset:
  - n_estimators: 125
  - criterion: "gini"
  - max_depth: 30
  - class_weight: Custom weights per class
  
- Forest Cover Dataset:
  - n_estimators: 140-145
  - criterion: "entropy"
  - max_depth: 40
  - class_weight: "balanced"

## Results

### Wine Quality Dataset
- Accuracy: 64.6%
- OOB Score: 64.8%
- Notable class-wise performance variation due to imbalanced data

### Forest Cover Dataset
- Accuracy: 95.5%
- OOB Score: 96.9%
- Better performance across all classes with feature selection

## Dependencies
- Python 3.x
- pandas
- numpy
- scikit-learn
- imbalanced-learn (for SMOTE)
- matplotlib
- seaborn

## Future Improvements
- Implementation of boosting or stacking ensembles
- Further optimization of class weighting
- Advanced feature selection techniques
- Enhanced handling of class imbalance

## Files
- `WineQT.csv`: Wine quality dataset
- `covtype.csv`: Forest cover type dataset

## Usage
1. Load and preprocess the data
2. Train the Random Forest model with optimized parameters
3. Evaluate performance using provided metrics
4. Optional: Apply feature importance analysis for optimization

## Performance Metrics
The project includes comprehensive evaluation using:
- Accuracy scores
- Confusion matrices
- Class-wise prediction analysis
- Out-of-Bag (OOB) scores
- Feature importance rankings

## DATASETS 
    1. COVER TYPE : https://www.kaggle.com/datasets/uciml/forest-cover-type-dataset
    2. WINE-QUALITY: https://www.kaggle.com/code/mhassansaboor/wine-quality-analysis-plotly

## FOR MORE DETAILS CHECK DOC.pdf and Presentation.pptx