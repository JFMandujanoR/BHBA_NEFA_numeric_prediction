# rtFMS Outcome for BHBA

The following picture is a histogram of the balanced accuracy after running all the options. We have a mean = 0.7777 with sd = 0.0231.

![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Hist_Binary_Bal_Acc_GLMNET_BHBA.png)

We used the rtFMS technique to obtain the following tree with 5 terminal nodes:
![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Tree_Bal_Acc_GLMNET_BHBA.png)

We have n models per branch. These n models have a similar performance. On the bottom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. We then choose the branch with the highest mean balanced accuracy.

Then we can select the branch 2, from left to right, with mean = 0.7919 and sd = 0.0072:

- Variable: IR
- Either of Standardization: FD, SD, FD.EMR, SD.EMR
- EMR_standardization: EMR.STAND

Top 5 branches: 2,1,4,3,5

Note: The other variables do not appear in these conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

Tables of variable importance for the 32 models in the best branch:

[importance](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_binary_tables_importance.csv)

Tables of performance for the 32 models in the best branch: 

[performance](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_binary_tables_performance.csv)

_For Branch 1:_

Tables of variable importance for the 32 models in the first branch:

[importance_B1](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_binary_tables_importance_B1.csv)

Tables of performance for the 32 models in the best branch: 

[performance_B1](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_binary_tables_performance_B1.csv)


NOTE: 

To download a table click "Raw" button (right up) and then do right click on the text in the screen and select "save as..."

In the following tables we can see a comparison among the different types of variables (FAF, FAF1, FAF2, FAF3, IR, IR with stand):

![tab_nefa](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/BHBA_binary_tablas.png)

In yellow we can see the best model which also belongs to the best branch in the rtFMS.

[download here](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Total_BHBA.xlsx)
_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/README.md)
