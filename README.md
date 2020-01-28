
# Module 4 -  Final Project Specifications

## Introduction

This project focuses on housing data.  A new start-up company, Pretend Houses, is looking to buy properties and rent them out.  As they're a start up company, they don't have much capital but they would like to buy several properties in a zip code to help manage their risk.  It's my goal to recommend the 5 best zip codes for them to invest in.

## Contents

* README.md: This file.  Contains an overview of the project and the github repository.
* mod_4_starter_notebook.ipynb: Contains the code to analyze the data as well as some commentary about what the code is doing.  Also includes some brief explanations about why certain decisions were made.
* mod4project.ppt: Business presentation. Contains an overview of the data analysis as well as my recommendations and potential future work. The audience for this presentation are the business owners and potential investors.
* zillow_data.csv: Data.  This is the raw data from Zillow that my analyses are based on.
* Blog entry: It's not in this repository but here's a link to my blog entry about this project: [blog](https://alvacat.github.io/project_3_housing_price_prediction)
* YouTube code walkthrough:  Also not in this repository, but here's a link to a YouTube video that walks through the code: [walkthrough](https://youtu.be/JbBpDTyJ0tw)

## Notebook Table of Contents
The mod_4_starter_notebook has the following subsections:
* Step 1: Load the Data/Filtering for Chosen Zipcodes
* Step 2: Data Preprocessing
* Step 3: EDA and Visualization
* Step 4: Reshape from Wide to Long Format
* Step 5: ARIMA Modeling
* Step 6: Interpreting Results

### Functions
The following functions are in the Step 1 subsection in the mod_4_starter_notebook
* get_datetimes(): converts values in a row to datetime objects
* make_ts(): makes a time series from the dataframe given a zipcode
* make_ts_small(): makes a time series from a reduced dataframe given a zipcode
* stationarity_check(): determines if a given time series is stationary using the Dickey Fuller test
* melt_data(): converts a dataframe from wide to long format and aggregates the data using the mean values
* melt_data2(): converts a dataframe from wide to long format without aggregating the data
* growth_rate(): calculates the growth rate between Jan 2015 and Jan 2018
* detrend(): detrends a time series using an exponentially weighted mean
* find_arima_paramters(): finds the best ARIMA parameters, assuming a first order model
* fit_arima(): fits an ARIMA model given parameters and uses it to make predictions for the next 3 years
* slope(): finds the slope of the predicted values between Jan 2018 and Jan 2021
* plot_prediction(): creates a plot of the time series, predictions, and confidence intervals