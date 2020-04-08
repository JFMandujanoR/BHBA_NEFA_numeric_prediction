# rtFMS Regression Outcome for Blood NEFA

The following picture is a histogram of the root mean square error after running all the options.
![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Histogram_Numeric_RMSE_GLMNET_NEFA.png)

We used the rtFMS technique to obtain the following tree:
![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Tree_Numeric_RMSE_GLMNET_NEFA.png)

We have n models per branch. These n models have a similar performance. On the botom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. We then choose the branch with the highest mean balanced accuracy.

Then we have one best model that we can select:

- Variable: IR
- Breed: Breed.No
- Filter: EMR212
- Standardization: FD, SD, FD.EMR, SD.EMR

Note 1: The other variables do not appear in this conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

Note 2: The target variable NEFA was transformed using y = log(x) in order to normalize the data. 

_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report)

