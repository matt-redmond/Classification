Abstract

The goal of this project was to build a model that could predict whether a person's income would be greater than or less $50,000 per year based on demographic information from Census Data.  Multiple models were compared and then tuned to get the best possible predictions.

Design

The design of this project was mostly around working through building and evaluating different models.  The Census Data was readily available through Kaggle although it did need to be cleaned and processed.  The data needed to be fitted to each model and then using an iterative approach, parameters could be optimized.  The output of each version of each model could be compared based on accuracy, precision, recall, and f1 scores.  Then these scores could be compared between models to ultimately choose the best approach.  The final model could be further tuned using a grid and/or randomized search approach.

Data

Data was sourced from Kaggle at https://www.kaggle.com/datasets/uciml/adult-census-income.  The dataset started as 48852 rows of data with a total of 15 columns which were 14 features and the target.  A very small number of rows (10) were deleted because they contained null values.  This was done in the csv file.  The data was scaled only for the K nearest neighbor algorithm.  Dummy columns were created to convert categorical data into 0 and 1's.  This increased the number of features to 108.  For the target, greater or equal to 50K was converted to 1's and less than 50K was converted to 0's.
  
Algorithms

6 Algorithms were tested and after an initial attempt to optimize each algorithm using one parameter.  They ranked as follows
XG Boost F1 score 71%
Random Forest F1 score 69%
Decision Tree F1 score 67%
Extra Trees F1 score 65%
K nearest neigbor F1 score 63%
Logistic Regression F1 score 39%

Then XG Boost was further tuned both using an iterative approach to maximize parameters individually and using a randomized seatch approach using 7 parameters(learning_rate, n_estimators, min_child_weight, gamma, subsample, max_depth, and scale_pos_weight).  Each of these 2 approaches increased the F1 score by only 0.4% for the individual approach and 0.7% for the randomized search approach.  

Tools

Tools used included pandas, scikit-learn, XGBoost, matplotlib, and seaborn.  Almost all of the work for this project was done in python jupyter notebooks.  The data itself was downloaded manually through the kaggle website.


Communication

Slides and visuals presented included data and the pre-processing as well as the scores of the different models.  Confusion matrixes are in the appendix.  There are also 2 plots of accuracy vs f1, recall, and precision in the appendix.



