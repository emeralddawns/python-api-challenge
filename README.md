# python-api-challenge
This assignment consisted of using python pandas in Jupyter Notebook to create a list from a python library, pull data from an API, perform an analysis, output plots, and create maps using gmaps.

# What the code does (in general terms)
**Weatherpy** creates a list of cities from https://pypi.python.org/pypi/citipy, retrieves data from https://openweathermap.org/api, reads thru the data, plots the data and any requested trend lines, and displays the r-values and equations for the trend lines.

**Vacationpy** creates a heat map of humidity levels for all of the cities found in **Weatherpy**, reduces the list to only cities that match certain parameters, and displays the nearest hotels in 10 of those cities using jupyter-gmaps and Google Places API.

# What the code calculates
The **Weatherpy** code currently calculates and displays the following:

    The processing list for 500+ cities found using citipy

    Scatter plots displaying the following information for all cities:
        * Temperature (F) vs. Latitude
        * Humidity (%) vs. Latitude
        * Cloudiness (%) vs. Latitude
        * Wind Speed (mph) vs. Latitude
    
    Scatter plots with added trend lines displaying the following information for all cities:
        * Northern Hemisphere - Temperature (F) vs. Latitude
        * Southern Hemisphere - Temperature (F) vs. Latitude
        * Northern Hemisphere - Humidity (%) vs. Latitude
        * Southern Hemisphere - Humidity (%) vs. Latitude
        * Northern Hemisphere - Cloudiness (%) vs. Latitude
        * Southern Hemisphere - Cloudiness (%) vs. Latitude
        * Northern Hemisphere - Wind Speed (mph) vs. Latitude
        * Southern Hemisphere - Wind Speed (mph) vs. Latitude

The **Weatherpy** code currently calculates and displays the following:

    A heat map displaying humidity levels for the cities found in **Weatherpy**

    A reduced list of cities based on preferred vacation weather

    A map of the nearest hotel within 5000 meters of city coordinates for 10 cities

# Observable Trends in **Weatherpy**
The following trends have been observed in the data:

1) The majority of cities appear to have humidity levels above 60%.  This may be due to major cities tending to be located near water sources, which increase the humidity of surrounding areas.

2) The northern hemisphere has a strong negative correlation between maximum temperature and latitude, while the southern atmosphere has a negative correlation.  Temperatures trend higher closer to the equator (latitude 0) because the equator and surrounding regions receive the greatest amount of direct sunlight. The northern hemisphere is currently angled away from the sun (causing overall cooler temperatures), while the southern hemisphere is angled toward the sun (causing overall warmer temperatures).

3) The other attributes looked at (humidity, cloudiness, and wind speed) had fairly weak correlations to latitude. This is likely because those three attributes have various other presiding factors, such as altitude and topography. 
