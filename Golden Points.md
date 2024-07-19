# Golden Points

* When you launch spark interactive shell two objects will be created

  * SparkContext (sc)
  * SparkSession (spark)

* All the methods to create RDD is present inside SparkContext

  * The primary interface to created DataFrame is dataFrameReader

    ```
    dfr = spark.read
    ```

    

* Can you name some of the methods presents inside DataFrameReader
  * .csv
  * .json
  * .parquet
  * .jdbc
* Methods present inside DF
  * .select
  * .filter
  * .groupBy
  * .count
  * .write
  * .show
  * .display
* All the functions is part of what package
  * from pyspark.sql.functions import col, ltrim, lower, sum, min, max, avg, 