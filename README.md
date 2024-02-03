Koala Kubs Diabetes Classification

This folder contains all the jupyter notebooks used in the CIS520 final project for team Koala Kubs. In this project, using responses to the CDC's Behavioral Risk Factor Surveillance System (BRFSS) from 2011-2015 ([1], [2]), we optimize and compare several binary classification models’ performance in accurately predicting diabetic status using a curated set of questions from the survey. Below is a summary of each file you will find in this folder:
        
1) clean_dataset.ipynb: notebook for preprocessing and cleaning the raw data from Kaggle ([1], [2])
    
2) comparison_across_years.ipynb: notebook for assessing and comparing LightGBM model’s (best classification model on the test set) performance on cleaned dataset of different years, and feature importance across years using SHAPley values
    
3) Data_Exploration.ipynb: notebook for summarizing the preprocessed data, including visualizing class imbalances and feature types
    
4) Ensemble_Methods.ipynb: notebook for Random Forest, XGBoost, LightGBM, and CatBoost classifiers. Also includes code for training Random Forest and LightGBM models on undersampled training data
    
5) FCNeuralNet.ipynb: notebook for Fully Connected Neural Network classifier
    
6) logReg.ipynb: notebook for baseline (symmetric) and asymmetric logistic regression models. Also includes code for training on undersampled training data.
    
7) SVM.ipynb: notebook for Support Vector Machine classifier. Due to the large number of observations in data, this method could not be used in a timely manner and was therefore removed from the analysis.
    
8) Train_Test_split.ipynb: notebook for 80-20 splitting of the cleaned 2015 dataset into train-test sets and also preparing an undersampled training set.
    
9) Selected_Feature_description: description of 22* selected features and how responses were encoded

Based on the pipeline described in clean_dataset.ipynb, 23 features (besides the output variable) were identified. However, upon closer inspection we realized that one of the features, “_TOTINDA”, was defined by another one, “EXERANY2”, so we removed the former to avoid redundancy

[1] Centers for Disease Control and Prevention. Behavioral Risk Factor Surveillance System. URL: https://www.kaggle.com/cdc/behavioral-risk-factor-surveillance-system.
[2] Alex Teboul. Diabetes Health Indicators Dataset. URL: https://www.kaggle.com/alexteboul/diabetes-health-indicators-dataset.
