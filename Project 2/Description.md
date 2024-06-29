## Project description

You're working as an analyst for Zuber, a new ride-sharing company launching in Chicago. Your task is to find patterns in the available information, understanding passenger preferences, and the impact of external factors on rides.

Working with a database, you'll analyze data from competitors and test hypotheses about the impact of weather on ride frequency.

## Description of the data

### Database with info on taxi rides in Chicago:

- **neighborhoods table**: Data on city neighborhoods
  - name: Name of the neighborhood
  - neighborhood_id: Neighborhood code

- **cabs table**: Data on taxis
  - cab_id: Vehicle code
  - vehicle_id: The vehicle's technical ID
  - company_name: The company that owns the vehicle

- **trips table**: Data on rides
  - trip_id: Ride code
  - cab_id: Code of the vehicle operating the ride
  - start_ts: Date and time of the beginning of the ride (time rounded to the hour)
  - end_ts: Date and time of the end of the ride (time rounded to the hour)
  - duration_seconds: Ride duration in seconds
  - distance_miles: Ride distance in miles
  - pickup_location_id: Pickup neighborhood code
  - dropoff_location_id: Dropoff neighborhood code

- **weather_records table**: Data on weather
  - record_id: Weather record code
  - ts: Record date and time (time rounded to the hour)
  - temperature: Temperature when the record was taken
  - description: Brief description of weather conditions, e.g., "light rain" or "scattered clouds"

### Table scheme
![Table Scheme](image)

**Note**: There isn't a direct connection between the trips and weather_records tables in the database. But you can still use JOIN and link them using trips.start_ts and weather_records.ts.

## Instructions on completing the project

### Step 1. Exploratory data analysis

1. Find the number of taxi rides for each taxi company for November 15-16, 2017. Name the resulting field trips_amount and print it along with the company_name field. Sort the results by trips_amount in descending order.

2. Find the number of rides for every taxi company whose name contains the words "Yellow" or "Blue" for November 1-7, 2017. Name the resulting variable trips_amount. Group the results by the company_name field.

3. In November 2017, the most popular taxi companies were Flash Cab and Taxi Affiliation Services. Find the number of rides for these two companies and name the resulting variable trips_amount. Join the rides for all other companies in the group "Other." Group the data by taxi company names. Name the field with taxi company names company. Sort the result in descending order by trips_amount.

### Step 2. Determine if and how the duration of rides from the Loop to O'Hare International Airport changes on rainy Saturdays compared to other days of the week and other weather conditions.

1. Retrieve the identifiers of the O'Hare and Loop neighborhoods from the neighborhoods table.

2. For each hour, retrieve the weather condition records from the weather_records table. Use the CASE operator to categorize hours into "Bad" if the description field contains "rain" or "storm," and "Good" for other conditions. Name the resulting field weather_conditions.

3. Retrieve rides from the trips table that started in the Loop (neighborhood_id: 50) and ended at O'Hare (neighborhood_id: 63) on a Saturday. Fetch weather conditions for each ride using the method from the previous step. Also, retrieve the duration of each ride. Ignore rides where weather condition data is unavailable.

The takeaway sheets and summaries from previous lessons have everything you need to complete the project.
