# World_Weather_Analysis

World Weather Analysis
Basic Project Plan

Task: Collect and analyze weather data across cities worldwide.
Purpose: PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
Method: Create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data. Your analysis of the data will be split into three main parts, or stages.

### Collect the Data

Use the NumPy module to generate more than 1,500 random latitudes and longitudes.

Use the citipy module to list the nearest city to the latitudes and longitudes.

Use the OpenWeatherMap API to request the current weather data from each unique city in your list.

Parse the JSON data from the API request.

Collect the following data from the JSON file and add it to a DataFrame:

City, country, and date

Latitude and longitude

Maximum temperature

Humidity

Cloudiness

Wind speed

Exploratory Analysis with Visualization

### Create scatter plots of the weather data for the following comparisons:

Latitude versus temperature

Latitude versus humidity

Latitude versus cloudiness

Latitude versus wind speed

### Determine the correlations for the following weather data:

Latitude and temperature

Latitude and humidity

Latitude and cloudiness

Latitude and wind speed

### Create a series of heatmaps using the Google Maps and Places API that showcases the following:

Latitude and temperature

Latitude and humidity

Latitude and cloudiness

Latitude and wind speed

Visualize Travel Data

### Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences. Complete these steps:

Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.

Create a heatmap for the new DataFrame.

Find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.

Store the name of the first hotel in the DataFrame.

Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.

## Project Summary

Jack loves the PlanMyTrip app. Beta testers love it too. And, as with any new product, they’ve recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data you’ve already retrieved in this module. Then, you'll have the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, you will create a travel route between the four cities as well as a marker layer map.

This new assignment consists of three technical analyses. You will submit the following deliverables:

### Deliverable 1: Retrieve Weather Data
### Deliverable 2: Create a Customer Travel Destinations Map
### Deliverable 3: Create a Travel Itinerary Map
### Including a README.md.

## Resources and Before Start Notes:

Data Source: PyBer_Challenge_starter_code.ipynb named later as PyBer_Challenge.ipynb
Data File: file.csv

Software: Matplotli 3.2.2, Python 3.9, Visual Studio Code 1.50.0, Anaconda 4.8.5, Jupyter Notebook 6.1.4, Pandas

For more information, read the Documentation on Python data typess.

### Review the Geographic Coordinate System

We use the geographic coordinate system (GCS) to reference any point on Earth by its latitude and longitude coordinates.

Latitudes are imaginary lines on Earth that run parallel east to west and are measured in angular units called degrees, minutes, and seconds, with 60 minutes in a degree and 60 seconds in a minute. Sometimes a latitude is referred to as a parallel. Consider, for example, the embattled 38th parallel (38° north) in East Asia that roughly demarcates North Korea and South Korea.

The equator is an imaginary line around the middle of the earth that is equidistant from the North and South Poles and has a latitude of 0°. The equator splits Earth into Northern and Southern Hemispheres.


All latitude lines above the equator are measured northward and considered positive, after 0° (the equator) and up to 90°, or 90° north (the North Pole). All latitude lines below the equator are measured southward and considered negative, before 0° (the equator) and down to –90°, or 90° south (the South Pole).

The equator splits Earth into the Northern and Southern hemispheres, with positive north and negative south latitudes.

Longitudes are imaginary lines on Earth that run from the North to the South Poles and are called **meridians. The prime meridian represents zero meridian, the origin for longitude coordinates, and splits Earth into the Eastern and Western Hemispheres.

Review how to Generate Random Latitudes and Longitudes
Before we write the algorithm to generate the latitudes and longitudes, we need to refresh our memory of where people live in the world. Time for another quick geography lesson!

Earth's surface is covered by 70% water while the rest is covered by land. So, we can assume 70% of the latitude and longitude coordinates we generate are positioned over a body of water, whether an ocean, major lake (e.g., Lake Superior), or major river (e.g., Amazon). Geographic coordinates over a body of water may not be close to a city, especially if in the middle of an ocean.

Seven continental landmasses comprise 30% of Earth's surface. Some land is uninhabitable or sparsely populated due to extreme terrain and climes (e.g., Sahara, Siberia, the Himalayas, and areas of the western United States).

First consider the bodies of water. Start with at least 1,500 latitudes and longitudes, because 500 divided by 0.3 (30% land mass) equals 1,666 latitudes and longitudes.

We'll generate random latitudes and longitudes to ensure coordinates are fairly distributed around the world. An algorithm will pick random numbers between the low and high values for latitudes and longitudes. Also, the latitudes and longitudes must be floating-point decimal numbers, as each angular unit of degrees, minutes, and seconds can be represented by a decimal number. For example, Kailua-Kona, Hawaii has the angular coordinates 19° 38' 23.9784'' north and 155° 59' 48.9588'' west and can be written as a decimal number as follows: 19.639994, -155.996933.

To generate random numbers, we can use the Python random module. This module is part of the Python and Anaconda installation, so we don't need to install it. Let's test some random module functions to find one that can help us.

![image](https://user-images.githubusercontent.com/57301554/122156540-ca226000-ce2e-11eb-83c5-30850ad1c5c6.png)







