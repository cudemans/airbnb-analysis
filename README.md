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
from sklearn.neighbors import KNeighborsRegressor
from sklearn.model_selection import train_test_split
```

## Investigation

The notebooks have been structured to answer several questions:

1. What times of year are most expensive?
2. What times of year are the majority of properties available for rent?
3. Which factors affect listing prices?
4. What factors affect a property's rating?

## Findings
