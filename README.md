# python-api-challenge


* Context: This weather dataset contains detailed city and corresponding weather data, such as city name, country, latitude and longitude, maximum temperature, cloudiness, wind speed and date of data capture.

* Objective: This analysis aimed to gather city-specific weather data and identify correlations between latitude and the above mentioned weather variables. For example, one of the elements examined is the correlation between latitude and humidity.

* Solution: I used the OpenWeatherMap API to retrieve cities' weather data and used the python scripting to analyze the votes by candidate by tracking the the unique list of candidates and the percentage of votes each candidate won. 

I leveraged panda's hvplot library to illustrate the humidity distribution among various cities and also used the Geoapify API to find the first hotel located wtihin 10,000 miles of my coordinates in each city.

    Following libraries were imported:

    * import matplotlib.pyplot as plt
    * import pandas as pd
    * import numpy as np
    * import requests
    * import time
    * from scipy.stats import linregress
    * from scipy import stats
    * from api_keys import weather_api_key
    * from citipy import citipy
    * import hvplot.pandas

# Import API key
from api_keys import geoapify_key

* Findings: 
  1) Latitude and maximum temperature does not have a strong correlation
  2) Within -20 to 70 latitude, the high and low extreme tends to have the highest humidity; whereas within 0 to 40 altitude, the closer it is to 20 latitude, the humidity tent to drop more visibly.
  3) City latitude and wind speed oes not have a strong correlation
  4) Nothern vs Southern hemisphere comparison:
        * Northern: 
        * temperature & Lat: negative correlation
        * cloudiness & Lat: positive correlation 
        * wind speed & Lat: neutral relation

        Southern: 
        * temperature & Lat: positive correlation
        * cloudiness & Lat: positive correlation 
        * wind speed & Lat: slightly negative corelation, almost minimal

* Finding Explanation:
    Latitude is correlated with a variety of weather variables such as cloudiness, temperature, etc.

* Citation:
  * When troubleshooting the OpenWeatherAPI call, our kwon helped me identify the current weather base url should be used instead of the weather forecast url. I also checked my coding errors throughout using bootcamp's expert learning assistant.