# python-api-challenge
Using Python, APIs, and JSON traversals to answer questions about global and regional weather.

Part I - WeatherPy

This part consists of creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, the script utilizes a simple Python library (https://pypi.python.org/pypi/citipy), the OpenWeatherMap API (https://openweathermap.org/api), and analytical code to create a representative model of weather across world cities.

First, create a series of scatter plots to showcase the following relationships:

  Temperature (F) vs. Latitude
  Humidity (%) vs. Latitude
  Cloudiness (%) vs. Latitude
  Wind Speed (mph) vs. Latitude

Second, run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

  Northern Hemisphere - Temperature (F) vs. Latitude
  Southern Hemisphere - Temperature (F) vs. Latitude
  Northern Hemisphere - Humidity (%) vs. Latitude
  Southern Hemisphere - Humidity (%) vs. Latitude
  Northern Hemisphere - Cloudiness (%) vs. Latitude
  Southern Hemisphere - Cloudiness (%) vs. Latitude
  Northern Hemisphere - Wind Speed (mph) vs. Latitude
  Southern Hemisphere - Wind Speed (mph) vs. Latitude

The final notebook accomplishes the following:

  Randomly selects at least 500 unique (non-repeat) cities based on latitude and longitude.
  Performs a weather check on each of the cities using a series of successive API calls.
  Includes a print log of each city as it's being processed with the city number and city name.
  Save a CSV of all retrieved data and a PNG image for each scatter plot.


Part II - VacationPy

This part uses jupyter-gmaps and the Google Places API to plan future vacations.

First, create a heat map that displays the humidity for every city from part I above. Then, 
narrow down the DataFrame to find personal preference of ideal weather condition. For example:

  A max temperature lower than 80 degrees but higher than 70.
  Wind speed less than 10 mph.
  Zero cloudiness.

  Drop any rows that don't contain all three conditions.

The next task is to use Google Places API to find the first hotel for each city located within 
5000 meters of its coordinates.

Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.
