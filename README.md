# Sparkify
## Udacity Datascience Nano Degree Capstone Project

Pyspark code that explores and cleans a large dataset, engineers features and labels, and trains a model to predict which "Sparkify" music service users are likely to cancel their subscriptions.

The code was developed with a Jupyter Notebook on the Apache Spark framework running on an AWS cluster.

### Motivation

The overall purpose of the project is to use the Apache Spark framework on an AWS cluster for training a machine learning model with a large dataset. The goal I hoped to accomplish while learing Spark, was to develop an accurate model for predicting when a "Sparkify" user is likely to churn.

### Blog Post

The full discussion of my project and code are [in this blog post on Medium](https://medium.com/@kennyflutes/using-apache-spark-to-predict-user-churn-c4a50a2520e8)



### What's Inside

- [Sparkify-Local.html](https://github.com/klrpdx/sparkify/blob/master/Sparkify-Local.html) : Jupyter Notebook with code running on my local machine with a small subset of the total dataset. This code was used to explore and clean the data and tryout engineering the features before moving to the AWS cluster.

- [SparkifyProject.html](https://github.com/klrpdx/sparkify/blob/master/SparkifyProject.html): Jupyter Notebook with code for running on the AWS cluster. Much of the initial code from the Sparkify-Local notebook ws copied here once I had it running locally on the smaller dataset. Additionally, this notebook splits the full dataset into train, validation, and test data; trains the model and evaluates the accuracy of the model.

### Credits

I relied on three main references during this project:

1. [The Apache Spark documentation and examples for linear regression](https://spark.apache.org/docs/2.1.1/mllib-linear-methods.html#logistic-regression)
2. [Susan Li's blog post on Machine Learning with PySpark](https://towardsdatascience.com/machine-learning-with-pyspark-and-mllib-solving-a-binary-classification-problem-96396065d2aa)
3. [Chang Hsin Lee's blog post on turning python functions into PySpark](https://changhsinlee.com/pyspark-udf/)


### Libraries Used

- pyspark.sql.SparkSession
- pyspark.sql.functions
- pyspark.sql.types
- pyspark.ml.feature: VectorAssembler, StandardScaler
- pyspark.storagelevel
- pyspark.ml.classification.LogisticRegression
- pyspark.ml.evaluation.BinaryClassificationEvaluator
- pyspark.ml.tuning: CrossValidator, ParamGridBuilder
- pandas
- matplotlib
