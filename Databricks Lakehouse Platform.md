# Databricks Lakehouse Platform

## Drawbacks of ADLS

* ADLS is not a database hence no ACID properties
* Job failure lead to inconsistent data.
* No support for Updates
* No support for versioning
* Data quality issues

## What is Delta Lake

> Delta Lake, an open source project developed by Databricks, enables building a **Lake House Architecture** with transactional capabilities  on top of data lakes.

**Important Points**

* Delta Lake is built on top of cloud storage like AWS S3, Azure Blob Storage, Google Cloud Storage

## Key Features of Delta Lake

1. ACID Transaction
2. Scalable Metadata handling
3. Time Travel (Data Versioning)
4. Schema Enforcement, & Evolution
5. Unified Batch and Streaming



## Data Warehouse vs Data Lake vs Data Lakehouse

| Feature                                 | Data Warehouse | Data Lake | Delta Lake |
| --------------------------------------- | -------------- | --------- | ---------- |
| ACID compliant transaction              | Yes            | No        |            |
| Define schema upfront                   | Yes            | NA        |            |
| Good at analyzing structured data       | Yes            | NA        |            |
| Work with unstructured, semi-structured | No             | Yes       |            |
| Expensive                               | Yes            |           |            |
| Support for AIML                        | No             | Yes       |            |

## Understanding Lakehouse Architecture

> A Data Lakehouse is a new paradigm in data engineering that combines the best features of data lakes and data warehouse.

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXdC8apjrPB4Cyc-wIvzd0vevA8C-72iwtrvOrYFJu7FZidt4sBFoTtBGP_n4vblhMdSqlXdMqxwkAWSQyAw2qccbcnMPkdCwmsWSaz0jEMSjUjHwyoepaLg2_1QfMJMXQ3YnyyQRn986jtGPkW50BMhlaiX?key=ifuSKoMy61kApFwZIJr_Qw)

## Understanding Delta Format

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXcHnyjjjtQBqfDEu63Fdaud8TOem4YXlmDoMzDQrdKb3FstleS-gR7_B5U_LFqOAX-Ws4frLnd3rPBhbypVyEJrBc21xkp_YbNNSGypgR-tFNwN1g6Ps7xWA9H06uN-MAdUamcE_3TAGblL8y8QYYBlmdBd?key=ifuSKoMy61kApFwZIJr_Qw)

