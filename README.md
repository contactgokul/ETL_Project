# ETL_Project

This ETL project is done in a group by Gokul & Bharat

We followed the ETL concept as below:

(E)xtraction
------------
We used below datasets from public platforms:
1. airlines_code.csv
Downloaded airlines.csv from https://www.kaggle.com/usdot/flight-delays#airlines.csv and rename it to “airlines_code.csv”

2. airlines_delay.csv 
Downloaded from Kaggle. The file size of this file is 500+MB, not able to upload to GitHub. Download “flights.csv” from “https://www.kaggle.com/usdot/flight-delays#flights.csv” and rename it to “airlines_delay.csv” 

3. airline_safety.csv
Downloaded from https://aviation-safety.net/wikibase/

4. airlines_pass_stats.csv (passenger statistics)
Downloaded from https://data.world/sanfrancisco/rkru-6vcg

All our data was based on several airlines information (including US Carriers) spread across several years. These were the datasets we could find.

(T)ransformation
----------------
Our first step is cleaning each csv file to extract data for only US Carriers. We loaded each csv file, read it and removed the unwanted columns and retained only the required columns as part of Data Clean up.

Final dataset (dataframe) consists of details of only US Carriers which is the Transformed dataset. We created this dataframe based on common id “IATA Code” (airlines code)

(L)oad
------
The last step is to transfer our final output into a mysql Database. 

We created a database in MYSQL “ETL_PROJECT” with respective table “US_AIRLINES_STATS” to match the columns from the final Panda’s Data Frame. 

Using MYSQL in Pandas the dataframe is loaded into the database as final result. Same can be retrieved from Pandas and MYSQL.