# ai_conference_june_2019
Material for "Using deep learning and time-series forecasting to reduce transit delays" at O'Reilly AI Conference in Beijing, June 2019

## Prequisites
To run the code in this repo you will need access to an environment (such as Paperspace https://www.paperspace.com/ or Watson Studio Cloud https://cloud.ibm.com/catalog/services/watson-studio ) that supports Jupyter notebooks.

## Background

**AICH19_Using_deep_learning_and_time-series_forecasting_to_reduce_transit_delays.pdf** presentation material
**https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#e8f359f0-2f47-3058-bf64-6ec488de52da** original dataset
**https://www.kaggle.com/knowledgegrappler/a-simple-nn-solution-with-keras-0-48611-pl** Kaggle submission that was used as input to creation of the Keras model used in this example

## Intermediate datasets
**2014_2018.pkl** pickled dataframe containing data from the original dataset 2014 to November 2018
**2014_2018_df_cleaned_keep_bad_loc_geocoded_SCtrimmed_apr26.pkl** pickled dataframe with cleanup from streetcar_data_preparation.ipynb applied and latitude and longitude added for Location values (results of calling Geocoding API in streetcar_data_preparation-geocode.ipynb)

## Code
**streetcar_data_preparation.ipynb** load original dataset into a single dataframe and perform basic cleanup on values
**streetcar_data_exploration.ipynb** basic data exploration
**streetcar_time_series.ipynb** additional data exploration using time series forecasting techniques
**streetcar_data_preparation-geocode-public.ipynb** use Google Geocoding API to get latitude and longitude values from Location values. NOTE: to run the code in this file, you will need to get your own API Key from Google Cloud Platform https://developers.google.com/maps/documentation/embed/get-api-key
**streetcar_DL_train-trimmed.ipynb** train Keras deep learning model
