# [Analyzing Flight Delays and Cancellations](https://projects.datacamp.com/projects/1962)

## Project Description
Unlock the secrets of flight delays and cancellations with data analysis! Dive into the world of aviation data to identify key factors and airlines most affected by disruptions in the Pacific Northwest by using your data wrangling, data visualization, and exploratory data analysis skills.


## Project Instructions (modified)
Which airlines and routes (for example "PDX-SFO") are most affected by flight delays, and what impact does wind have on departure delays?

- Load the two CSV files into separate DataFrames. Explore the data and create any new columns that might benefit your analysis.
- For routes, calculate the average departure delays (`mean_dep_delay`) and highest number of canceled flights (`total_cancellations`) and store this as a DataFrame called `routes_delays_cancels`, resetting the index after calculating.
- For airlines, determine the average departure delays (`mean_dep_delay`) and the highest number of canceled flights (`total_cancellations`) and store this as a DataFrame called `airlines_delays_cancels`, resetting the index after calculating.

- Produce two bar graphs to show (1) the top 9 highest number of cancellations (`top_routes_by_cancellations`) by route in a plot called `top9_route_cancels_bar` and (2) the top 9 highest average departure delays (`total_cancellations`) by airline in a plot called `top9_airline_delays_bar`.

- Determine if 10 mile per hour wind gusts or more have a larger average departure delay for both of SEA and PDX, setting `wind_response` to `True` if so and `False` if not.


### How to approach the project
1. Loading and manipulating data
2. Finding the average of aggregated data
3. Identifying the airlines and routes most affected
4. Creating data visualizations
5. Identifying whether larger wind gusts contribute to bigger delays

**Steps to complete**

### 1. Loading and manipulating data
Load the `flights2022` dataset and create the route column.
- Reading in a CSV file
- Generate a new column called `route` combining `origin` and `dest` with a "-" separating

### 2. Finding the average of aggregated data
For each route, use .groupby() and .agg() to find the mean departure delay and number of canceled flights as `routes_delays_cancels`, and do a similar analysis for airlines in `airlines_delays_cancels`.

- Aggregate after grouping
- Calculation inside aggregation
- Lambda functions

### 3. Identifying the airlines and routes most affected
For each of `routes_delays_cancels` and `airlines_delays_cancels` identify the top 9 highest mean departure delays (`top_routes_by_cancellations`) and number of cancellations (`total_cancellations`).

- Sorted values
- Descending sorted values

### 4. Creating data visualizations
Design plots showing (1) highest number of cancellations by route saved to `top9_route_cancels_bar` and (2) highest average departure delay by airline  saved to `top9_airline_delays_bar`.

- Creating a figure and axes object
- Creating a bar graph
- Add appropriate labels and titles to a graph
- Rotating the axis

### 5. Identifying whether larger wind gusts contribute to bigger delays
Create a new column (`group`) with the `flights_weather2022` data, splitting the data at 10 miles per hour.

- Lambda function with if-else
- Aggregate grouping by both the new variable and origin
- Review results to see if 10 mph or higher wind gusts contributes to greater average departure delays
