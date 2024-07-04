# Apache Spark

- [ ] What is Apache Spark
- [ ] What is PySpark
- [ ] Communication between PySpark and Spark
- [ ] What makes Spark Faster (DAG and Data Sharing)
- [ ] Spark Eco system

![image-20240704092803246](C:\MyTrainings\data-engineering-essentials-and-spark-on-gcp-skellamai-28062024\imgs\Module 02 - Getting Started with Apache Spark\image-20240704092803246.png)

> Apache Spark is an **in-memory cluster computing framework** <u>designed to handle a wide range of big data workloads</u>

**Designed to handle a wide range of big data workloads**

1. Data Integration and ETL
2. High Performance Batch Computation
3. Real-time stream processing
4. Machine Learning Analytics

* The main features of spark is its **in-memory cluster computing framework**
* Spark is also built on top of Map Reduce 
* Google released two white papers to explain how their distributed computing works
  * GFS  --> HDFS
  * Map Reduce  --> Map Reduce (Hadoop)
* Apache Spark is natively written using Scala Programming



## What is PySpark

> PySpark is the Python API for Apache Spark (Distributed Processing Framework)

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXfqHY5d-Mz1DiYBqdQg_DpH_Yv8wlZf-w2Y1Kz-h9mf2Wz4FKHVsHGOXPXm1tmbUm-GPtB1RiEB3ppPclO0l6jLgUi_SPT0AWZP8bTOM5M69YXq48qei_oUayborah84YWaXg4Kr3WHzhzflAIdDNZNvPw?key=uvmlVet7-pBAx-jz0PuzLA)



* The PySpark communicates with Spark using **Py4J API**

**Assignment 01**

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXewq-jwTvSoqZcS91h2lUQ071bfAuvUScB58gAE3o8Opi0sBYZhPKD-ZLsefxx_QKm89ej4s_xbxbWhJCGFRC1ptBCkDFdUgU8Hf2QBCT7h0-jrwegIsbccbXjwWnQuDO3RYhklRaptm-dFuRvTcUAuuNo?key=uvmlVet7-pBAx-jz0PuzLA)



## How Spark is Faster

There are two reasons what makes spark faster

1. Advance DAG execution
2. Data Sharing

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXfPKFKc7cM0PmPOAZeMxHeq8hfylQFMRpyl7105QjCtD_hTjrJ76SINRENRqRi2f6iSgedO5uvJDHpaPizSnl0MQgK25chr5sotyAnxpaaWRC8LeJzlePV2IsP4TCIB2gZSz7Hy_FEF_zFQVQKB50sWcmNB?key=uvmlVet7-pBAx-jz0PuzLA)

![](C:\MyTrainings\data-engineering-essentials-and-spark-on-gcp-skellamai-28062024\imgs\Module 02 - Getting Started with Apache Spark\MapReduceExecutionFlow.drawio.png)



## Spark Ecosystem

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXf7Ew4mMpdh85KTTWh16D8hnGeU8HFEGfyFFtsyeZ0QQj2kNvmgj6cpCS3hLEXuDwCgh0YUfnsDylCuVtvuqq2rl9wYI28rJes5v1ip68wv17JH-6wrCmpv-20pQSOFI9T382x4GdpQceeKWI9nZAyjwbs?key=uvmlVet7-pBAx-jz0PuzLA)

1. **Spark Core** : Spark Core is the base engine for large-scale parallel and distributed data processing.
2. **Resource Management** : It is responsible for managing the cluster resources
3. **Storage** : To store the data for analysis
4. **Libraries** : 
5. **Programming Interfaces**

## Different ways to execute Spark/PySpark applications

1. Spark Interactive Shell
2. Databricks
3. EMR, HDInsights

### Spark Interactive Shell

> Spark Interactive Shell refers to the interactive command-line interface provided by Apache Spark

Spark provides two main interactive shells

1. Spark Shell (Scala)
   1. spark-shell

**Important Points**

* When we launch any spark application via spark interactive shell , it will create two objects
  * SparkContext (sc)
  * SparkSession (spark)
  * Every spark application you launch you will have one Web UI

1. PySpark Shell
   1. pyspark

**YARN Commads**

```
yarn application -list
yarn application -list -appStates FINISHED
```



## Two level of API

1. Low Level API (RDD's) : Deprecated
2. high Level API : Spark SQ

# RDD (Resilient Distributed Dataset)

> RDD are the building blocks of any spark application

* The fundamental data structure for apache spark for parallel processing is RDD's

**Partitions**

A partition is spark is a logical division of data stored on a node in the cluster

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXeve20SMofjsZMQDNvzRHnOndCEVbz-BjB60XGvQ9UZkg-8GSk-Ch9LbLS2I_goOa4-Rf0QM0mOa9DcqwX7oNnmzqkyGi7EPqEBgK9U8TdtMyuPZL33VARIC4ad9pJjCmF4YsBeoNGS-PNODnCJKN_jF4JV?key=uvmlVet7-pBAx-jz0PuzLA)

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXctN_AoCXQVuEnif8w8XIZZsnDY4T_WeOfLH7hYBEDw0or9OEy7oB56GURWauGV3FYaMaul1L49px9QXXOEesCSKmscYfqVRSOrFEQ0mZuQ_VWTMExNVtqj18WlXVgFslyEKee09yoq8E4hu0xkLSlcK5k?key=uvmlVet7-pBAx-jz0PuzLA)



## RDD Creations and Operations

There are two popular ways to create an RDD

1. Create an RDD from Collection

   ```
   L = list(range(1,11))
   numbers_rdd = sc.parallelize(L)
   print(type(numbe))
   ```

   

2. Create an RDD from External source



**Important Points**

1. All the methods to create an RDD is present inside SparkContext (sc)

## Assignments

**Assignment 01**



```java
public class SparkAPI {
	public String select(String name){
        return "Hello "+name
    }
    
    public String selectRequiredCols(Map<String,[]String> map, String key) {
        
    }
}
```

**PySparkAPICode**

```
class PySparkAPI:
	def select(self):
		message = new SparkAPI().select("Name")
		print(message)
	def selectRequiredCols(self, dictionary, key):
    	values = new SparkAPI().selectRequiredCols(dictionary,key)
    	return values
```

<u>User Application</u>

```
obj = PySparkAPI():
message = obj.select()
print(message)
```



**Assignment 02**

1. Explore the properties of RDD

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXewzJ4eXJIt0fSl-UWjFaj5UjDiZ7ba4FBJv-16vuKgvKxQ1uEeovfWTR7Kji40XTgbHa6u63nidqF2uPxsOS5R3_QuKVspi3XOISBWnwn31Hir-TBaMrkBBSkZFBqFlsRYVjIsJDiUlCGm82ln12vBpUE4?key=uvmlVet7-pBAx-jz0PuzLA)



