Koala Kubs Diabetes Classification

This folder contains all the data and notebooks used in the CIS520 final project for team Koala Kubs (Seung-Hyun Ko, Kshitiz Parihar, Yi Qi). In this project, using responses to the CDC's Behavioral Risk Factor Surveillance System (BRFSS) from 2011-2015, we optimize and compare several binary classification models’ performance in accurately predicting diabetic status using a curated set of questions from the survey. Below is a summary of each file you will find in this folder:

    • dataset: contains 20**.csv files for raw data from Kaggle for 2011-2015 and folder for our pre-processed data
        ◦ pre_processed: contains 20**_selected.csv files of our preprocessed data with select features* from BRFSS’s original dataset for 2011-2015. Also includes the 2015 training, undersampled training, and test sets (Train.csv, Train_undersample.csv, Test.csv)
    • clean_dataset.ipynb: notebook for preprocessing and cleaning the raw data from Kaggle
    • comparison_across_years.ipynb: notebook for assessing and comparing LightGBM model’s (best classification model on the test set) performance on cleaned dataset of different yeast, and feature importance across years using SHAPley values
    • Data_Exploration.ipynb: notebook for summarizing the preprocessed data, including visualizing class imbalances and feature types
    • Ensemble_Methods.ipynb: notebook for Random Forest, XGBoost, LightGBM, and CatBoost classifiers. Also includes code for training Random Forest and LightGBM models on undersampled training data
    • FCNeuralNet.ipynb: notebook for Fully Connected Neural Network classifier
    • logReg.ipynb: notebook for baseline (symmetric) and asymmetric logistic regression models. Also includes code for training on undersampled training data.
    • SVM.ipynb: notebook for Support Vector Machine classifier. Due to the large number of observations in data, this method could not be used in a timely manner and was therefore removed from the analysis.
    • Train_Test_split.ipynb: notebook for 80-20 splitting of the cleaned 2015 dataset into train-test sets and also preparing an undersampled training set.
    • Selected_Feature_description: description of 22* selected features and how responses were encoded
* Based on the pipeline described in clean_dataset.ipynb, 23 features (besides the output variable) were identified. However, upon closer inspection we realized that one of the features, “_TOTINDA”, was defined by another one, “EXERANY2”, so we removed the former to avoid redundancy
