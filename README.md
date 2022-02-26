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

