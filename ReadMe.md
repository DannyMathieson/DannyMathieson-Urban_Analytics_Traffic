# **Vision Zero 2.0: Classifying Traffic Collisions in New York City**

The machine learning approach in this work aligns with the efforts of New York City’s Vision Zero Initiative to eliminate all traffic deaths in the city by 2024. Through classification analysis of NYC Open Data’s robust, yet often disparate datasets on traffic crashes, (including demographics, time and location, behaviors, and roadway data) we can glean new insights to support this goal.

The goal of this research is to build a classification model that will predict whether a collision will result in injury (including fatalities). With an accurate predictive model, we can shift our analysis to feature importance. By identifying key features in the dataset that are likely to occur in a crash resulting in injury, we can target behavior and policy to decrease the occurrence of the most severe accidents. Further discussion will include implications for building on this model for future work.

## Data
There are 5 CSV files within the data folder. However, since all data is queried directly from the source's API or imported from an existing library, none of the files are required to run code. I included them here, in the event queries are unsuccessful beyond client control. The Jupyter notebook includes comments on where to import data if queries are unsuccessful. The data is as follows:

##### Raw Data

- Crashes_Data.CSV: NYC Open Data on crash statistics
- Vehicle_Data.CSV: NYC Open Data on vehicles involved in Crashes_Data
- Road_Data.CSV: NYC Open Data on street characteristics

##### Processed Data

- Combined_DF_Data.CSV: Simple combination of the three raw datasets. No other preprocessing completed.
- Cleaned_Data.CSV: Fully preprocessed data ready for use in ML section of Jupyter Notebook

## Requirements
The included *Requirements.txt* file allows for efficient installation of the libraries necessary to run the notebook. These libraries included
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- fuzzymatcher: probablistic matching of data frames on textual columns. Used in combining dataframes.
- datetime: allows for processing of datetime objects into numerical data
- meteostat: library containing historical weather data from various stations
