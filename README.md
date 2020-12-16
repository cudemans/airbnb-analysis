# Airbnb analysis

The purpose of this project is to create a pipleline for analysing Airbnb data for any city. It provides a backbone for analysis through a series of functions that prepare the data, analyse and visualizse, and clean it for furhter modeling.

The project consists of two notebooks: `seattle-analysis.ipynb` and `boston-analysis.ipynb`. Each notebook analyses the data from the respective cities.

In order to broaden this to the city of your choosing, find the datasets [here](http://insideairbnb.com/get-the-data.html). For each city, the required datasets are:

- `listings.csv` - Information about the property and owner, including its location, and its availability over time
- `calendar.csv.gz` - Information about when the availability and price per day
- `neighbourhoods.geojson` - Geographical data for the city's neighbourhoods

## Required imports and packages

```
import pandas as pd
import numpy as np
import geopandas as gpd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```

## Investigation

The notebooks have been structured to answer several questions:

1. What times of year are most expensive?
2. What times of year are the majority of properties available for rent?
3. Which factors affect listing prices?
4. What factors affect a property's rating?

## Findings

#### Seattle

1. The peak in prices came during the summer months. Year on year prices were significantly higher at the beginning of 2017 than the previous year.
2. For most neighborhoods, the mean availability was more than 50%, with a number of exceptions. Some neighborhoods including Greenwood, Genesee, and Montlake only reached these these levels of availability one or two months a year.
3. Highest correlations with the price of nightly rental include the number of people a property can accomodate, the number of bedrooms a property includes, how big the property is, and the number of beds.
4. Highest correlations to how well-rated a property is include other review metrics those that relate to value for money, cleanliness, and the accuracy of the listing.

#### Boston

1. October 2016 appeared to be the most expensive in the dataset, though there was another peak in mid-April 2017. Unlike in Seattle, prices fell year on year.
2. Properties in Boston were available less than those in Sealle. A significant number of the city's neighborhoods saw availability rates of less than 50% for the majority of the year.
3. Highest correlations with the price of nightly rental include the size of the property, how many people it accomodates, and the number of beds a property has.
4. Highest correlations to how well-rated a property is include other review metrics those that relate to value for money, cleanliness, and the accuracy of the listing.
