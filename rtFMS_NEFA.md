# rtFMS Detection Outcome for Blood NEFA

The following picture is a histogram of the balanced accuracy after running all the options. We have a mean = 0.77 with sd = 0.01

![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Hist_Binary_Bal_Acc_GLMNET_NEFA2.png)

We used the rtFMS technique to obtain the following tree with 7 terminal nodes:

![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Tree_Bal_Acc_GLMNET_NEFA2.png)

We have n models per branch. These n models have a similar performance. On the bottom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. We then choose the branch with the highest mean balanced accuracy.

Then we can select the branch 6, from left to right, with mean = 0.7860 and sd = 0.0039:

- Variable: IR
- Filter: EMR212
- Standardization: FD, FD.EMR

Top 5 branches: 6,1,3,7,5

Note: The other variables do not appear in these conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

Tables of variable importance for the 16 models in the best branch:

[importance](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/NEFA_binary_tables_importance.csv)

Tables of performance for the 16 models in the best branch: 

[performance](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/NEFA_binary_tables_performance.csv)

NOTE: 

To download a table click "Raw" button (right up) and then do right click on the text in the screen and select "save as..."

In the following tables we can see a comparison among the different types of variables (FAF, FAF1, FAF2, FAF3, IR, IR with stand):

![tab_nefa](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/NEFA_binary_tablas.png)

In yellow we can see the best model which also belongs to the best branch in the rtFMS.

[download here](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Total_NEFA.xlsx)

_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/README.md)
