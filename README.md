# Project-6
New York City Taxi Passenger Dataset

Data set used:  https://www.kaggle.com/boltzmannbrain/nab

This data set contains details of number of passengers using nyc_taxi for a period of six months- from 07/01/2014 to 01/31/2015.The total taxi passengers have been divided into a 30 minutes bucket. There are five anomalies occurring in this dataset:

1.	NYC Marathon- 11/02/2014
2.	Thanksgiving- 11/27/2014
3.	Christmas- 12/25/2014
4.	New Year's Day- 01/01/2015
5.	Snow-storm- 01/26/2015 and 01/27/2015

Timestamp: Date and time when the taxi ride was taken

Value: Number of trips taken

1.	Data Cleaning

Loaded the dataset nyc_taxi.csv using pandas library

Performed data cleaning in data and removed the redundant records and null records and described the dataset

2.	Data Transformation

Modified the data type of ‘Timestamp’ column from string to date and set it as an index for pandas to treat it as a date.

Created a subset of the dataset for regular dates and the dates where anomaly was observed.

3.	Data Analysis

Analyzed the data and converted ‘timestamp’ column to date datatype.

Added an additional column called ‘event’ with a value of ‘0’ for all entries on regular days and with a ‘1’ for entries on special days.

Noted that that there are 293 entries in anomaly dataset and have a mean value of 10213. There are 10027 entries in the normal dataset with a mean value of 15281.

Calculated the outlier fraction and noted that outliers consisted about 2.9% of the entire dataset. 

Performed anomaly detection using random forest and isolation forest algorithms.

4.	Data Plotting

Plotted a graph of timestamp and number of taxi rides taken in the period of six months to visualize the dataset

Plotted a graph comparing the anomaly detection using random forest and isolation forest.

5.	Conclusion/Inferences

Noted that isolation forest gave better and accurate prediction as compared to random forest.

Isolation forest detected 515 outliers, local outlier detected 573 outliers and support vector machine detected 4267 outliers. Isolation forest algorithm has the maximum accuracy of 95% followed by local outlier which is 94% accurate. Hence noted that isolation forest has much better performance in detection of anomalies compared to other two algorithms
