# Retail-Demand-Foreceast

This repository showcases the implementation and comparison of two powerful ensemble learning models: Random Forest and LightGBM. Both models are widely used in various machine learning tasks and offer unique advantages in terms of performance, speed, and handling of data.


## Dataset

Original dataset include
- Store: Range from 1-45
- Departments: Range from 1-99
- Temperature
- Size
- Sale Type: 3 types A,B,C
- Date: Range from 2010-2012
- **Weekly Sales** [Target]

Additionally new featues added 
- CPI
- Unemployment Rate
- Holidays

## Models

### **Random Forest**

Random Forest is an ensemble learning method that builds a forest of decision trees during training. It utilizes bagging and feature randomness techniques to create diverse trees and improve prediction accuracy. 

* Bagging: Improves model robustness by training each tree on a random subset of the data
* Feature Randomness: Introduces randomness in feature selection to reduce overfitting and improve generalization
* Ensemble of Trees: Combines predictions from multiple decision trees to make final predictions, resulting in a robust and stable model

### **LightGBM**

LightGBM is a gradient boosting framework designed for efficient and distributed training of decision trees. It offers superior speed and performance, making it suitable for large-scale datasets.

* Gradient Boosting: Boosts model performance by sequentially training decision trees to correct errors made by previous trees.
* Fastness: Utilizes efficient algorithms for tree building and leaf-wise growth, resulting in faster training times.
* Leaf-wise Growth: Grows trees leaf-wise, leading to a more complex tree structure and improved predictive performance.

## Results

| Model | Info | RMSE |
|----------|----------|----------|
| Random Forest | All Features | 16,811 |
| Random Forest| w/New Features | 16,827 |
| Random Forest | Feature Enginnering | 16,782 |
| LightGBM | All Features | 16,697 |
| LightGBM|  Feature Enginnering | 16,690 |


### Environment


```BASH
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```