# Exploring Spark SQL and DataFrame API

> **Spark SQL** is one of the module in the spark eco system, to analyze structured and semi structured

![image-20240706091223103](C:\MyTrainings\data-engineering-essentials-and-spark-on-gcp-skellamai-28062024\imgs\Exploring Spark SQL and DataFrame API\image-20240706091223103.png)

You can interact with Spark SQL using three ways

1. SQL
2. DataFrame API (Python + Scala)
3. Dataset API (Scala)

In any Spark Application you perform three steps.

1. Load the data 

2. Process the data

3. Write the result to different destination systems

   

![](C:\MyTrainings\data-engineering-essentials-and-spark-on-gcp-skellamai-28062024\imgs\Exploring Spark SQL and DataFrame API\What is Spark DataFrame (1).png)

> A DataFrame is distributed Collection of data organized into named columns.

* It is similar to a tables in relational database, they store data in columns and rows i.e. DataFrames have schema
* Provides operations to Filter, Group, Aggregate etc.
* Can be created from different source like HDFS, Hive, CSV, JSON, Cassandra etc.