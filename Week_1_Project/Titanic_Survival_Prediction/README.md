\# Titanic Survival Prediction



This folder contains the first weekly project of my Machine Learning \& AI internship at Skill Nexis. The objective of this project is to clean, explore, and build a machine learning model that predicts passenger survival rates using the classic Titanic dataset.



\# Project Structure



* 'Model/': Contains the final and fully trained model.
* 'data/': Contains the original raw dataset ('Titanic\_Dataset.csv'), the generated clean splits ('X\_train\_clean.csv', etc.).
* 'notebooks/data\_cleaning\_preprocessing.ipynb': Handles feature engineering (extracting titles from names), missing value imputation, and train-test splitting.
* 'notebooks/model\_training\_and\_evaluation.ipynb': Loads the preprocessed data, optimizes classification thresholds via the ROC curve, and tracks evaluation benchmarks.



\# Workflow \& Methodology



1\. Data Cleaning \& Feature Engineering

* Title Extraction: Parsed titles (Mr., Mrs., Miss., Master.) from the passenger name column to perform targeted age imputation and preserve social dynamics.
* Data Partitions: Split the raw dataset into training and validation folds prior to cleaning to guarantee zero data leakage.
* Transformation Pipeline: Handled categorical encoding and missing value replacements cleanly across train and test states.



2\. Model Optimization via ROC Curve



Instead of using a default '0.5' decision cutoff, we computed the True Positive Rate (TPR) and False Positive Rate (FPR) across all thresholds. We selected the optimal cutoff using the Youden's J-Statistics to strike a clean balance between sensitivity and specificity.



\# Final Model Performance Metrics



By deploying our optimized classification threshold against the validation partition, the system achieved the following performance metrics:



* Validation Accuracy: 83.80%
* Precision Score: 79.22%
* Recall Score: 82.43%
* F1 Score: 80.79%
* AUC Score: 0.8925



Note: The final, fully trained model state has been successfully serialized and exported as 'titanic\_survival\_model.pkl' inside the Model directory for future live inference tasks.



