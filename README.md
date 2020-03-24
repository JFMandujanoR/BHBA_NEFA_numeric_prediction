# QCheck_Prediction_Report
Report of prediction model for bNEFA and bBHBA using QCheck data

In this repository we present the outcomes of the Regression Tree Full Model Selection (rfFMS) approach to select the best model to predict a binary outcome to dectect high blood BHBA and NEFA values. We used the QCheck data to test different combinations of possible models:

We ran 400 permutations of models, always using the so called Elastic Net regression, using these options for the model:

- Variable (5): FAF, FAF1, FAF2, FAF3, IR
- EMR_standardization (2): EMR.STAND, EMR.NONE
- Standardization (5): Raw, FD, SD, FD.EMR, SD.EMR
- Filter (2): AllWN, EMR212
- Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No

We fit a __regression tree model__ using the metric __balanced accuracy__ as target variable and as regressors the afforementioned _options for the model_. With the following links we can see regression tree graphs and histograms of balanced accuracy

- Here we can find the [rtFMS outcome for blood NEFA in dairy cows]()
- Here we can find the [rtFMS outcome for blood BHBA in dairy cows]()




__________________________________________________________________________________________________________________________
_Reported by: J. Francisco Mandujano R. (UW-MAdison)_
