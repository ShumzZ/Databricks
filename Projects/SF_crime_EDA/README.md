#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/3431157766323343/5214049462728440/latest.html)

%md
### SF crime incidents report - exploratory data analysis (EDA), visualization and time series modeling

- Data description
The SFPD provides public access to its well-maintained [crime incidents reports](https://data.sfgov.org/api/views/tmnf-yvry/rows.csv?accessType=DOWNLOAD) to empower use of data, as an important step towards the goal of improving the quality of life and work for SF residents and visitors. All the analyses and modelings in the notebook are based on historical crime data collected from 2003 to 2018.05 (~200 mill rows of records).
  
- Project outline:
  - PART 0, ETL on 200M rows of raw data and data preprocessing;
  - PART I, EDA, mainly driven by the 7 questions, and associated visualization are focused on differenct aspects of crime incidents and desinged to provide insights on these crimes and better communicate the EDA findings to general public as well as SFPD;
  - PART II, additional advanced visualizations and time series analysis:
    - create interactive visualization clustering map and Choropleth map to provide more insights 
    - use ARIMA with seasonality to model number of crime incidents in SF downtown, formulating resource allocation advices for SFPD.

- Framework / Language/ Libraries/ Others:
  - Spark APIS (both RDD based API and datafram based API) 
  - Python
  - PySpark, pandas, matplotlib, geopandas, shapely, folium, statsmodels, pmdarima
  - Basic Linux knowledge and CLI commands

#### PS: all codes tested on runtime version: 5.5 LTS (includes Apache Spark 2.4.3, Scala 2.11) and 6.4ML (includes Apache Spark 2.4.5, Scala 2.11)

#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/3431157766323343/5214049462728440/latest.html)
