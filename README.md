# Python API Challenge: WeatherPy & VacationPy

## Overview

These assignments focus on analyzing weather data to answer questions about how weather patterns change based on geographic location (latitude) and to plan vacations based on ideal weather conditions. The project is divided into two parts:

1. **WeatherPy**: Visualizes the relationship between weather variables (e.g., temperature, humidity) and latitude across multiple cities globally.
2. **VacationPy**: Uses weather data to identify cities with ideal vacation weather and find nearby hotels using the Geoapify API.

---

## Part 1: WeatherPy

### Objective

The goal of **WeatherPy** was to retrieve weather data for over 500 cities worldwide using the OpenWeatherMap API and plot the relationships between latitude and various weather conditions.

### Process

1. **City Generation**: I generated random geographic coordinates and used the `citipy` library to find the nearest city for each set of coordinates.
2. **Weather Data Retrieval**: I used the OpenWeatherMap API to retrieve weather data (temperature, humidity, cloudiness, and wind speed) for each city.
3. **Scatter Plots**: Created scatter plots to show the relationship between latitude and each of the following variables:
   - Latitude vs. Temperature
   - Latitude vs. Humidity
   - Latitude vs. Cloudiness
   - Latitude vs. Wind Speed
4. **Linear Regression Analysis**: Computed linear regression for the above relationships, separating the data into the Northern Hemisphere and Southern Hemisphere. Each plot included the linear regression line, equation, and R-squared value.

### Key Findings

- **Temperature**: Strong correlation between latitude and temperature, with temperatures increasing near the equator (lower latitudes) and decreasing toward the poles.
- **Humidity, Cloudiness, and Wind Speed**: These variables showed weaker correlations with latitude, indicating that other factors (e.g., geographic features, local weather patterns) likely play a significant role.

---

## Part 2: VacationPy

### Objective

The goal of **VacationPy** was to use the weather data generated from **WeatherPy** to plan a vacation by finding cities with ideal weather conditions. Additionally, I used the Geoapify API to find hotels within a 10,000-meter radius of these ideal cities.

### Process

1. **Filtering Ideal Vacation Cities**: I filtered the cities based on ideal weather conditions:
   - Temperature between 21°C and 27°C.
   - Wind speed less than 4.5 meters per second.
   - Clear skies (cloudiness = 0).
2. **Hotel Search Using Geoapify API**: For each city with ideal weather conditions, I used the Geoapify API to find the nearest hotel within a 10,000-meter radius.
3. **Interactive Map**: Created an interactive map using `hvPlot` to display the cities. The hover functionality included the city name, country, hotel name, and humidity level.

### Key Results

- Cities with ideal vacation weather conditions were successfully identified, and nearby hotels were found.
- The final interactive map allows for easily exploring vacation cities with hotels.

---

## Tools and Libraries Used

- **Python**: Used as the main programming language.
- **OpenWeatherMap API**: Used to retrieve weather data for multiple cities.
- **Geoapify API**: Used to find nearby hotels for cities with ideal weather conditions.
- **Pandas**: For data manipulation and DataFrame operations.
- **Matplotlib**: Used to create scatter plots for visualizing weather relationships.
- **hvPlot**: Used to create interactive maps with hover functionality.
- **SciPy**: Used for linear regression analysis.
