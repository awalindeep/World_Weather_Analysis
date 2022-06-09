# World Weather Analysis

World Weather Analysis using API

## Project Overview

The purpose of this project is to collect, analyze and visualize weather data across cities worldwide and to provide travellers with a tool that will allow them to determine their travel destination based on weather conditions.We had to put together a beta version of an application for potential travel technology services that specializes in hotel and logging industry. The application collects and presents data for customers via the search page that can be filtered based on preferred travel criteria in order to find their ideal hotel anywhere in the world.

*This project consists of three modules.*

### 1. Weather Database

* In this module we used  **NumPy**  random module to retrieve 2000 random coordinates (latitudes and longitudes) and  **CityPy**  module to define the closest city names based on these coordinates. 
* Once city names were stored in a list, we used  **Open Weather APIs**  to request json weather data from a website. After cleaning the data, final results were transformed into Pandas data frame and stored in [CSV file](https://github.com/awalindeep/World_Weather_Analysis/blob/AwalinGHMAIN/Weather_Database/WeatherPy_Database.csv).
![Weather Database](https://github.com/awalindeep/World_Weather_Analysis/blob/AwalinGHMAIN/Weather_Database/Weather_Database.png)
*Data frame from Open Weather API.*

### 2. Vacation Search

* In this module we used  **input**  function to take and store potential customer preferred minimum and maximum temperatures. 
* Based on the input we used Pandas  **loc**  method on Weather Database file to filter the data. 
* We also used  **Google Maps APIs**  to retrieve hotel names. After cleaning the data, the data frame was exported to [CSV file](https://github.com/awalindeep/World_Weather_Analysis/blob/AwalinGHMAIN/Vacation_Search/weatherpy_vacation.csv). 
* With the  **Jupyter gmaps module**  we plotted map with pop-up message that includes hotel name, city, country and weather information.

![Weatherpy](https://github.com/awalindeep/World_Weather_Analysis/blob/AwalinGHMAIN/Vacation_Search/WeatherPy_vacation_map.png)


*Map by Google Directions with 4 connecting points and Google Map with pop-up message with hotel and weather information.*

### 3. Vacation Itinerary

* In this module we selected 4 hotel destinations that potential customers might like to use for their trip planning. 
* Based on selection I extracted coordinates with  **to_numpy()**  function and used  **Google Directions API**  to connect and mark those points via selected traveling mode.
![Weather Map](https://github.com/awalindeep/World_Weather_Analysis/blob/AwalinGHMAIN/Vacation_Itinerary/WeatherPy_travel_map.png)

![Weather marker](https://github.com/awalindeep/World_Weather_Analysis/blob/AwalinGHMAIN/Vacation_Itinerary/WeatherPy_travel_map_markers.png)
*Map by Google Directions with 4 connecting points and Google Map with pop-up message with hotel and weather information.*

### Resources
-   Software
    *-   Jupyter Notebook*
-   Python
-   Dependencies
    *-   Pandas Library*
    *-   Numpy Library*
    *-   CitiPy Module*
    *-   Python Requests*
-   APIs
    *-   **Open Weather APIs**  to retrieve weather data.*
    *-   **Google Maps API**  to create heat maps and retrieve information about hotels around the world.*
    *-   **Google Directions API**  to map the direction between 4 points.*
