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

![image](https://user-images.githubusercontent.com/87340105/155857541-5a7781b6-bf67-425c-91fb-edf5dc96242c.png)

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

![image](https://user-images.githubusercontent.com/87340105/155857579-e40223f7-3088-4f29-8e43-2439170d13af.png)

### In Steps 8a-b, create an output file to store the hotel_df DataFrame as WeatherPy_vacation.csv in the Vacation_Search folder.

![image](https://user-images.githubusercontent.com/87340105/155857610-5b38abb4-1bd5-436a-b59f-32cef0833661.png)

### In Step 9, add the city name, the country code, the weather description, and the maximum temperature for the city to the info_box_template format template we have provided.

![image](https://user-images.githubusercontent.com/87340105/155857626-cc0f4bf3-5cdd-4c40-9348-ed0610d38f46.png)

### In Step 10a, use the provided list comprehension code to retrieve the city data from each row, which will then be added to the formatting template and saved in the hotel_info list.

### In Step 10b, use the provided code snippet to retrieve the latitude and longitude from each row and store them in a new DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155857636-d8f25c20-0d0f-4f0c-9fee-dae3f0675066.png)

### In Steps 11a-b, refactor your previous marker layer map code to create a marker layer map that will have pop-up markers for each city on the map.

![image](https://user-images.githubusercontent.com/87340105/155857640-48f6eeba-c3f3-4a81-84d4-fb2e4dfd6faf.png)

### Take a screenshot of your map and save it to the Vacation_Search folder as WeatherPy_vacation_map.png.

![image](https://user-images.githubusercontent.com/87340105/155857659-017ad59e-62d6-45b7-b8ee-41306a0b4898.png)

## Deliverable 3: Create a Travel Itinerary Map
### In Step 1, import the WeatherPy_vacation.csv file from your Vacation_Search folder from Deliverable 2 as a DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155857745-a052f373-2532-44fb-b37d-757c9941d71f.png)

### In Steps 2-4, copy or refactor the code from Steps 11a-b of Deliverable 2 to create a marker layer map of the vacation search results.

![image](https://user-images.githubusercontent.com/87340105/155857788-91461391-21c9-4a33-ab4c-17e2a3108a2d.png)

### From the vacation search map, choose four cities that a customer might want to visit. They should be close together and in the same country.

![image](https://user-images.githubusercontent.com/87340105/155858057-8c75fd2c-acfa-4432-af0d-09e0c77cd3fb.png)

### In Step 5, use the variables we have provided and the loc method to create separate DataFrames for each city on the travel route.

![image](https://user-images.githubusercontent.com/87340105/155858027-a449fc3c-9c97-4f90-89c4-53e34b89df25.png)

### In Step 6, use the to_numpy() function and list indexing to write code to retrieve the latitude-longitude pairs as tuples from each city DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155858103-9d3e5e1c-168c-4819-b4de-6833ea05e3da.png)

### In Step 7, use the gmaps documentation (Links to an external site.) to create a directions layer map using the variables from Step 6, where the starting and ending city are the same city, the waypoints are the three other cities, and the travel_mode is either "DRIVING", "BICYCLING", or "WALKING".

![image](https://user-images.githubusercontent.com/87340105/155858119-f94a7419-3ab2-4841-8d07-d085e915d626.png)

### Take a screenshot of your map from Step 7 and save it to the Vacation_Itinerary folder as WeatherPy_travel_map.png.

![image](https://user-images.githubusercontent.com/87340105/155858140-b5589655-d4a3-4761-be51-2e70a8cbb8ec.png)

### In Step 8, use the provided concat() function code snippet to combine the four separate city DataFrames into one DataFrame.

![image](https://user-images.githubusercontent.com/87340105/155858209-4435cc82-d42a-4f93-80a7-f9525d113ae8.png)

### In Steps 9-11, refactor the code from Steps 2-4 to create a new marker layer map of the cities on the travel route.

![image](https://user-images.githubusercontent.com/87340105/155858218-45f5787b-a69c-4518-86fc-e02c4915f184.png)

### Take a screenshot of your map and save it to the Vacation_Itinerary folder as WeatherPy_travel_map_markers.png.

![image](https://user-images.githubusercontent.com/87340105/155858203-ad21d9af-dd4c-4d13-a44d-e53b906e85a6.png)
