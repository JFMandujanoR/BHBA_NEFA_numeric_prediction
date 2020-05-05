# rtFMS Regression Outcome for Blood BHBA

The following picture is a histogram of the root mean square error after running all the options. We have a mean = 0.1763 with sd = 0.0143.

![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/RMSE_BHBA.png)

We used the rtFMS technique to obtain the following tree with 22 terminal nodes:
![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_tree.png)

We have n models per branch. These n models have a similar performance. On the bottom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. 

Then we can select the branch 3, with mean = 0.1587 and sd = 0.0015:

- Variable: IR
- Breed: Breed.No
- Filter: EMR212
- Model: GLMNET

Note 1: The other variables do not appear in these conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

Note 2: The target variable BHBA was transformed using y = log(x) in order to normalize the data. 

The following graph shows a plot of the best model predicted values vs actual values for BHBA. The red line is the identity. We can see that we are underestimating the real value of the high BHBA values.
![bhba](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_0.png)

Tables of variable importance for the 20 models in the best branch:

[importance](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_numeric_tables_importance.csv)

NOTE: 

To download a table click "Raw" button (right up) and then do right click on the text in the screen and select "save as..."
_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/README.md)

