# World Weather Analysis
## Background
Jack loves the PlanMyTrip app. Beta testers love it too. And, as with any new product, they’ve recommended a few changes to take the app to the next level. Specifically, they recommend adding the weather description to the weather data I've already retrieved in this module. Then, I'll have the beta testers use input statements to filter the data for their weather preferences, which will be used to identify potential travel destinations and nearby hotels. From the list of potential travel destinations, the beta tester will choose four cities to create a travel itinerary. Finally, using the Google Maps Directions API, I will create a travel route between the four cities as well as a marker layer map.

## What I'm Creating
This new assignment consists of three technical analyses. You will submit the following deliverables:

* Deliverable 1: Retrieve Weather Data
* Deliverable 2: Create a Customer Travel Destinations Map
* Deliverable 3: Create a Travel Itinerary Map

### Resources
* Data Sources: cities.csv
* Software: Python 3.7.6, Jupyter Notebook 6.4.5
* Libraries: NumPy, CitiPy, Pandas, Matplotlib
* Interchange formats/interfaces: OpenWeatherMap API, Google Places API, JSON

## Deliverable 1: Retrieve Weather Data 
### Retrieve all of the following information from the API call:

- Latitude and longitude
- Maximum temperature
- Percent humidity
- Percent cloudiness
- Wind speed
- Weather description (for example, clouds, fog, light rain, clear sky)

![image](https://user-images.githubusercontent.com/87340105/155856571-802ef29a-7b7d-4d82-8614-f9d9d6de27b1.png)

### Add the weather data to a new DataFrame

![image](https://user-images.githubusercontent.com/87340105/155856667-b65d7893-8eea-4ef1-a5ec-147964e48454.png)

### Export the DataFrame as WeatherPy_Database.csv into the Weather_Database folder

![image](https://user-images.githubusercontent.com/87340105/155856695-272b441f-c718-4e9a-8386-5ec4d0aed3eb.png)

## Deliverable 2: Create a Customer Travel Destinations Map

### In Step 1, import the WeatherPy_Database.csv file from your Weather_Database folder from Deliverable 1 as a DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155857073-76f32963-bbf7-4e3e-a3c3-7b8fb54a2ab8.png)

### In Step 2, write two input statements that prompt the user to enter their minimum and maximum temperature criteria for their vacation.

![image](https://user-images.githubusercontent.com/87340105/155857099-a1c17e28-e0f9-42f2-a301-0a1d69618a42.png)

### In Step 3, use the loc method to filter the city_data_df DataFrame for temperature criteria collected in Step 2, then create a new DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155857120-86e3bdda-1609-4d04-a00e-f5c88a394113.png)

### In Steps 4a-b, determine if there are any empty rows, then drop them if necessary and create a new DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155857136-699b8030-447c-4aa5-b393-3c91d7672da0.png)

![image](https://user-images.githubusercontent.com/87340105/155857149-7be567bc-ef33-49b8-b32a-c8fc77f9998f.png)

### In Steps 5a-b, use the provided code to create a new DataFrame, hotel_df, that will hold the hotel names from the hotel search in Steps 6a-6f.

![image](https://user-images.githubusercontent.com/87340105/155857161-289f1bfa-5683-4557-8bed-ebc58460ef63.png)

### In Step 6a, we have supplied the search parameters, which are the same as in this module, that you’ll need to use to search for a hotel for each city in Steps 6b-f.

![image](https://user-images.githubusercontent.com/87340105/155857478-d1df2abf-5401-425f-8e74-03420e1fd42c.png)

### In Steps 6b-f, iterate through the hotel_df DataFrame, retrieve the latitude and longitude of each city to find the nearest hotel based on the search parameters from Step 6a, then add the hotel name to the hotel_df DataFrame. If a hotel isn't found, skip to the next city.

![image](https://user-images.githubusercontent.com/87340105/155857491-aaaf07e6-0483-4a30-9257-c0b1c9bf9861.png)


### In Step 7, drop any rows in the hotel_df DataFrame where a hotel name is not found.

Before exporting your DataFrame as a CSV, take a moment to confirm that your hotel_df DataFrame looks similar to the image below.
