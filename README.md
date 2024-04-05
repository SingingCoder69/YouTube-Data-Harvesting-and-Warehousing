# YouTube Data Harvesting and Warehousing.

## Introduction 

* YouTube, the online video-sharing platform, has revolutionized the way we consume and interact with media. Launched in 2005, it has grown into a global phenomenon, serving as a hub for entertainment, education, and community engagement. With its vast user base and diverse content library, YouTube has become a powerful tool for individuals, creators, and businesses to share their stories, express themselves, and connect with audiences worldwide.

* This project extracts the particular youtube channel data by using the youtube channel id, processes the data, and stores it in the MongoDB database. It has the option to migrate the data to PostgresSQL from MongoDB then analyse the data and give the results depending on the customer questions.

* I developed this project as a YouTube data harvesting and warehousing tool to extract, transform, and load (ETL) YouTube data into a MongoDB database and then migrate it to a PostgreSQL database for further analysis and querying. I utilized the YouTube Data API to collect information such as channel details, playlists, videos, and comments. This tool provides users with functionalities to view and analyze the harvested data through a Streamlit web interface and perform various queries using SQL.


## Developer Guide 

### 1. Tools Install

*Python (version 3.0 or higher)
*MongoDB
*PostgreSQL
*Streamlit

### 2. Requirement Libraries to Install

*google-api-python-client
*pymongo
*psycopg2
*pandas
*streamlit
 
### 3. Import Libraries

*import googleapiclient.discovery
*import pymongo
*import psycopg2
*import pandas as pd
*import streamlit as st


### 4. E T L Process
The ETL process involves extracting data from the YouTube Data API, transforming it into a suitable format, and loading it into MongoDB and PostgreSQL databases. This process is divided into several functions, including fetching channel information, retrieving video details, collecting comments, and migrating data to SQL tables.

#### a) Extract data
The exploratory data analysis (EDA) process involves analyzing the harvested YouTube data to gain insights and identify patterns. In this project, I facilitated the EDA through Streamlit, a web application framework for Python. Users can interact with the data using a user-friendly interface, visualize data using charts and graphs, and perform SQL queries to extract specific information.

* Extract the particular youtube channel data by using the youtube channel id, with the help of the youtube API developer console.

#### b) Process and Transform the data

* After the extraction process, takes the required details from the extraction data and transform it into JSON format.

#### c) Load  data 

* After the transformation process, the JSON format data is stored in the MongoDB database, also It has the option to migrate the data to MySQL database from the MongoDB database.

### 5. E D A Process and Framework

#### a) Access MySQL DB 

* Create a connection to the MySQL server and access the specified MySQL DataBase by using pymysql library and access tables.

#### b) Filter the data

* Filter and process the collected data from the tables depending on the given requirements by using SQL queries and transform the processed data into a DataFrame format.

#### c) Visualization 

* Finally, create a Dashboard by using Streamlit and give dropdown options on the Dashboard to the user and select a question from that menu to analyse the data and show the output in Dataframe Table.


## User Guide

#### Step 1. Data collection zone

* Search **channel_id**, copy and **paste on the input box** and click the **Get data and stored** button in the **Data collection zone**.

#### Step 2. Data Migrate zone

* Select the **channel name** and click the **Migrate to MySQL** button to migrate the specific channel data to the MySQL database from MongoDB in the **Data Migrate zone**.

#### Step 3. Channel Data Analysis zone

* **Select a Question** from the dropdown option you can get the **results in Dataframe format**.




