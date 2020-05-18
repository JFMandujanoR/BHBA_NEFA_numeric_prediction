# QCheck_Prediction_Report
Report of prediction model for bNEFA and bBHBA using QCheck data

In this repository we present the outcomes of the Regression Tree Full Model Selection (rtFMS) approach to select the best prediction model in two tasks: to dectect high blood BHBA and NEFA values (detection/classification task), and to predict a numeric value of those indicators (regression task). We used the QCheck data to test different permutations of possible models, we list the different options per task below. The data set consists in 9660 data points. Our predictive models will always consider the information available for the cow: days in milk, lactation number and daily milk yield.

__Detection/Classification Task:__

We run 96 models (per indicator), always using the so called Elastic Net regression, using one of the following options:

- Type of Variable (5): FAF, FAF1, FAF2, FAF3, IR
- Use of EMR_standardization (2): EMR.STAND, EMR.NONE (only for IR)
- Type of Standardization (5): Raw, FD, SD, FD.EMR, SD.EMR (only for IR)
- Filter (2): AllWN, EMR212 (only for IR)
- Use of Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No

We fit a __regression tree model__ using the metric __balanced accuracy__ as target variable and as regressors the afforementioned _options for the model_. With the following links we can see the results obtained for detecting high blood NEFA and blood BHBA.

- Here we can find the [rtFMS detection outcome for blood NEFA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_NEFA.md)
- Here we can find the [rtFMS detection outcome for blood BHBA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_BHBA.md)

__Regression Task:__

We run 384 models (per indicator), using the four different algorithms of regression and one of the following options:

- Type of Variable (5): FAF, FAF1, FAF2, FAF3, IR
- Use of EMR_standardization (2): EMR.STAND, EMR.NONE (only for IR)
- Type of Standardization (5): Raw, FD, SD, FD.EMR, SD.EMR (only for IR)
- Filter (2): AllWN, EMR212 (only for IR)
- Use of Breed (2): Breed.Yes, Breed.No
- Time of milk sampling (2): Milk.Model.Yes, Milk.Model.No
- Algorithms (4): PLSRegression, PCRegression, Elastic Net and MARS

We fit a __regression tree model__ using the metric __root mean squared error__ as target variable and as regressors the aforementioned _options for the model_. With the following links we can see the results obtained for predicting blood NEFA and blood BHBA.

- Here we can find the [rtFMS regression outcome for blood NEFA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_NEFA_numeric.md)
- Here we can find the [rtFMS regression outcome for blood BHBA in dairy cows](https://github.com/JFMandujanoR/QCheck_Prediction_Report/blob/master/rtFMS_BHBA_numeric.md)
__________________________________________________________________________________________________________________________
NOTE: 

Regarding complete tables with metric results from each model please email me (mandujanorey@wisc.edu) asking for a specific model following the nomenclature above. Please specify the task and indicator. For example:

_Model IR, EMR.NONE, Raw, AllWN, Breed.Yes, Milk.Model.Yes for Detection/Classification Task NEFA_

Or, if you wish I can send a complete branch of a regression tree (in the links above) asking for a number of branch. For example:

_Branch 2 for Detection/Classification Task NEFA_
__________________________________________________________________________________________________________________________
_Reported by: J. Francisco Mandujano R. (UW-MAdison)_

_mandujanorey@wisc.edu_
