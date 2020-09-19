# User-Services-Analysis
Cohort Analysis Problem Statement

Data Set
•	search_cohort_raw.csv

Task
You have 2 columns - userId and the day on which they searched. 
If a user has done search on two different dates, there will be 2 entries for this user in the sheet. 

The goal of this exercise is to look at returning users. How many users come back on day2, day3 and so on after he did search on day 1. 

This kind of analysis is called cohort analysis. 

Your goal is to build a cohort table with this long csv. 
The end result should be able to tell us what percentage of the users come back from day 1 of their search to day 7.

----------------------------------

Distance Finder Problem Statement

You will be provided with a dataset of the geo-locations of our field relationship manager which we capture via their android phones on which the Field CRM app runs. The data set contains their locations at various time snapshots. 

Data Set
•	frm_locations.csv

This dataset contains a CSV which is a set of events which we receive of 4 columns - executive identifier,  time at which the location is captured, latitude and longitude. 

You are required to get the total distance covered by an executive per day in kms. 
As pointed out the geo-location comes from the CRM app running on the android phones of our field executives. So there is one problem. The android location service sometimes sends abrupt location points. So you should be able to see some random points which do not look like the movement pattern of the executive. You need to filter out these points. 

The resulting dataframe should look something like this: (The values are in kilometers travelled per executive by the end of the day)

Important Notes 
•	You are only required to compute great circle distance and you can assume 1 degree = 110km in both directions. If you are ambitious you can calculate the on road distance using a Maps provider. 
•	You should achieve this with just DataFrame manipulations using Pandas/SQL.
•	Do not use loops to achieve this. 
•	Make assumptions as required. 

-------------------------------------

Spatial Analysis

You will be provided with 3 datasets - one containing locations of bus stops in bangalore city, other containing health establishments and the third containing restaurants. Let’s say a user wants to set a preference criteria among these three. A user Raj would assign 0.5 weightage for restaurants, 0.4 for health establishments and 0.1 for educational establishments. Let assume that the weights add up to 1.0. We would like to show the top 5 locations on the Bangalore map (with ranking) where X can choose to relocate with his preference weights. 

You are expected to make a function that takes preference weights and returns the ranked points where he can choose to relocate in the city. In Jupyter notebook on running this function we would like to get the points visualized on a map. 

Data Set 
- bus_stops.csv 
This hypothetical dataset is a CSV which contains 3 columns. bus stop id, lat, lng these represent bus stop geo locations in Bangalore 

- restaurants.csv 
This hypothetical dataset is a CSV which contains 3 columns. restaurant id, lat, lng these represent restaurant geo locations in Bangalore 

- hospitals.csv 
This hypothetical dataset is a CSV which contains 3 columns. hospital id, lat, lng these represent hospital geo locations in Bangalore 

Important Notes 
●  Make assumptions as required. 
●  These points lie within the boundaries of Bangalore. However, the dataset is artificially created  and does not represent real locations of anything. So do not worry if the outputs do not make logical sense in real geographical locations. 
