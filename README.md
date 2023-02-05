# Freightfox-GPS-Algo-ans

# Output

![Screenshot_20230205_045518](https://user-images.githubusercontent.com/74095019/216816014-e37aff58-c465-452c-ad54-2afeeab9a847.png)

# Logic

A class named StoppageDetector that predicts stoppages from a GPS data file. The algorithm performs the following steps:
1. Reads a GPS data file in the form of a CSV file using the pandas library.
2. Initializes some variables for storing start and end timestamps and current and previous locations.
3. Loops through the GPS data to find the distance between consecutive points.
4. If the distance between two points is less than or equal to a user-defined distance_range, then the end_timestamp is updated and current_location is stored.
5. If the distance is greater than the distance_range, then the result list is updated with the start_timestamp, end_timestamp and a list of dictionaries containing the previous and current locations.
6. The result list is then returned as a list of tuples.
7. The result list is then converted to a Pandas dataframe and written to a CSV file.
