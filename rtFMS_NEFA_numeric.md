# rtFMS Regression Outcome for Blood NEFA

The following picture is a histogram of the root mean square error after running all the options.We have a mean = 0.6972 with sd = 0.1001.

![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/RMSE_NEFA.png)

We used the rtFMS technique to obtain the following tree with 21 terminal nodes:

![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/NEFA_tree.png)

We have n models per branch. These n models have a similar performance. On the bottom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. 

Then we can select the branch 3, with mean = 0.6121 and sd = 0.0053:

- Variable: IR
- Breed: Breed.No
- Filter: EMR212
- Standardization: FD, SD, FD.EMR, SD.EMR
- Model: GLMNET, MARS

Note 1: The other variables do not appear in these conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

Note 2: The target variable NEFA was transformed using y = log(x) in order to normalize the data. 

The following graph shows a plot of the best model (GLMNET) predicted values vs actual values for NEFA. The red line is the identity. We can see that we are overestimating the real value of the high NEFA values.
![nefa](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/NEFA.png)
_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/README.md)

