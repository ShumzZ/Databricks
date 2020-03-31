
#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/1436982558090289/5214049462728440/latest.html)

### Youtube comments analysis - NLP, identify potential cat/ dog owners

- General description:
  - In this notebook, all analyses and modelings are based on a dataset of user comments gathered on Youtube videos related to animals or pets. The goal is to identify cat / dog owners based on these comments, find out the topics important to them, and then identify video creators with the most viewers that are cat or dog owners.
  
- Data description:
  - The dataset consists of over 5 million records of comments, (~ 240MB compressed); it has been collected and accessible at:
https://drive.google.com/file/d/1o3DsS3jN_t2Mw3TsV0i7ySRmh9kyYi1a/view?usp=sharing
  - The dataset file is comma separated, with a header line defining the field names:
    - creator_name: Name of the YouTube channel creator;
    - userid: Integer identifier for the users commenting on the YouTube channels;
    - comment: Text of the comments made by the users.

- Project outline:
  - PART 0: ETL on 5M of comments;
  - PART I: constructed training data by naive labeling and resampling;
  - PART II, built pipeline for feature engineering (tokenization, normalization, stemming, vectorization etc.);
  - PART III: 
      - estimated and evaluated different classifiers(logistic regression, random forest and GBT) through training and hyper parameter tuning
      - classified the rest of the unlabeld comments using the optimal model
  - PART IV: 
      - identified topics important to cat and dog owners (using latent topics / LDA model)
      - formulated recommendations to monetize the audience under different channels.
      - future work, better labelling through analysis of the capitalization, explicit breed info mentioned in the comment, other references to cats/ dogs, cats/ dogs products and even emoji
      
      
- Framework / Language/ Libraries/ Others:
  - Spark APIS (both RDD based API and datafram based API) 
  - Python
  - PySpark, pandas, matplotlib, nltk
  - Basic Linux knowledge and CLI commands

#### PS: all codes tested on runtime version: 5.5ML (includes Apache Spark 2.4.3, Scala 2.11) and 6.4ML (includes Apache Spark 2.4.5, Scala 2.11)

#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/1436982558090289/5214049462728440/latest.html)
