# QCheck_Prediction_Report
Report of prediction model for bNEFA and bBHBA using QCheck data

In this repository we present the outcomes of the Regression Tree Full Model Selection (rtFMS) approach to select the best model to predict a binary outcome to dectect high blood BHBA and NEFA values. We used the QCheck data to test different permutations of possible models:

We run 400 models, always using the so called Elastic Net regression, using one the following options:

- Type of Variable (5): FAF, FAF1, FAF2, FAF3, IR
- Use of EMR_standardization (2): EMR.STAND, EMR.NONE
- Type of tandardization (5): Raw, FD, SD, FD.EMR, SD.EMR
- Filter (2): AllWN, EMR212
- Use of Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No

We fit a __regression tree model__ using the metric __balanced accuracy__ as target variable and as regressors the afforementioned _options for the model_. With the following links we can see the results obtained for predictiong blood NEFA and blood BHBA.

- Here we can find the [rtFMS outcome for blood NEFA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_NEFA.md)
- Here we can find the [rtFMS outcome for blood BHBA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_BHBA.md)




__________________________________________________________________________________________________________________________
_Reported by: J. Francisco Mandujano R. (UW-MAdison)_
