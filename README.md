# Udacity Capstone Project: Predicting Inventory

## Basic Information

## Implementation
### Pre-Requisites

This project has been built using the **Anaconda** installation of Python 2.7 version 4.1.6, utilisiing the following packages:

+ python 2.7
+ numpy
+ pandas
+ re
+ time
+ sklearn
+ matlpotlib

### File structures

All data files, including engineered files which result from some notebooks have been provided:

+ train.csv (the original input file from grupo bimbo): this is not included in the submission please see later
+ smaller_train.csv (a reduced version created to allow local workstation operation)
+ engineered_train.csv (an engineered version of smaller_train with additional features): this is not included in the submission please see later
+ town_state.csv (a lookup table for agency showing the town and state in mexico where each agent resides)
+ cliente_tabla.csv (a lookup table for client with their name)
+ engineered_cliente_tabla.csv (an engineered version of client which extracts an aggregated version of the name)
+ producto_tabla.csv (a lookup table for product with its name)
+ engineered_producto_tabla.csv (an engineered version of product which extracts a shortened name, weight, pieces and supplier code)

The folder structure is:
home/
	/data
	/code

The project's notebooks can be run independently of each other - except those reliant on train.csv and engineered_train.csv - but a suggested order would be:

+ explore_agency (examines the town_state lookup)
+ explore_product (examines the product look up and creates the engineered version of the file)
+ explore_client (examines the client look up and creates the engineered version of the file)
+ explore_train (analysis of the training data file - please note that various elements of this notebook can take up to 20 mins to run)
+ engineer_smaller_train_file (takes the large train file and creates a smaller version)
+ engineer_features (with the smaller train file, adds lookup features, creates lagged sales data, encodes categorical data)
+ create_model (initial training, testing then tuning of model - please note that the tuning element of modelling with gridSearch takes about 3 hours)

### Missing Data Files
The train.csv file is too large to upload. It can be downloaded from Kaggle at: https://www.kaggle.com/c/grupo-bimbo-inventory-demand/data
Once downloaded it needs to be placed into the /data folder

The engineered_train.csv is also too large for submission. This can be created using engineer_features notebook.