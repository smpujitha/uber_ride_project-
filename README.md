# uber_ride_project-
this project is about the analysis of uber _ride 
Uber Ride Analysis – NCR Region
##Overview:

This project performs an Exploratory Data Analysis (EDA) on Uber ride booking data from India's National Capital Region (NCR). The objective is to uncover customer behavior, ride demand patterns, vehicle preferences, wait-time trends, cancellation reasons, and customer satisfaction metrics.

Using Python, Pandas, Matplotlib, and Seaborn, the analysis transforms raw ride-booking data into actionable business insights through data cleaning, feature engineering, statistical exploration, and visualization.
##code:
import pandas as pd
import numpy  as np
import matplotlib.pyplot as plt
import seaborn as sns 
dataset:
uber_df=pd.read_csv('ncr_ride_bookings.csv')
** the dataset is downloaded from kaggle.com 
## Objectives

The analysis aims to answer the following questions:

* Which vehicle categories are most preferred by customers?
* During which hours is ride demand highest?
* What factors contribute to ride cancellations and incomplete trips
* How do customer and driver ratings vary across vehicle categories?
* What payment methods are most commonly used?
* How does ride distance influence booking value?

## Dataset Information

The dataset contains ride booking records from the NCR region and includes:

| Feature                | Description                            |
| ---------------------- | -------------------------------------- |
| Vehicle Type           | Category of Uber service               |
| Date & Time            | Booking timestamp                      |
| Pickup Location        | Ride starting point                    |
| Drop Location          | Ride destination                       |
| Ride Distance          | Distance traveled (km)                 |
| Booking Value          | Fare amount (₹)                        |
| Booking Status         | Completed, Cancelled, Incomplete, etc. |
| Avg CTAT               | Customer Turn Around Time              |
| Avg VTAT               | Vehicle Turn Around Time               |
| Customer Rating        | Rating given by customer               |
| Driver Ratings         | Rating given by driver                 |
| Payment Method         | Payment mode used                      |
| Incomplete Ride Reason | Reason for ride failure                |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook (Anaconda)
* using seaborn and matplotlib for analysis i used
       *boxplot
       *countplot
       *violinplot
       *histplot
       *scatterplot
       *swarmplot
       *lineplot
      

---

## Data Preprocessing

The following preprocessing steps were performed:

* checked for  duplicate records-no such duplicate records found
* Identified missing values-using isnull().sum 
* Filled numerical missing values using median imputation
* Filled categorical missing values using mode imputation
* Converted time-related columns into useful analytical features
* Created a custom DAY segment:

| Time Range    | Category  |
| ------------- | --------- |
| 12 AM – 10 AM | Morning   |
| 10 AM – 3 PM  | Afternoon |
| 3 PM – 7 PM   | Evening   |
| 7 PM – 12 AM  | Night     |






