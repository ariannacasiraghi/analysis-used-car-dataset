# Analysis of a used car dataset

## Project Overview
This project was completed as part of the **Programming for Data Science module in the MSc in AI program at the University of Leeds**. The task was to explore how various car characteristics influence their market value and to develop predictive models capable of estimating car prices and determining whether a car was involved in an accident based on the provided features.

## Objectives
- **Objective 1:** understand how the various features of the dataset affect the car price both qualitatively (using specific visualization tools) and quantitatively (through correlation).
- **Objective 2:** develop a random forest regression model that is capable of predicting the car price based on selected features from the dataset and evaluate the prediction accuracy of the model using appropriate metrics.
- **Objective 3:** develop a random forest classification model that is capable of predicting whether a car was involved in an accident based on selected features from the dataset and evaluate the classification accuracy of the model using appropriate metrics.

## Datasets
The dataset can be found [here](https://www.kaggle.com/datasets/taeefnajib/used-car-price-prediction-dataset). This dataset is rather small; it comprises 4,009 entries, each corresponding to a unique car listing, and for each car, it contains information regarding several features/properties. According to the description of the dataset, this data was scraped from the web. 

## Methods
**Preliminary steps:**
- Exploratory data analysis
- Data cleaning
- Feature engineering
**Objective 1:**
- Visualize car price distribution
- Plot the effect of various features on car price
- Investigate correlation (Spearman) between numerical features
**Objective 2:**
- Data preprocessing (imputing and encoding)
- Build and fit a random forest regression model on the training data. The model was tuned using grid search and cross validation.
- Model evaluation (R2 score)
 **Objective 3:**
- Data preprocessing (imputing and encoding)
- Build and fit a random forest classification model on the training data. The model was tuned using grid search and cross validation.
- Model evaluation (macro recall, confusion matrix)

## Results
- The car price follows a log-normal distribution and is mostly influenced by mileage and car age (among the numerical features) and brand and fuel type (among the categorical features).
- The R2 score of the regression model built to predict car price is rather low both on the training (0.47) and test (0.45) data, possibly due to the small and noisy nature of the dataset and the fact that outliers were not removed.
- The macro recall score of the classification model built to predict whether a car was involved in an accident is also rather low both on the training (0.72) and test (0.64) data, possibly due to the small and noisy nature of the dataset and the fact that outliers were not removed.


## How to Run
- git clone [analysis-used-car-dataset](https://github.com/ariannacasiraghi/analysis-used-car-dataset.git)
- `pip install -r requirements.txt`
- `jupyter notebook analysis-used-car-dataset.ipynb`
