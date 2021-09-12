# **Google Data Analytics - Capstone Project**
<img src="bellabeat.jpg" alt="drawing" width="300"/>


## Ask

1. How many users does the data include?
2. How many days of data do we have?
3. What are the different metrics available across all datasets
4. What is the daily activity profile of each user?
5. What is the overall activity profile of each user?<br>
These are some of the questions we are trying to answer in this study.

## Prepare

- The dataset used for this study is available on Kaggle - https://www.kaggle.com/arashnic/fitbit
- This dataset has 33 unique users and 31  days of their data.
- The tables that we are using in this study are as follows:
 - Daily Activity Data
 - Heartrate in seconds
 - Minutes METs
 - Sleep Day
 - Weight Loginfo


## Process

Step 1: Loading all data in csv format in a Python jupyter file.
Step 2: Changing the datatype of column "activity day" From "Object" to "Datetime".
Step 3: Since the "Heartrate" and "METs" data file is too big I have stored it in pickle format and then used .pkl file for further ananlysis. (to avoid long run times on subsequent reloads).
Step 4: "Activity date" column is named differently in different tables. To make it easier to join the column name has been renamed.
Step 5: Then the values have been sorted in ascending order first by "Id" column and then by "activity date" column.
Step 6: The heartrate and Met data is in second and minute level so they have been converted to daily level to activity date.
Step 7: Then the above tables are merged into a new dataframe using a left join on column "Id" and "ActivityDate" 
Step 8: Then dataframe is sorted in ascending order again first by id and the activity date columns.
Step 9: Now this dataframe, which is at a daily level is ready to perform analysis.

## Analyze

To help us understand how active are the users (or if they use the product on a daily basis)
    - We bin the total steps in 4 buckets - Sedentary/Light/Fairly Active/Very Active (4 buckets based on 25th percentile, median, 75th percentile)
    - Then we look at daily percent of users in each bucket
Then look at average percent of users across all days.

From the Data provided we see that there is not enough data on sleep and weightlog and if the company wants to focus on those features they must gather more data of the same.
Which also means that users are not using the smart watch to track their sleep and weight actively.

From the plot it is clear that all of the users are using the smart watch to track their steps/activity on daily basis.
We also see there is a sudden spike in sedentary active which could be because of an outlier.
Otherwise there is no clear pattern which can suggest that only very active or fairly active people tend to use the smart watch more than the others.


## Share


## Act
