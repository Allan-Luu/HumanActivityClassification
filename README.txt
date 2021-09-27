==========================================================================================
# Human Activity Classification
# Brainstation Final Capstone
# By: Allan Luu
# Completed: 09/27/2021
==========================================================================================

BACKGROUND 

==========================================================================================
This analysis was conducted on the dataset found on the UCI Machine Learning Repository at this link: 

http://archive.ics.uci.edu/ml/datasets/Smartphone-Based+Recognition+of+Human+Activities+and+Postural+Transitions

The dataset contains experiments with 30 participants from the ages of 19 to 48 years of age, performing 6 different activities. There were 3 static postures, which were standing, sitting and laying down and 3 dynamic movements, which were walking, walking up-stairs and walking down-stairs.

The data was collected through accelerometer and gyroscope sensors of a Samsung Galaxy S II smartphone, captured at a 50Hz frequency rate and measuring the XYZ linear acceleration and XYZ angular velocity.

A video on how the participants performed the activities and phone placement during the activities can be found at this link:

https://www.youtube.com/watch?v=XOEN9W05_4A&ab_channel=JorgeLuisReyesOrtiz

Within the dataset there were two sections, the raw data and the cleaned/split data. The bulk of the analysis was conducted on the cleaned/split data, and there are plans to perform feature engineering on raw data to create ML models to load into a Flask Web App.
==========================================================================================

PROJECT NOTES:
The web app is still in development, I attached them for reference in the future. The analysis is conducted mainly on the first 3 notebooks, the notebooks 4/5/6 are just for fun and bonus points during demo day. I'll be completing the web app soon.

==========================================================================================

FILES AND FOLDER STRUCTURES

==========================================================================================
This section is going to explain the files within the zipped submission and a brief description of each file.

********************************************
*********** Main Folder - Files: ***********
********************************************

- "01 Basic_EDA.ipynb"
Jupyter Notebook that contains initial EDA on clean data, with some analysis of the data using some dimensionality reduction and aggregations.

- "02 Linear Models.ipynb"
Jupyter Notebook that contains machine learning pipeline for linear classification models such as DT, SVM, KNN and LogReg. Used GridSearchCV to find combination for model and evaluated that model.

- "03 Neural Networks.ipynb"
Jupyter Notebook that contains dense NN and RNN model execution on cleaned data with model evaluations.

- "04 WebApp.ipynb"
Jupyter Notebook that contains initial raw data organization and cleaning to future model training for web application.

- "05 WebApp.ipynb"
Jupyter Notebook that contains feature engineering on raw data, was conducted in google colab to enhance efficiency.

- "06 Data Collection.ipynb"
Jupyter notebook that contains cleaning of data collected through personal smartphone, with some analysis on the data run through the models.

- "conda_evnironment.txt"
Text file explaining how the anaconda environment was set up in the Mac terminal

*******************************************
********* Main Folder - Folders: **********
*******************************************

- "Data"
Contains all data that was provided, collected and created during project

- "Documents"
Contains reports and powerpoint for project submission

- "Flask"
Contains all files associated with the web app development ###INCOMPLETE###

- "Models"
Contains .pkl files of exported machine learning models.

******************************************
********* Data Folder - Files: ***********
******************************************

- "activity_labels.txt"
List that explains what the activity class numbers mean

- "data.csv"
Csv export from "04 WebApp.ipynb", contains raw data transformed to train ML models

- "features_info.txt"
Explanation of how the raw data was modified to create the cleaned data

- "features.txt"
Original list of all the features

- "features2.txt"
Modified version of "features.txt" to replace duplicate column names

- "README.txt"
Data source's read me file

********************************************
********* Data Folder - Folders: ***********
********************************************

- "collected"
Contains files of data collected from personal smartphone

- "RawData"
Contains all raw data files from different users and experiments and activity labels

- "Test"
Contains data that was feature engineered and cleaned from raw data, split into test files and user information

- "Train"
Contains data that was feature engineered and cleaned from raw data, split into train files and user information

********************************************************
********* Data SubFolder - RawData - Files: ************
********************************************************

- "acc_exp##_user##.txt"
Contains accelerometer data from experiment ## and user ##

- "gyro_exp##_user##.txt"
Contains gyroscope data from experiment ## and user ##

- "labels.txt"
Contains information on how to label rows of experiment data, with activity numbers, start/end rows and user/experiment numbers

********************************************
********* models Folder - Files: ***********
********************************************

- "logit.pkl"
Logistic Regression model trained on raw data with lagged rows as feature engineered columns

********************************************
********* Flask Folder - Files: ************
********************************************

- "app.py"
Main python file that runs Flask Web App

**********************************************
********* Flask Folder - Folders: ************
**********************************************

- "__pycache__"
Contains Python 3 bytecode compiled and ready to be executed

- "templates"
Contains html template files for webpages run in flask

***********************************************************
********* Flask SubFolder - Templates - Files: ************
***********************************************************

- "data.html"
Html template for the data webpage, after csv is submitted

- "index.html" 
Html template for main webpage

- "styles.css"
CSS file that holds styling for html templates


==========================================================================================

REFERENCES

==========================================================================================

FLASK:

- CSV upload button: https://www.youtube.com/watch?v=tJKHrLzcopo&ab_channel=1BestCsharpblog
- plotly graph: https://www.youtube.com/watch?v=qNF1HqBvpGE&ab_channel=GregHogg
- example ML web app: https://www.youtube.com/watch?v=Pc8WdnIdXZg&ab_channel=NachiketaHebbar

Workflow: https://www.analyticsinsight.net/human-activity-prediction-using-machine-learning/
# This article was the foundation of how I knew where to start, only used as reference

