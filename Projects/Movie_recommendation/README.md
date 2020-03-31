#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/2352903793671506/5214049462728440/latest.html)

### MovieLens Dataset - OLAP analysis and Recommendation system

All the analyses and modelings in this notebook are based on the [MovieLens dataset](https://grouplens.org/datasets/movielens/latest/). As stated in the description, the datasets consists of a `small` version and a `full` version, the following sections were run against the `full` dataset and some of the commands can be time consuming even if the processes are parallelized by Spark under the hood. For illustration purposes, if desired, substitude with the `small` dataset.

- Data description:
  - Small: 100,000 ratings and 3,600 tag applications applied to 9,000 movies by 600 users. Last updated 9/2018.
  - Full: 27,000,000 ratings and 1,100,000 tag applications applied to 58,000 movies by 280,000 users. Includes tag genome data with 14 million relevance scores across 1,100 tags. Last updated 9/2018.

- Project outline:
  - PART 0: ETL to load the data into Databricks instance
  - PART I: OLAP analysis, mainly driven by a few questions;
  - PART II: Build a backend of a movie recommendation system:
    - applied matrix factorization collaborative filtering, and adopted Alternating Least Squares (ALS) algorithm to parallelize the computation of user matrix and item matrix;
    - fine-tuned the hyper parameters via cross-validation and visualization of learning curve;
    - recommended top 10 movies for any given user

- Framework / Language/ Libraries/ Others:
  - Spark APIS (both RDD based API and datafram based API) 
  - Python
  - PySpark, pandas, matplotlib
  - Basic Linux knowledge and CLI commands
  
#### PS: all codes tested on runtime version: 5.4 ML (includes Apache Spark 2.4.3, Scala 2.11) and 6.4 (Spark 2.4.5 Scala 2.11)

#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/2352903793671506/5214049462728440/latest.html)
