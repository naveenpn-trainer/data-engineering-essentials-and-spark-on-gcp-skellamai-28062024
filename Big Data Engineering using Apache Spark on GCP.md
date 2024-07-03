# Big Data Engineering using Apache Spark on GCP

## Introduction to Big Data and Hadoop 2.x

> Big Data refers to the data which is **large**(Volume), **fast** (Velocity) and **complex type of structured, semi-structured and unstructured** that becomes <u>difficult to store and process using a traditional processing system. (RDBMS)</u>

**Disadvantages of RDBMS**

1. RDBMS is designed to store structured
2. RDBMS is not designed to handle High Velocity Data (Schema on write)
3. RDBMS is vertical scaling

**Challenges of Big Data**

1. Storage : Distributed Storage System
2. Processing : MPP (Massive Parallel Processing Frameworks)

### Distributed System

> A DS is a collection of computer systems that are physically separated but are linked together as a single computer

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXeO1nSXKc3OqjKupkhsO2DcbLl55f1ULoK7AVKvolQO_5U3Gh58SEhMyEA2ARVvMCc6KfLzX8bDk7dNC-Sj2d8Lz_bGTRaq_HCVpv4izmRskJIC8EXz1y4nEnui9Pe44oHAQQqg1cB0ltTC7buKlGLMIEQ?key=ZDQI9yPkLwmZ3ZH_j9fetA)

### Hadoop

> Apache Hadoop is a software that allows us to **store and process large datasets** in parallel and distributed fashion.

* Apache Hadoop is written in Java

### Components of Hadoop

3 core components

1. Storage Layer : HDFS (Hadoop Distributed File System)
2. Data Processing Layer : Map Reduce (v2)
3. Resource Management Layer : YARN (Yet Another Resource Negotiator)

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXflCCwiT04UK8IRpuA3NDM4-Ag5fY7FdiPE9QxHRhfqs-7pntrcMyllhlmfdmorWsGUHADDI2-bF7_sL_BeUWVYV1NgoWc6sd23_oAdC3ut5Yr2FUJ5eAG-mY5OkpLPwK775lr03a4-DwCwFPuJPwOOrzlF?key=KG4XycolQz2vWFq2bNIfEQ)

### Hadoop Daemon Services

* In hadoop, a daemon service refers to a long running background process.
* There are 5 daemon services
  * NameNode
  * SecondaryName
  * DataNode
  * ResourceManager and 
  * NodeManager

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXespqZ9v5sQeG1FKuD-oa1NvAV0Nc6zCfP2sqmddM18BQnIr5hmzjS2ya2FTKmpGd7uZA6grpJYvP5ogf13swPVfABLlFhJdHoKgn8RPQfEl64kltGC2hejxbL2eX_ndjtzLo-YV2Y3PtGhBKALyZ7XLje3?key=KG4XycolQz2vWFq2bNIfEQ)

### Master and Slave Architecture

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXcx3xiQomrYfoWplXrNOOQetu99lqsVAfyIIJDkOPRXn-fQZqCYWcBQbQUv5WYQStbZCvv98BYDS_htfd_rs-K9wXdrbSVTW8rSK3Z9x80QaQtzac65tpFrnJrvNR6xk0I4U7Z-BczypYxB5BPOn98nZL-p?key=KG4XycolQz2vWFq2bNIfEQ)

1. NameNode : The NN stores metadata about the files and directories in the HDFS.

#### Map Reduce

> MR is a programming model to process the data in parallel in multiple machines.

* Map Reduce is deprecated alternat is Apache Spark 

####  HDFS (Hadoop Distributed File System)

* It is a primary storage component of Hadoop
* **GFS** Google FS

> HDFS is a **distributed** and **scalable file system** designed for storing very large files.



300 MB : The file will be broken down into blocks of size 128 MB

BlockA : 128 MB

BlockB : 128

BlockC : 54 MB

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXezcPZanQb3dtJQpq0ZinOfS3HozcXI4R75xXARjV2VJHqMjEluNMpQJxRoGiwR6HN3jHBC5o4l2l7HxEKExHpRy2ly5u1eq-SgsLdxQXEfpWHFevDLGDnTATXFOngkAUzpvtaKFoo0ob2C3fcXgbkGnpOh?key=KG4XycolQz2vWFq2bNIfEQ)

##### HDFS Architecture

![](C:\MyTrainings\data-engineering-essentials-and-spark-on-gcp-skellamai-28062024\imgs\Big Data Engineering using Apache Spark on GCP\HDFS Architecture-Page-1.drawio.png)

1. Client wants to save 30 MB of data (executes a command), the request is sent to NameNode.
2. NameNode responds to the client giving information of all the datanodes where the block has to be copied.
3. Client will copy the block into DataNode
4. TO Handle fault tolerance Hadoop uses replication i.e each block will be available as 3 copies in the cluster.

#### YARN (Yet Another Resource Negotiator) Resource Management

![](C:\MyTrainings\data-engineering-essentials-and-spark-on-gcp-skellamai-28062024\imgs\Big Data Engineering using Apache Spark on GCP\Cluster Manager.drawio.png)

When you are working with Hadoop.

1. NameNode UI : Browse the HDFS - http://localhost:50070/dfshealth.html#tab-overview
2. ResourceManager UI : Monitor the job - http://localhost:8088/cluster



**Steps to execute MapReduce**

1. Create file001.txt file002.txt Add some duplicate contents
2. Copy the files into HDFS

```
$> hdfs dfs -mkdir /workspace
$> hdfs dfs -put file001.txt file002.txt /workspace

$> cd /home/naveenpn/hadoop-2.10.2/share/hadoop/mapreduce
$> yarn jar hadoop-mapreduce-examples-2.10.2.jar wordcount /workspace /output_01
```

**Observation**

Open the ResourceManager UI and see the job progress

## Apache Spark

