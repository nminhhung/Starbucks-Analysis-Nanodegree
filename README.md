# Starbucks Analysis Nanodegree Capstone Project
This project is a part of Udacity Data Science Nanodegree.
My Medium blogspot: [Data Scientist Nanodegree Capstone — Starbucks Project](https://medium.com/@nguynminhhng/data-scientist-nanodegree-capstone-starbucks-project-f38e00ef022e)

## Table of content
1. [Project Overview](https://github.com/nminhhung/Starbucks-Analysis-Nanodegree/blob/main/README.md#1-project-overview)
2. [Project Components](https://github.com/nminhhung/Starbucks-Analysis-Nanodegree/blob/main/README.md#2-project-components)
3. [Installation](https://github.com/nminhhung/Starbucks-Analysis-Nanodegree/blob/main/README.md#3-installation)
4. [File Descriptions](https://github.com/nminhhung/Starbucks-Analysis-Nanodegree/blob/main/README.md#4-file-descriptions)
5. [Instructions](https://github.com/nminhhung/Starbucks-Analysis-Nanodegree/blob/main/README.md#5-instructions)
6. [Credits and Acknowledgements](https://github.com/nminhhung/Starbucks-Analysis-Nanodegree/blob/main/README.md#6-credits-and-acknowledgements)

## 1. Project Overview
Starbucks data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer, and that is the challenge to solve with this data set.
The task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.

## 2. Project Components
The way I approach and handle the problem is that I divide it into 3 main parts:
- Data Preprocessing:
  - Reading and cleaning the given datasets.
  - Overviewing the data.
  - Combining datasets to get a final clean data.
- Data Exploration:
  - Performing EDA to the final dataset to get the inportant infomation.
  - Visualization the data.
- Data Modeling:
  - Split data into train and test data then scaling the features.
  - Choose some reasonable machine learning models to handle the problem.
  - Select the best model, then tune it with GridSearchCV.
  - Calculate features importance.
  - Compare the effectiveness between models and conclude.
  
## 3. Installation
- The code using Python 3 and Jupyter Notebook.
- Data Processing: Pandas, Numpy.
- Data Visualization: Matplotlib, Seaborn, Plotly.
- Machine Learning Libraries: SciPy, Scikit-Learn, XGBoost

## 4. File Descriptions
-- data/
    -- data.csv: final data file after preprocessing and combining 3 data files into 1. Because the file size is too large (34.75 MB), I stored the file on Kaggle. [data.csv](https://www.kaggle.com/datasets/scvgyahoo/starbucks-udacity-project-dataset?select=data.csv).
    -- portfolio.json: containing offer ids and meta data about each offer.
    -- profile.json: demographic data for each customer.
    -- transcript.json: records for transactions, offers received, offers viewed, and offers completed. Because the file size is too large (40.24 MB), I stored the file on Kaggle. [transcript.json](https://www.kaggle.com/datasets/scvgyahoo/starbucks-udacity-project-dataset?select=transcript.json).
-- 1_Preprocessing.ipynb: performs data preprocessing steps and combines them into a final dataset.
-- 2_Data_Exploration.ipynb: perform data EDA and data visualization steps.
-- 3_Data_Modeling.ipynb: perform the steps to build the model and evaluate the model and results.

Here is the schema and explanation of each variable in the files:

portfolio.json
- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

profile.json
- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

transcript.json
- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

## 5. Instructions
- The entire anlaysis is contained in 3 jupyter notebook files. Each file do a step.
- All 3 json files should be located in data folder and the same for final data 'data.csv' file.

## 6. Credits and Acknowledgements
- This project was completed as part of the [Udacity](https://udacity.com) Data Science Nanodegree.
- Special thanks to [Starbucks](https://www.starbucks.com/) and Udacity for providing the data utilized in this project.
