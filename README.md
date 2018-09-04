# Data Description

## Overview
This section describes a dataset with information on single-family homes in Denver, CO.  These data were used to fit a model for predicting home values.  After constructing such features as comparables-based valuation, forecaseted value using the last and previous sale prices and home-specific features (e.g., the number of bedrooms and square footage), a random forest model was fit using a training set and evaluated using a test set.  The model produced the test set R-squared of 0.92.  The subsequent sections discuss the steps that I took in more detail. 

Cleaning and processing of the data are described in the [next section](https://eagronin.github.io/housing-forecast-prepare/).

The analysis for this project was performed in Python.

## Data 
The dataset contains 15,000 records with information on single-family homes in Denver, CO.  Home values in the dataset are the Zillow "zestimates" for each home.  The other variables in the dataset are shown below:

```
id
address 
city
state
zipcode
latitude
longitude
bedrooms
bathrooms
rooms
square footage
lot size (in sq. feet)
year built
last sale date
last sale amount
prior sale date
prior sale amount
```

The data was loaded from a CSV file into a Pandas data frame:

```python
data = pd.read_csv('single_family_home_values.csv')
```

Next step:  [Data Preparation](https://eagronin.github.io/housing-forecast-prepare/).
