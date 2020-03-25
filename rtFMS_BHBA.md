# rtFMS Outcome for BHBA

Here we can find a [histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Hist_Binary_Bal_Acc_GLMNET_BHBA.png) of balanced accuracy after running all the options.

This [tree graph](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Tree_Binary_Bal_Acc_GLMNET_BHBA.png) shows us that the we have two best models with similar permance:

- Variable: IR
- Either of Standardization: FD, SD, FD.EMR, SD.EMR
- EMR_standardization: EMR.STAND

And: 

- Variable: IR
- Either of Standardization: FD, SD, FD.EMR, SD.EMR
- EMR_standardization: EMR.NONE

Note: The other variables do not appear in this conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

In order to compare the different branches of the tree we selected one model per brach and made a _radar graph_ usign sensitivity (__se__), specificity (__sp__), balanced accuracy (__balanced.acc__) and diagnostic accuracy (__diag.acc__). We can see this [comparation of branches here](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/comparing_branches_BHBA.png). 

We can consult the complete [tables of these models here](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/dat1_BHBA.xls).

_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report)
