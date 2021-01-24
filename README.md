# Python API - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. I used Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"


![Equator](Images/equatorsign.png)

## [Part I - WeatherPy](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/starter_code/WeatherPy.ipynb)

In part-I, a Python script was created to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), to create a representative model of weather across world cities.

I created a series of scatter plots to showcase the following relationships:

* [Temperature (F) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/output_data/Fig1.png)
* [Humidity (%) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/output_data/Fig2.png)
* [Cloudiness (%) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/output_data/Fig3.png)
* [Wind Speed (mph) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/output_data/Fig4.png)

Note: a written analysis is provided after each plot. 

Then a linear regression analysis was performed to determined each relationship, only this time, separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* [Northern Hemisphere - Temperature (F) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/north_temp_lg.png)
* [Southern Hemisphere - Temperature (F) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/south_temp_lg.png)
* [Northern Hemisphere - Humidity (%) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/north_humidity_lg.png)
* [Southern Hemisphere - Humidity (%) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/south_humidity_lg.png)
* [Northern Hemisphere - Cloudiness (%) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/north_cloud_lg.png)
* [Southern Hemisphere - Cloudiness (%) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/south_cloud_lg.png)
* [Northern Hemisphere - Wind Speed (mph) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/north_wind_lg.png)
* [Southern Hemisphere - Wind Speed (mph) vs. Latitude](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/south_wind_lg.png)

After each pair of plots, an explanation of what the linear regression is modeling, such as any relationships or associations, and any other analysis.


### [Part II - VacationPy](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/starter_code/VacationPy.ipynb)

In part-II, the weather data outputted in part-I was used to plan future vacations using a jupyter-gmaps and the Google Places API.

* A heat map displaying the humidity for every city from the part-I was created.

  ![heatmap](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/Heat_map1.png)

* The DataFrame to find ideal weather conditions was narrowed down. For example:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

* The Google Places API was used to find the first hotel for each city located within 5000 meters of the coordinates.

* The hotels were plotted on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](https://github.com/Chahnaz-Kbaisi/Python-API-WeatherPy-VacationPy/blob/main/Images/Hotel_map1.png)

