# rtFMS Detection Outcome for Blood NEFA

The following picture is a histogram of the balanced accuracy after running all the options.
![histogram](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Hist_Binary_Bal_Acc_GLMNET_NEFA.jpg)

We used the rtFMS technique to obtain the following tree:
![tree](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/Tree_Binary_Bal_Acc_GLMNET_NEFA.png)

We have n models per branch. These n models have a similar performance. On the botom of the tree we can see box plots centered in the mean balanced accuracy of the n models in the branch. We then choose the branch with the highest mean balanced accuracy.

Then we have two different models with similar performance that we can select:

- Variable: FAF
- Breed: Breed.No
- Time of milk sampling: Milk.Model.Yes

And: 

- Variable: FAF1, FAF2
- Breed: Breed.No
- Time of milk sampling: Milk.Model.Yes

Note: The other variables do not appear in this conclusions because their elections among their options are not significant for the final result. In other words, _it doesn't matter which option we choose_.

In order to compare the different branches of the tree we selected one model per brach and made a _radar graph_ usign sensitivity (__se__), specificity (__sp__), balanced accuracy (__balanced.acc__) and diagnostic accuracy (__diag.acc__):

![comparation of branches here](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/comparing_branches_NEFA.png). 

We say that the best branch of models is the one that reach the highest value in each feature (se, sp, blanced.acc and diag.acc). In this case, we selected the first two branches of models.

We can consult the complete tables of these models here:
![table](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/NEFA_tables.PNG)

[Download Table](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/dat1_NEFA.xlsx)

_________________________________________________________________________________________________________________________________
[QCheck_Prediction_Report](https://github.com/JFMandujanoR/QCheck_Prediction_Report)
