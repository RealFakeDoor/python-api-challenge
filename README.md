Dependencies:
matplotlib.pyplot
pandas
numpy
requests
time
scipy.stats.linregress
pprint
datetime
citipy
hvplot.pandas
pathlib



Weather Data Analysis
This Python script retrieves weather data for a list of randomly selected cities across the globe using the OpenWeatherMap API. It then analyzes and visualizes the relationship between various weather parameters and latitude.

Obtain an API key from OpenWeatherMap and save it in a file named api_keys.py.

Ensure you have a folder named output_data in the same directory where you run the script to store the output CSV and plots.

Logic Overview:

City Selection: 
Utilizes citipy to select a random list of cities based on latitude and longitude coordinates.

API Calls & Data Processing: 
Fetches weather data for each city from the OpenWeatherMap API including:
temperature, humidity, cloudiness, and wind speed.

Visualization: 
Generates scatter plots to visualize the relationships between latitude and weather parameters. 
Calculates linear regression for specific hemispheres to analyze trends.

Output: 
Saves the weather data to a CSV file and scatter plots to PNG files.





Hotel Finder with Geoapify API

This Python script utilizes the Geoapify API to find hotels near cities with ideal weather conditions. It begins by loading weather data for cities from a CSV file, filters cities based on weather criteria, and then searches for nearby hotels using Geoapify API. Finally, it displays the locations of the cities and the found hotels on an interactive map.

Logic overview:

Loading Weather Data: 
The script loads weather data for cities from a CSV file created in a previous steps.

Plotting All Data Points: 
It plots all cities on an interactive map using hvplot.pandas to visualize their locations and humidity levels.

Filtering Cities: 
The script filters cities based on predefined weather criteria such as temperature range, wind speed, and cloudiness to find cities with ideal weather conditions.


Creating DataFrame for Hotels: 
It creates a new DataFrame to store information about the cities with ideal weather conditions and an empty column for hotel names.

Searching for Hotels: 
For each city in the DataFrame, the script makes an API request to Geoapify to find the nearest hotel within a specified radius of 10 000 metres.

Storing Hotel Information: 
It stores the name of the nearest hotel (if found) in the DataFrame.

Plotting Cities and Hotels: 
Plots the locations of the filtered cities and the found hotels on an interactive map using hvplot.pandas.




Files:
WeatherPy.ipynb:
upyter Notebook containing the Python script for weather data analysis.

output_data/cities.csv: 
CSV file containing the weather data for the selected cities.

output_data/Fig1.png, Fig2.png, Fig3.png, Fig4.png: 
Scatter plots depicting the relationships between latitude and various weather parameters.

VacationPy.ipynb: 
Jupyter Notebook containing the Python script for finding hotels with ideal weather conditions.

output_data/cities.csv: 
CSV file containing weather data for the selected cities.



Instructions:
Run the WeatherPy.ipynb script in a Jupyter Notebook environment or any Python IDE.
Run the VacationPy.ipynb script in a Jupyter Notebook environment or any Python IDE.

