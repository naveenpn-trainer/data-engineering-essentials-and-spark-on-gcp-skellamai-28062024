# Exploring Databricks using GCP

- [x] What is Databricks
- [x] Hosted on various Cloud providers
- [x] Databricks Architecture (Control Plane and Compute Plane / Data Plane)
- [x] Databricks Components (Workspaces, Notebooks, Compute, Catalog, Workflows, Job Runs)
- [x] **Hands on ** - Magic Commands
- [x] **Hands on ** - Databricks Utilities (FS, Widgets, )
- [x] **Hands on ** - Databricks Notebook Commands

> Databricks is a cloud based **unified analytics platform** designed for Data Engineering, Data Analyst and Data Science

Databricks can be hosted on different cloud providers

1. Azure
2. AWS
3. GCP

## Databricks Architecture

Databricks consists of two components:

1. Control Plane
2. Compute / Data Plane

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXeTv8B45w9C4jMWB43mwD72XPj8NxWF5IpxjM8lEElzXdMMQoD2bX6yOEveY3BDiPzN33kyhyh8vs2CDKL0sifOf5pi3ajFdrm0FHbGTN3l7n5uVzsAR8UJpxwDxwjF2f7-lmgRnwT3YvSddEXnEL-5wYI?key=aJiAWgzYP3udRlKejSDPqw)

**Control Plane**

1. The Control Plane consists of backend services that databricks manages in its own cloud account.
2. Most data isn't stored here,

**Compute Plane**

* The Data Plane is where you data is processed.



**DBFS (Databricks File System**

## Databricks Components

1. **Workspace / Notebook**
   - A web based interface where we write code
   - Manage notebooks using UI
   - Import and Export Notebooks
   - Notebook supports version control with Azure DevOps, BitBucket, GitHub
   - Support various types of visualizations 

2. **Compute** (All Purpose and Job Cluster)

   | All Purpose / Interactive Cluster  | Job Cluster               |
   | ---------------------------------- | ------------------------- |
   | Created Manually by users, AWS CLI | Created by Job            |
   | Expensive to run                   | Cheaper to run            |
   | Persistent                         | Isolated just for the job |
   | Autoscale                          | Autoscale                 |

   

3. Instance Pools : 

4. Workflows

5. Catalog







## Certification

* https://www.databricks.com/learn/certification/data-engineer-associate
* https://learn.microsoft.com/en-us/credentials/certifications/azure-data-engineer/?practice-assessment-type=certification
* https://aws.amazon.com/certification/certified-data-engineer-associate/



