# Databricks

A collection of projects I have done and/or quick how-to guides I have complied over time on [Databricks](https://databricks.com/)\
If you are utilizing Spark for data analytics and data science projects and would like some awesome built-in visualization tools and features, check out the community (free) version [here](https://community.cloud.databricks.com/login.html)

Projects:

- Inference pipeline deployment to AWS SageMaker for real-time prediction

  Project outline: (for details see [project notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/3490305292750161/5214049462728440/latest.html))
  - PART 0: set up environment (Databricks, AWS, Docker, etc.)
  - PART I: Feature engineering, model training and logging
    - Process features and train models(in particular a text classification model) using Spark
    - Log / save trained model and construct inference pipeline (pre-processing, prediction, post-processing) in Mleap - compatible format using Mlflow
  - PART II: Deploy to AWS SageMaker (from scratch using boto3 and concise implementation using mlflow) for real-time prediction requests.


- YouTube user comments analysis\
  \- Identify pet owners from Youtube video comments

  Project outline: (for more details see [project notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/1436982558090289/5214049462728440/latest.html))
  - PART 0: ETL on 5M of comments;
  - PART I: constructed training data by naive labeling and resampling;
  - PART II, built pipeline for feature engineering (tokenization, normalization, stemming, vectorization etc.);
  - PART III:
    - estimated and evaluated different classifiers(logistic regression, random forest and GBT) through training and hyper parameter tuning
    - classified the rest of the labeled comments using the optimal model
    PART IV:
    - identified topics important to cat and dog owners (using latent topics / LDA model)
    - formulated recommendations to monetize the audience under different channels.
    - future work, better labelling through analysis of the capitalization, explicit breed info mentioned in the comment, other references to cats/ dogs, cats/ dogs products and even emoji



- MovieLens dataset OLAP analysis\
  \- OLAP analysis and Recommendation system

  Project outline: (for details see project page or [project notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/2352903793671506/5214049462728440/latest.html))
  - PART 0: ETL to load the data (27M ratings and 1M tag applications applied to 58K movies by 280K users) into Databricks instance
  - PART I: OLAP analysis, mainly driven by five questions;
  - PART II: Build a backend of a movie recommendation system:
    - applied matrix factorization collaborative filtering, and adopted Alternating Least Squares (ALS) algorithm to parallelize the computation of user matrix and item matrix;
    - fine-tuned the hyper parameters via cross-validation and visualization of learning curve;
    - recommended top 10 movies for any given user



- SF crime incidents report\
  \- EDA, visualization and time series modeling

  Project outline: (for details see [project notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/3431157766323343/5214049462728440/latest.html))
  - PART 0, ETL on 200M rows of raw data and data preprocessing;
  - PART I, EDA, mainly driven by the 7 questions, and associated visualization are focused on different aspects of crime incidents and designed to provide insights on these crimes and better communicate the EDA findings to general public as well as SFPD;
  - PART II, additional advanced visualizations and time series analysis:
    - create interactive visualization clustering map and Choropleth map to provide more insights
    - use ARIMA with seasonality to model number of crime incidents in SF downtown, formulating resource allocation advices for SFPD.




Note: All the .ipynb files are converted from Databricks directly.\
If they can not be rendered properly here on Github, please either click the Databricks notebook link, or copy and paste the .ipynb link to [nbviewer](https://nbviewer.jupyter.org/)
