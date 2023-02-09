# World_Weather_Analysis
## **Learning to use WeatherPy with Python APIs**

#### This Read Me Contains: 

​    1 - Project description and a three part project summary.
​    2 - List of outputs: files and pictures.

### 1 - Project Description. Module G6 Challenge WeatherPy.  

1. Generate random latitudes and longitudes and use them to pull cities from citipy library. 
2. Make API calls to OpenWeatherMap to pull Weather data based on lats and lngs.
3. Use inputs on weather preferences to crawl Google Nearby Search for related data
4. Plot a Google map showing cities meeting preferences, with a marker layer
5. Use Google Direction Layers to plot a map of selected cities
6. Use Google Marker Layers to plot info for selected vacation cities.
   	

### Part I. Get the Weather Description and Amount of Precipitation for Each City

1. Add the latitudes and longitudes to a list.
2. Get the nearest city using the citipy module. 
3. Perform an API Call with the OpenWeatherMap.
   1. Return: Latitude and Longitude, Max Temp, Percent Humidity, Percent Cloudiness, Wind Speed, Weather description
   2. Return: Rainfall -use try-except, if it is raining get rainfall # in last three hours. If not raining, add 0 for city
   3. Return: Snow -use try-except, if it is snowing get snowfall # in last three hours. If not snowing, add 0 for city
4. Add collected data to new datafram
5. Save the new DataFrame as CSV to be used later in Part II.  as weatherPy_challenge.csv
6. Sync to Github
7. Using Pandas: How many cities have recorded rainfall or snowfall? 
   1. *answer to #7:   In the Weather_Database.ipynb, the results were 72 cities showing rain and 23 cities showing snow.*

### Part II. Provide inputs for customers to narrow Travel Searches based on Temp and Rain.

1. Import Weather Data CSV as new Dataframe.
2.  Filter the DF for min and max temps and presence of rain or snow
   1. a Prompt Customer for Min Temperature Preference
   2. Prompt Customer for Max Temperature Preference
   3. Prompt Customer for Rain Preference
   4. Prompt Customer for Snow Preference
3. Add the cities to a marker layer map with pop-marker for each city that includes: 
   1. Hotel name,
   2. City,
   3. Country,
   4. Current Weather Descrip with Max Temp
4. Create the Hotel DF.
5. Configure search parameters
6. Crawl through Google NearbySearch to get data based on our locations
   1. Iterate through the DataFrame by row, and populate the info_box_template
   2. Save and upload new DF as WeatherPy_vacation.csv
   3. Save and upload new marker layer map as WeatherPy_vacation_map.png

### Part III. Create a Travel Itinerary with a Corresponding Map

1. Create new Jup NB as Vacation_Itinerary
2. Import WeatherPy_vacation.csv as new DF
3. From the vacation search map,  choose at least four cities in close proximity on your map that are on the same continent that customer may like  and create a directions layer map.
4. Create needed dataframes. One per city and one with all the filtered cities.   Use list indexing to get the latitude and longitude pairs.
5. Create the travel map as WeatherPy_travel_map.png
6. Create the marker layer travel map
   1.  Use info_box_template and iterate thru DF to populate the info_box_template.
   2. Create the marker layer travel map as WeatherPy_travel_map_markers.png.

## 2 - List of outputs. Files and pictures.

### Code: 

1. Weather_Database.ipynb
2. Vacation_Search.ipynb
3. Vacation_Itinerary.ipynb

### CSV Files: 

1. ​	Weather_Py_challenge.csv
2. Weather_Py_vacation.csv
   	

### Image Files: 

1. WeatherPy_vacation_map.png
2. WeatherPy_travel_map.png
3. WeatherPy_travel_map_markers.png