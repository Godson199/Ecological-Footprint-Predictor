# Ecological-Footprint-Predictor 

### Description
In this project, I worked on a classification problem using an imbalanced dataset which predicts ecological footprints.
The aim of the project was not necessarily to build a classification model but to investigate the different methods of correcting an imbalanced dataset in order not to build a biased classifier.

### Data Sources and Description
The data set used for this project was gotten from the 
[University of Carlifornia (UCI) machine learning repository](https://archive.ics.uci.edu/ml/machine-learning-database/00374)


### Exploratory Data Analysis
The statistical overview of the dataset was properly investigated using the pandas-profiling report, pandas correlation method (corr()) cum matplotlib's heatmap.
The EDA reaveals that most of the features were strongly correlated and there was no missing values in the dataset.
The dataset was also described to give a statistical summary such as the mean, percentiles, minimum and maximum values (this reveals the range of the data for outlier detection).

### Data Preprocessing
For the data preprocessing, I used three different techniques , namely: Under sampling, Over sampling with replacement and SMOTE technique from imblearn. The preprocessing of the data is at the heart of the project. 
For undersampling tecnique, the majority instances were reduced to a very close number with the minority classes. while in the oversampling tecnique with replacement, I increased the minority class to meet the number of the majority class each time taking an instace from a class and replacing it before picking another.
The SMOTE tecnique as provided by imblearn (A project that is formerly part of scikit-learn) is an acronymn for Synthetic Minority Oversampling Technique. The difference between this method and the oversampling with replacement is that synthetic data was generated for the minority class while in the former the original data was repeated.

### Modelling 
In the modelling aspect of this project, I used a voting classification method which consists of three different models ie XGBOOST, Logistic Regression and LGBM.
The different models were stacked to form a single model (the models learning from each other)


### Conclusion
The classification report as a method of evaluation shows the most effective method as can be seen in the source code.
This may arguably be problem specific and each method should be explored for every problem before decision making as the saying goes: There's no free lauch.
