-- Creating a table of first three months of data for 2022
CREATE TABLE biketrips2022Q1 AS
SELECT * FROM `biketrips2022-01`
UNION
SELECT * FROM `biketrips2022-02`
UNION
SELECT * FROM `biketrips2022-03`;

-- Compare the number of trips made by casual riders vs. member riders
SELECT COUNT(ride_id) AS number_of_users, member_casual AS type_of_user
FROM biketrips2022q1
GROUP BY member_casual; 

-- Compare the number of electric, docked and classic bikes used for trips
SELECT COUNT(ride_id) AS number_of_bike_type, rideable_type AS bike_type
FROM biketrips2022q1
GROUP BY bike_type; 

-- 10 Most used stations to start a trip
SELECT COUNT(ride_id) AS number_of_trips_started_at_station, start_station_name
FROM biketrips2022q1
GROUP BY start_station_name
ORDER BY number_of_trips_started_at_station DESC
LIMIT 10;

--  10 Most used stations to finish a trip
SELECT COUNT(ride_id) AS number_of_trips_finished_at_station, end_station_name
FROM biketrips2022q1
GROUP BY end_station_name
ORDER BY number_of_trips_finished_at_station DESC
LIMIT 10;

-- 10 Most used stations to finish a trip using DOCKED bike
SELECT COUNT(ride_id) AS Number_End_Stations_Docked_Bike, end_station_name AS Name_10_End_Stations_Docked_Bike
FROM biketrips2022q1
WHERE rideable_type = "docked_bike"
GROUP BY end_station_name
ORDER BY Number_End_Stations_Docked_Bike DESC
LIMIT 10;

-- 10 Most used stations to start a trip using DOCKED bike
SELECT COUNT(ride_id) AS Number_Start_Stations_Docked_Bike, start_station_name AS Name_10_Start_Stations_Docked_Bike
FROM biketrips2022q1
WHERE rideable_type = "docked_bike"
GROUP BY start_station_name
ORDER BY Number_Start_Stations_Docked_Bike DESC
LIMIT 10;

-- 10 Most used stations to finish a trip using CLASSIC bike
SELECT COUNT(ride_id) AS number_of_trips_finished_at_station, end_station_name
FROM biketrips2022q1
WHERE rideable_type = "classic_bike"
GROUP BY end_station_name
ORDER BY number_of_trips_finished_at_station DESC
LIMIT 10;

-- 10 Most used stations to finish a trip using ELECTRIC bike
SELECT COUNT(ride_id) AS number_of_trips_finished_at_station, end_station_name
FROM biketrips2022q1
WHERE rideable_type = "electric_bike"
GROUP BY end_station_name
ORDER BY number_of_trips_finished_at_station DESC
LIMIT 10;

SELECT COUNT(ride_id) AS Number_of_Usertype, member_casual AS Usertype
FROM biketrips2022q1
WHERE rideable_type = "docked_bike" && start_station_name = "Streeter Dr & Grand Ave"
GROUP BY member_casual;

SELECT COUNT(ride_id) AS Number_of_Usertype, member_casual AS Usertype
FROM biketrips2022q1
WHERE rideable_type = "docked_bike"
GROUP BY member_casual;

SELECT COUNT(ride_id) AS number_of_trips
FROM biketrips2022q1
