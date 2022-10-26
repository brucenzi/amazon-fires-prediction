# amazon-fires-prediction
This README describes work done predicting spot fires in the Amazon forest, as part of the mid-project of the Ironhack Data Analytics Bootcamp. Resources used include Python and associated packages.

[![Amazon](https://i.postimg.cc/wBDLMm6P/Amazon.png)](https://postimg.cc/R3VNbqJQ)

## Introduction

The rate at which the Amazon forest is deforested is a global concern as it plays a key role in the environment and atmosphere. The main goal of this study is to understand some of the main characteristics of the fires in the Amazon and develop a model to predict the amount of spot fires for each main fire to address the problem of fire spreading in the forest.
 
Jupyter notebook: Mid-project_IH_Amazon_fires
Dataset: gfed_1998_2016_w_fire_spots.csv

## Table of contents 	
- General info
- Technologies
- Set up
- Sources
- Credits

## General info

The dataset gathered over 15 years, from 1998 to 2013. It contains 1513059 rows  of data relating to fires in the Amazonas. Information within includes year, month, burned_fraction, source, basis_regions, C, DM, BB, NPP, Rh, grid_cell_area, latitude, longitude, burned_area and fire_spots. All the variables are float64.

The following questions were chosen to guide our analysis: 
- Did the number of fires increase?
- Do carbon emissions correlate with the size of the burned areas?
- What is the capacity of the affected areas to retain Carbon?
- What are the most affected areas and how are they distributed in the Amazon territory?
- How do Amazon fires behave throughout the months of the year?

Approaches to develop the prediction model:
1. Linear Regression to predict the number of spot fires, whose results weren’t good; the model didn’t learn well from the data nor predict the number of fires. 
2. Logistic Regression to predict the presence or not of spot fires following the main fire. The performance was excellent, therefore we decided to explore more spot fires ranges with a third approach. 
3. KNN Model for multi classification to predict different ranges of spot fires, where we divided the number of spot fires in three categories, encoded as 0, 1 and 2, according to the distribution of feature “fire_spots”. We found out that the dataset is highly sensitive for outliers, so after applying the Robust Scaler to deal with outliers, the model performed very well, as shown in the jupyter notebook.

## Technologies 

Project is created with: 
- Python version: 3
- Tableau version: 2002.2.2

## Prediction Model Set up 

EDA and Prediction model were developed using the following Python libraries:
- Pandas
- Numby
- Seaborn
- Matplotlib
- Scipy.stats
- Sklearn
- Math
- Imblearn

## Sources

The database is from Kaggle, called Brazilian Legal amazon fire emissions:
(https://www.kaggle.com/datasets/mateus558/brazilian-legal-amazon-burned-area-dataset?datasetId=1222181)

Direct link for the database in google drive: (https://drive.google.com/drive/folders/1XzCcsPps-TzzP7d2mO5-N08DlFe0myRH?usp=sharing)

## Credits

Adela Sánchez Zarabozo & Bruno Vicenzi
