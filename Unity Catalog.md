# Unity Catalog

## Without Unity Catalog

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXffwF7DwV14IxsORqCIW1r_9coaUmoTOUv0I5-RdR-ts8j7McQkUknQGixT_j2XP8suXwHSAunT07_VK6tow6j8VdD8Mfzv-opkaqty8M-_sTl8OBf_DzCUxL4zq223e5R76vrdg77YBSdFqxUaFCT9Nn4?key=s_qMtqfg41hsjV15X24XGw)

## With Unity Catalog

> UC gives a unified governance layer layer to data with a single permission model with data sharing capabilities

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXdzSxpsGjunbYIn8873FGBZSL0kLkprrQXrl0Yhs5_ppc24giEul8DTpecOtiajEwpZ8aWOdtwIaBeq8zwj_r8Wb7G2XQLV4jzMs7og58z7WwdNlhIbjfNiEjcPMimklf7ZF_Rb40aUZAsJV5msduQHNv91?key=s_qMtqfg41hsjV15X24XGw)

* UC introduces centralized governance layer, serving as a master control center for 
  * User Management
  * Access Control
  * Metadata Storage

* All users, Databases, Tables and access permissions are concentrated within UC



## UC Object Model

![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXdQLUADp__kZNk64q1VCzyvHkgDXQAJZziOVafD0eKhCnRKArSArAzWvsUSPVaJV9iuI8jlKj08OItkd4YTmqhMAarl-Itm5D2hJBEcOKO_rT7pMNQlUwds8EEv7YW1_N-2hpJtMTZPtIc6TF2RASiVAcMK?key=s_qMtqfg41hsjV15X24XGw)

### Metastore

* Top level container in UC.
* Metastore, serving as the central container for all metadata and managed data objects like databases, tables, and permissions

## Catalog

* Multiple catalogs can exist within a Metastore, often organized on business units.
  * dev_catalog, qa_catalog, testing_catalog, adhoc_catalog

## Schemas / Databases

* Within a catalog, you can create one or more schemas, which are synonyms of databases

## Tables

* Inside schemas, you can create Managed Table, external tables, and views





## Hands-on - Setup and Configure UC

1. Create Access Connector for Databricks and link ADLS

**Databricks Accecss Connector**



![img](https://lh7-us.googleusercontent.com/docsz/AD_4nXdCv4Szh0anWrxFibnF2Ed0_75ZV91kvbMZ5u18ty5WlpUR04VhIoGhJryvrWdHOGxRmIidXm1lqJ6sw4wpv024cqc4Dxz6o2BuZYoqFBB97L_y_bDju1RE7Qafm8LbctYwA5ujsU_2Z4emFvhfe6tlbYNj?key=U2gx6_ime9XR6EAXOP0KSA)

/subscriptions/b3a34a45-4724-487f-a40f-d5138be20831/resourceGroups/azure-training-rg-main/providers/Microsoft.Databricks/accessConnectors/unity-catalog-access-connector



2, Grant Access to Access Connector for Azure Storage Account









