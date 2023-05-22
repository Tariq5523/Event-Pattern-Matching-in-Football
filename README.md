# Event-Pattern-Matching-in-Football
The aim of this project is to match similar events that happened in football matches (such as passes or shots). The dataset for the project contained around 4.7 million events from several popular football leagues (such as the Premier League and La Liga).
Summary of methodologies:
- Created a scalable database using MongoDB to store the events from matches and their relevant information.
-	Created indexes that helped in querying the data efficiently. 
-	Used Dynamic Time Warping (DTW) to match football events patterns (using the Python library fastdtw).
-	Evaluated the results by visualizing the patterns of football events on a football pitch plot (using Python libraries: mplsoccer and matplotlib).

The MongoDB database is set up locally and this script allows to connect to it and perform the necessary queries.

The database consists of the Events from the StatsBomb Open Data [1]. The Events were imported into the database using the mongoimport command line tool. The Events are stored in the eventswithID collection in the statsbomb database. The Events are stored in the database in the same format as they are in the JSON files provided by StatsBomb.

Our collection contains an extra variable called the match_id which is an identifier. This is used to identify the match in which the events takes place. The match_id is not present in the original JSON files provided by StatsBomb.

The code uses Python 3.9.16 and PyMongo 4.3.3. Using MongoDB: 6.0.5 Using Mongosh: 1.8.0

[1] https://github.com/statsbomb/open-data
