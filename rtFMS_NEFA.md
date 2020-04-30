# rtFMS Detection Outcome for Blood NEFA

The following picture is a histogram of the balanced accuracy after running all the options. We have a mean = 0.7732 with sd = 0.0126

![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Hist_Binary_Bal_Acc_GLMNET_NEFA.png)

We used the rtFMS technique to obtain the following tree with 6 terminal nodes:

![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Tree_Bal_Acc_GLMNET_NEFA.png)

We have n models per branch. These n models have a similar performance. On the bottom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. We then choose the branch with the highest mean balanced accuracy.

Then we can select the branch 5, with mean = 0.7860 and sd = 0.0039:

- Variable: IR
- Filter: EMR212
- Standardization: FD, FD.EMR

Note: The other variables do not appear in these conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/README.md)
