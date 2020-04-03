#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/3490305292750161/5214049462728440/latest.html)

### Inference pipeline deployment (to AWS SageMaker)

- General description:
  Partially following examples from Databricks documentations [notebook1](https://docs.databricks.com/applications/mlflow/tracking-examples.html#train-a-pyspark-model-and-save-in-mleap-format) and [notebook2](https://docs.databricks.com/applications/mlflow/mleap-model-deployment-on-sagemaker.html), and AWS SageMaker documentations [notebook3](https://github.com/awslabs/amazon-sagemaker-examples/blob/master/advanced_functionality/inference_pipeline_sparkml_blazingtext_dbpedia/inference_pipeline_sparkml_blazingtext_dbpedia.ipynb) and [notebook4](https://github.com/awslabs/amazon-sagemaker-examples/blob/master/advanced_functionality/inference_pipeline_sparkml_xgboost_car_evaluation/inference_pipeline_sparkml_xgboost_car_evaluation.ipynb), the goal of this project is to demonstrate the main steps to deploy a trained inference pipeline to AWS SageMaker:
  - process features and train models(in particular a text classification model) using `Spark`
  - log / save trained model and construct inference pipeline (pre-processing, prediction, post-processing) in `mleap`- compatible format using `mlflow`
  - deploy to AWS SageMaker for real-time prediction requests.
  
- Data description:
  - The modeling trainning section uses the [20 Newsgroups dataset](http://kdd.ics.uci.edu/databases/20newsgroups/20newsgroups.html) which consists of articles from 20 Usenet newsgroups, for details see the link above. Simply put, there are 20000 messages in total, taken from 20 newsgroups, which can be interpreted as 'topics', or 'labels' (such as `rec.autos`, `sci.electronics`, `talk.politics.guns`, etc.), each observation consists of two columns: `text` and `topic`.
  - Note: If using Databricks, this dataset is **pre-loaded** into Databricks in parquet format under path `file:/dbfs/databricks-datasets/news20.binary/data-001/training`; otherwise, the data is accessible at [this link](http://kdd.ics.uci.edu/databases/20newsgroups/20_newsgroups.tar.gz) (17.3M; 61.6M uncompressed)

- Project outline:
  - PART 0: set up environment (Databricks, AWS, Docker, etc.)
  - PART I: Feature engineering, model training and logging
  - PART II: Deploy to AWS SageMaker (from scratch using `boto3` and concise implementation using `mlflow`)
      
- Framework / Language/ Libraries/ Others:
  - Spark APIS (datafram based ML API `spark.ml`) 
  - Python
  - PySpark, mleap, mlflow, boto3, sagemaker
  - Basic Linux knowledge and shell scripts

#### PS: all codes tested on runtime version: 6.4ML (includes Apache Spark 2.4.5, Scala 2.11)

#### For better formatting and visualization, please check out the project/ notebook at:<br>
[Databricks notebook link](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6227236730275197/3490305292750161/5214049462728440/latest.html)


Note: The .ipynb file is converted from Databricks directly.
If they can not be rendered properly here on Github, please copy and paste the link to [nbviewer](https://nbviewer.jupyter.org)

