# data_exploration_and_mining
Case Study 1: Association mining to find hotspots based on a Patient Route 
Data 
During the initial outbreak of COVID19 in South Korea, the routes travelled by COVID19 
positive patients were reported. The “PatientRoute” dataset consists of 1509 observations where 
each observation presents a positive patient’s visit at a location and the date. There is a total of 
891 unique patients and 151 unique locations in this subset of data. More details about the full 
dataset can be found on the Kaggle website1
. The table below details the attributes in the dataset 
‘D1.csv’. 
Attribute Description Data type
patient_id Unique identifier of the positive patient ID
global_num Unique identifier of the positive patient given by the 
Korea Centers for Disease Control and Prevention
ID
location Location of the patient’s visit. It is a combination of 
province and city. For example, if ‘Seoul’ is the 
province and ‘Jung-gu’ is the city, the location will 
be recorded as ‘Seoul_Jung-gu’
String
date Date of patient’s visit at the location Datetime
latitude Latitude coordinate of the location Numeric
longitude Longitude coordinate of the location Numeric
 
Tasks
Analyze the dataset 'D1.csv' using Association mining, where each patient's route is considered 
a transaction, to identify the frequently travelled routes of COVID19 positive patients. The task
is to build an association mining model on the given dataset and answer the subsequent 
questions based on the data and analysis.
1. What pre-processing was required on the dataset before building the association mining 
model? What variables did you include in the analysis? Justify your choice.
2. Conduct association mining and answer the following:
a. What ‘min_support’ and `min_confidence’ thresholds were set for this mining 
exercise? Rationalize why these values were chosen. 
b. Report the top-5 (interesting) rules and interpret them.
3. List four most interesting routes taken by individuals who have tested positive for 
COVID19 and have travelled from Buk-gu City in Busan Province. 
4. Can you perform sequence analysis on this dataset? If yes, present your results. If not, 
rationalize why.
5. In what ways can the results of this task be utilized by the relevant decision-makers?
1
 https://www.kaggle.com/kimjihoo/coronavirusdataset#PatientRoute.csv
Case Study 2: Clustering COVID19 data 
For Assessment 1, you were given a subset of COVID19 dataset that consisted of responses 
from 6110 individuals, including demographic, behaviour, segmentation, and health condition
values. This dataset was pre-processed to remove some data errors and variables, resulting in 
the D2.csv dataset. Your task is to perform clustering on D2.csv and explain the least number 
of useful clusters discovered. 
The description of the D2.csv dataset is as follows:
No Column name Description 
1 Gender Male, Female or other 
2 Age Age quantile 
3 Height Height of the person in cm 
4 Weight Weight of the person in cm 
5 Blood_type Type of the person’s blood 
6 Insurance If the person has insurance or not? 
7 Income Type of income. For example, low, medium, high, or gov 
8 Race Race of the person 
9 Immigrant If the person is immigrant or not? 
10 Smoking Information on how often the person smokes 
11 Alcohol Level of alcohol
12 Contacts_count Number of people the person has contacted 
13 House_count Number of people living in the person’s house 
14 Working Status of the person’s work 
15 Worried On a scale of 1 to 5 indicating how much worried is the person.
16 Covid19 positive 1 and 0 stating the existence or not 
Tasks
Suppose you are interested in understanding the clusters of responses who stated COVID 
positive based on the variables containing numerical data. The task is to perform clustering
and answer the subsequent questions based on the data and analysis. (add screenshots as 
appropriate) 
1. What pre-processing was required on the dataset (D2.csv) before building the clustering 
model and why? 
2. Build a clustering model to profile the characteristics of COVID positive individuals. 
Answer the followings: 
a. What clustering algorithm have you used and why? 
b. List the attributes used in this analysis.
c. What is the optimal number of clusters identified? How did you reach this 
optimal number?
d. Did you normalize/standardize the variables? What was its effect on the model – 
Does the variable normalization/standardization process enable a better clustering 
solution? 
3. For the model with the optimal number of clusters, answer the following.
a. Visualize the clusters using ‘pairplot’ and interpret the visualization.
b. Characterize the nature of each cluster by giving it a descriptive label and a brief 
description. Hint: use cluster distribution.
4. Now, build another clustering model by including the variable ‘Age’.
Use the best setting (e.g., variable standardisation, optimal K, etc) obtained in the 
previous models. Answer the followings:
a. What clustering algorithm have you used and why?
b. List the attributes used in this analysis.
c. What difference do you see in this clustering interpretation when compared to the 
previous one (task 3)?
5. In what ways can the results of this task be utilized by the relevant decision-makers?
Case Study 3: Building and Evaluating Predictive Models
You are required to utilize the COVID19 dataset (D2.csv), as in Case Study 2, for predictive 
modelling with various techniques. The objective is to classify whether an individual will test 
positive for COVID-19 (indicated as 1) or negative (indicated as 0) based on past observations.
Tasks
You are required to build different predictive models, such as decision trees, regression models, 
and neural networks, for this data set and compare their performances. The task is to perform 
classification mining and address the following questions based on the data and analysis. (add 
screenshots as appropriate)
Predictive modelling using Decision Tree
1. What pre-processing was required on the dataset (D2.csv) before decision tree 
modelling? What distribution split between training and test datasets was used? 
2. Build a decision tree using the default setting. Answer the followings: 
a. What is the classification accuracy of training and test datasets?
b. What is the size of the tree (number of nodes and rules)?
c. Which variable is used for the first split?
d. What are the 5 important variables (in the order) in building the tree?
e. What parameters have been used in building the tree? Detail them.
3. Build another decision tree tuned with GridSearchCV. Answer the followings: 
a. What is the classification accuracy of training and test datasets?
b. What is the size of the tree (i.e. the number of nodes and rules)?
c. Which variable is used for the first split?
d. What are the 5 important variables (in the order) in building the tree?
e. Report if you see any evidence of model overfitting.
4. What differences do you observe between these two decision tree models (with and 
without fine-tuning)? How do they compare performance-wise? Produce the ROC 
curve for both DTs. Explain why those changes may have happened.
5. Using the better model, can you identify which individuals could potentially be 
"COVID positive"? Can you provide the general characteristics of those individuals? 
Predictive modelling using Regression
1. What pre-processing was required on the dataset before regression modelling? What 
distribution split between training and test datasets was used? 
2. Build a regression model using the default regression method with all inputs. Build 
another regression model tuned with GridSearchCV. Now, choose a better model to 
answer the followings:
a. Explain why you chose that model.
b. Name the regression function used.
c. Did you apply standardisation of variables? Why would you standardise the 
variables for regression mining?
d. Report the variables included in the regression model.
e. Report the top-5 important variables (in the order) in the model.
f. What is the classification accuracy on training and test datasets?
g. Report any sign of overfitting in this model.
3. Build another regression model on the reduced variables set. Perform dimensionality
reduction with Recursive feature elimination. Tune the model with GridSearchCV to 
find the best parameter setting. Answer the followings:
a. Was dimensionality reduction useful to identify a good feature set for building an
accurate model?
b. What is the classification accuracy on training and test datasets?
c. Report any sign of overfitting.
d. Report the top-3 important variables (in the order) in the model.
4. Produce the ROC curve for all different regression models. Using the best regression 
model, can you identify which individuals could potentially be "COVID positive"? 
Can you provide the general characteristics of those individuals?
Predictive modelling using Neural Networks
1. What pre-processing was required on the dataset before neural network modelling? 
What distribution split between training and test datasets was used?
2. Build a Neural Network model using the default setting. Answer the following:
a. Explain the parameters used in building this model, e.g., network
architecture, iterations, activation function, etc.
b. What is the classification accuracy on training and test datasets?
c. Did the training process converge and result in the best model?
3. Refine this network by tuning it with GridSearchCV. Report the trained model.
a. Explain the parameters used in building this model, e.g., network
architecture, iterations, activation function, etc.
b. What is the classification accuracy on training and test datasets?
c. Did the training process converge and result in the best model?
d. Do you see any sign of over-fitting?
4. Let us see if feature selection helps in improving the model. Build another Neural 
Network model with a reduced feature set. Perform dimensionality reduction by 
selecting variables with a decision tree (use the best decision tree model that you have
built in the previous modelling task). Tune the model with GridSearchCV to find the 
best parameter setting. Answer the followings:
a. Did feature selection favour the outcome? Any change in network 
architecture? What inputs are being used as the network input?
b. What is the classification accuracy of training and test datasets?
c. How many iterations are now needed to train this network?
d. Do you see any sign of over-fitting? Did the training process converge and 
result in the best model?
5. Produce the ROC curve for all different NNs. Now, using the best neural network 
model, can you provide characteristics of the individuals identified as COVID positive
by the model? If it is difficult (or even infeasible) to comprehend, discuss why.
Final remarks: Decision making
1. Finally, based on all models and analysis, is there a model you will use in decisionmaking? Justify your choice. Draw a ROC chart and accuracy table to support your 
findings.
2. Can you summarise the positives and negatives of each predictive modelling method 
based on this analysis?
