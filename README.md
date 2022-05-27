# Movies-ETL
Learning Extract Transform Load

## Overview
### Purpose
The Purpose of this assignment was to create a clean dataset for Hackathon participants. Data was gathered from both Wikipedia and Kaggle. Then we created a ETL pipeline from that data to store it in a SQL database. After extracting the data from various sources, we cleaned the data using Regular Expression (regex) and transform data using Pandas. Last step was to load the data with PostgreSQL.

## Results
#### Extracting the data
Following is the Wikipedia file data 

![image](https://user-images.githubusercontent.com/3753839/170623584-377846ce-755e-4a8c-9637-958c5d1e1b3c.png)



The Kaggle movie data had the following content
![image](https://user-images.githubusercontent.com/3753839/170623567-1b79c98c-fa57-4acb-9b7c-93f2a39bfcce.png)





Kaggle Ratings data had the following number of rows.

![image](https://user-images.githubusercontent.com/3753839/170623547-c96e1160-fbf0-4aca-9ac6-25c221bb77db.png)



#### Transforming the data.
##### Wikipedia Data
Wikipedia Movies dataframe was transformed to have 22 columns. The column names were changed to more meaningful and uniform ones. 

![image](https://user-images.githubusercontent.com/3753839/170623528-2e4b7266-d712-46e7-95aa-9bbaae565902.png)


![image](https://user-images.githubusercontent.com/3753839/170623511-34f207b3-725e-471e-ad67-e4971b4b3620.png)









###### Kaggle Data
Wikipedia Movies dataframe was then merged with Kaggle Movies dataframe . 
![image](https://user-images.githubusercontent.com/3753839/170623484-52b837bc-afab-4b89-96e3-5eab3bbe005b.png)



Wikipedia Movies dataframe was then merged with Kaggle Ratings dataframe . 
![image](https://user-images.githubusercontent.com/3753839/170623461-5426b844-4c4c-4ba2-a1bd-2e01e134dfe0.png)




#### Load


Next we loaded the data in Postgres

![image](https://user-images.githubusercontent.com/3753839/170623889-5d44f3a0-60ec-4d75-8608-7b6a3c07b63d.png)



![image](https://user-images.githubusercontent.com/3753839/170623898-2ec0318d-8753-4022-951d-40d56d3f5859.png)







## Summary:
The raw data from different sources were extracted cleaned and loaded in Postgres DB.
The dataset started with 7311 row in the Raw format which went through multiple iterations for clean up. 
Ultimately we are left with 6051 rows. 


###### Note: The assignment mentioned 6052 rows should be there after clean up. Initially after most of the clean up was done, there were 6052 rows in total, But then in 8.4.1 chapter, we have a cleaup exercise for release_date where we dropped one row

![image](https://user-images.githubusercontent.com/3753839/170623385-5bdb0d9f-0f8e-47d0-94e3-4d706ba86544.png)


![image](https://user-images.githubusercontent.com/3753839/170623390-e40f8a08-1ae6-4960-85e1-77e03894f334.png)





Which makes the count to be 6051.


