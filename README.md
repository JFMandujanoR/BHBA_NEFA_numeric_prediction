# QCheck_Prediction_Report
Report of prediction model for bNEFA and bBHBA using QCheck data

In this repository we present the outcomes of the Regression Tree Full Model Selection (rtFMS) approach to select the best prediction model in two tasks: to dectect high blood BHBA and NEFA values (detection/classification task), and for to predict a numeric value of those indicators (regression task). We used the QCheck data to test different permutations of possible models, we enlist the different options per task below.

__Detection/Classification Task:__

We run 400 models (per indicator), always using the so called Elastic Net regression, using one the following options:

- Type of Variable (5): FAF, FAF1, FAF2, FAF3, IR
- Use of EMR_standardization (2): EMR.STAND, EMR.NONE
- Type of tandardization (5): Raw, FD, SD, FD.EMR, SD.EMR
- Filter (2): AllWN, EMR212
- Use of Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No

We fit a __regression tree model__ using the metric __balanced accuracy__ as target variable and as regressors the afforementioned _options for the model_. With the following links we can see the results obtained for detecting high blood NEFA and blood BHBA.

- Here we can find the [rtFMS detection outcome for blood NEFA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_NEFA.md)
- Here we can find the [rtFMS detection outcome for blood BHBA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_BHBA.md)

__Regression Task:__

We run 1600 models (per indicator), using one the following options:

- Type of Variable (5): FAF, FAF1, FAF2, FAF3, IR
- Use of EMR_standardization (2): EMR.STAND, EMR.NONE
- Type of tandardization (5): Raw, FD, SD, FD.EMR, SD.EMR
- Filter (2): AllWN, EMR212
- Use of Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No
- Models (4): Elastic Net, Multivariate Adaptative Regression Splines, Principal Componet Regression, Partial Least Squares Regression

We fit a __regression tree model__ using the metric __root mean squared error__ as target variable and as regressors the afforementioned _options for the model_. With the following links we can see the results obtained for predicting blood NEFA and blood BHBA.

- Here we can find the [rtFMS regression outcome for blood NEFA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_NEFA_numeric.md)
- Here we can find the [rtFMS regression outcome for blood BHBA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_BHBA_numeric.md)

__________________________________________________________________________________________________________________________
_Reported by: J. Francisco Mandujano R. (UW-MAdison)_
