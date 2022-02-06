# Technical Test

## Procedure

This is supervised learning problem with binary classification for the insurance
industry. I use AUC as the performance metric as accuracy does not take into
account directly the False Negatives, which are essential in the insurance
sector.

## My methodology

* 1-Preanalysis.ipynb is a notebook where I analyze the different covariables,
change their type if necessary, and I also perform imputation. 
* 2-Exploratory-Descriptive-Statistics.ipynb I evaluate the predictive power
of each variable using non-parametric statistics. After I use PCA to combine two
correlated numerical variables. I reduce the number of cavariables from 34 to 15
because of their lack of predicting power
* 3-BaselineLinearModel.ipynb use Logistic Regression as a Linear Model, it is 
use gridsearch to find the best hyperparameters and there is a great difference
in the performance between training and testing set. It is required stronger
regularization
* 4-SelectedModel.ipynb Use xgboost to improve the performance of the binary
classification. It is use k-fold to find the best hyperparameters. Finally, this
model is used to calculate the answeres for 'train_auto.csv'