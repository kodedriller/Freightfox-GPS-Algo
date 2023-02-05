# Freightfox-GPS-Algo-ans

# Outputs 

start_timestamp,end_timestamp,"[ {lat1, long1}, {lat2, long2}] ] "
2023-02-04 06:08:01,2023-02-04 06:21:44,"[{'lat': 18.49616241455078, 'long': 73.97174835205078}, {'lat': 18.503061294555664, 'long': 73.92486572265625}]"
2023-02-04 06:21:54,2023-02-04 06:39:08,"[{'lat': 18.50324440002441, 'long': 73.9241943359375}, {'lat': 18.518442153930664, 'long': 73.87915802001953}]"
2023-02-04 06:39:09,2023-02-04 07:38:11,"[{'lat': 18.51846694946289, 'long': 73.87911987304688}, {'lat': 18.50892448425293, 'long': 73.83185577392578}]"
2023-02-04 07:38:21,2023-02-04 07:59:18,"[{'lat': 18.508337020874023, 'long': 73.83070373535156}, {'lat': 18.507307052612305, 'long': 73.7830810546875}]"
2023-02-04 07:59:19,2023-02-04 08:53:34,"[{'lat': 18.5073184967041, 'long': 73.78304290771484}, {'lat': 18.47183609008789, 'long': 73.81222534179688}]"
2023-02-04 08:53:35,2023-02-04 09:34:09,"[{'lat': 18.47180938720703, 'long': 73.81224060058594}, {'lat': 18.448516845703125, 'long': 73.85594940185547}]"
2023-02-04 09:36:07,2023-02-04 09:54:08,"[{'lat': 18.44727897644043, 'long': 73.85778045654297}, {'lat': 18.485435485839844, 'long': 73.88810729980469}]"
2023-02-04 09:56:10,2023-02-04 10:14:07,"[{'lat': 18.490297317504883, 'long': 73.89444732666016}, {'lat': 18.50042152404785, 'long': 73.94180297851562}]"
2023-02-04 10:16:07,2023-02-04 10:24:08,"[{'lat': 18.499311447143555, 'long': 73.95004272460938}, {'lat': 18.49555778503418, 'long': 73.9732666015625}]"

<br>
# Logic
<br>
## Implementation
The Haversine formula is used to calculate the distance between two GPS coordinates. The script loops through the GPS data and compares the distances between consecutive GPS points. If the distance is less than or equal to the distance_range parameter, the end timestamp is updated and the current location is stored. If the distance is greater than the distance_range, the current stoppage is added to the results and a new stoppage starts.
<br>
A class named StoppageDetector that predicts stoppages from a GPS data file. The algorithm performs the following steps:
1. Reads a GPS data file in the form of a CSV file using the pandas library.
2. Initializes some variables for storing start and end timestamps and current and previous locations.
3. Loops through the GPS data to find the distance between consecutive points.
4. If the distance between two points is less than or equal to a user-defined distance_range, then the end_timestamp is updated and current_location is stored.
5. If the distance is greater than the distance_range, then the result list is updated with the start_timestamp, end_timestamp and a list of dictionaries containing the previous and current locations.
6. The result list is then returned as a list of tuples.
7. The result list is then converted to a Pandas dataframe and written to a CSV file.
