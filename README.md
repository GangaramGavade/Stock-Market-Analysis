Historic Data Analysis---
The motive of the project is to analyse the historic sector
wise data and get key insights through visualizations so that investors can make better decisions while buying stocks. 
The project also encompasses real time stocks data fetched through Yahoo Finance API where investors would notify stocks updates through message. 
This project makes use of python and cloud technologies. 

Real Time Notification---
Second part of our project is real-time fluctuation of data. through Y finance we fetch every one minutes data .for fetching that data 
and load into s3 bucket. We use one lambda function and scheduled that lambda function for every one hour. so that every one hour stock data 
automatically load in s3 bucket from s3 bucket data load into Hdfs.in pypark we start spark session in that we write SQL query for generating KPI 
through SQL  query we generate 8 KPI. output of this 8 KPI written to s3 bucket as a csv file. 
whenever file is uploaded on s3 bucket at that time lambda function triggered. Lambda function program consist of reading  a data from s3 bucket. 
decoding that data and publish that data to end user through sns. In Sns service we create one topic and subscriber 
