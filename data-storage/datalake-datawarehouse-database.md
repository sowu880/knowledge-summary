
[TOC]

# Data lake (数据湖)

主要功能用于 AI/BI分析 + 存储

A data lake is a system or repository of data stored in its natural/raw format, usually object blobs or files. 

A data lake can include structured data from relational databases (rows and columns), semi-structured data (CSV, logs, XML, JSON), unstructured data (emails, documents, PDFs) and binary data (images, audio, video). 


Support **Online Analytical Processing (OLAP)**. 

> OLAP: OLAP systems are typically used to collect data from a variety of sources. The data is then used to power a range of analytical use cases ranging from business intelligence and reporting (e.g., quarterly sales reports by store) to forecasting (e.g., predicting home sales for the next six months based on historical trends).


## Examples
The following are examples of technology that provide flexible and scalable storage for building data lakes:

* AWS S3
* Azure Data Lake Storage Gen2
* Google Cloud Storage

Other technologies enable organizing and querying data in data lakes, including:

* MongoDB Atlas Data Lake.
* AWS Athena.
* Presto.
* Starburst.
* Databricks SQL Analytics.

# Data Warehouse

主要用于 BI分析

A data warehouse is a system that stores **highly structured** information from **various sources**. Data warehouses typically store current and historical data from one or more systems. The goal of using a data warehouse is to combine disparate data sources in order to analyze the data, look for insights, and create business intelligence (**BI**) in the form of reports and dashboards.

**Extract, transform, load (ETL)** processes move data from its original source to the data warehouse. The ETL processes move data on a regular schedule (for example, hourly or daily), so data in the data warehouse may not reflect the most up-to-date state of the systems.

Support **Online Analytical Processing (OLAP)**. 

## Examples

* Amazon Redshift.
* Google BigQuery.
* IBM Db2 Warehouse.
* Microsoft Azure Synapse.
* Oracle Autonomous Data Warehouse.
* Snowflake.
* Teradata Vantage.

# Database

主要用于事务处理

A database is a collection of data or information. Databases are typically accessed electronically and are used to support **Online Transaction Processing (OLTP)**. Database Management Systems (DBMS) store data in the database and enable users and applications to interact with the data. The term “database” is commonly used to reference both the database itself as well as the DBMS.

## Key features:

* Security features to ensure the data can only be accessed by authorized users.
* ACID (Atomicity, Consistency, Isolation, Durability) transactions to ensure data integrity.
* Query languages and APIs to easily interact with the data in the database.
* Indexes to optimize query performance.
* Full-text search.
* Optimizations for mobile devices.
* Flexible deployment topologies to isolate workloads (e.g., analytics workloads) to a specific set of resources.
* On-premises, private cloud, public cloud, hybrid cloud, and/or multi-cloud hosting options.

## Examples

* Relational databases: Oracle, MySQL, Microsoft SQL Server, and PostgreSQL
* Document databases: MongoDB and CouchDB
* Key-value databases: Redis and DynamoDB
* Wide-column stores: Cassandra and HBase
* Graph databases: Neo4j and Amazon Neptune
## Transaction

A transaction is a single unit of work. If a transaction is successful, all of the data modifications made during the transaction are committed and become a permanent part of the database. If a transaction encounters errors and must be canceled or rolled back, then all of the data modifications are erased.

* Atomicity（原子性）：一个事务（transaction）中的所有操作，要么全部完成，要么全部不完成，不会结束在中间某个环节。事务在执行过程中发生错误，会被恢复（Rollback）到事务开始前的状态，就像这个事务从来没有执行过一样。
* Consistency（一致性）：在事务开始之前和事务结束以后，数据库的完整性没有被破坏。这表示写入的资料必须完全符合所有的预设规则，这包含资料的精确度、串联性以及后续数据库可以自发性地完成预定的工作。
* Isolation（隔离性）：数据库允许多个并发事务同时对其数据进行读写和修改的能力，隔离性可以防止多个事务并发执行时由于交叉执行而导致数据的不一致。事务隔离分为不同级别，包括读未提交（Read uncommitted）、读提交（read committed）、可重复读（repeatable read）和串行化（Serializable）。
* Durability（持久性）：事务处理结束后，对数据的修改就是永久的，即便系统故障也不会丢失。

# Comparation

||Database|Data Lake|Data Warehouse|
|--|--|--|--|
|Workloads|Operational and transactional|Analytical|Analytical|
|Data Type|Structured or semi-structured|Structured, semi-structured, and/or unstructured|Structured and/or semi-structured | 
|Schema Flexibility|Rigid or flexible schema depending on database type|No schema definition required for ingest (schema on read)|Pre-defined and fixed schema definition for ingest (schema on write and read)|
|Data Freshness|Real time|May not be up-to-date based on frequency of ETL processes|May not be up-to-date based on frequency of ETL processes|
|Users|Application developers|Business analysts, application developers, and data scientists|Business analysts and data scientists
|Pros|Fast queries for storing and updating data|1. Easy data storage simplifies ingesting raw data. 2. A schema is applied afterwards to make working with the data easy for business analysts. 3. Separate storage and compute. | The fixed schema makes working with the data easy for business analysts|
|Cons|May have limited analytics capabilities|Requires effort to organize and prepare data for use| 1. Difficult to design and evolve schema. 2. Scaling compute may require unnecessary scaling of storage, because they are tightly coupled
# Reference
[1. data-warehouse-and-data-lake](https://taoyuyin.gitee.io/2020/09/data-warehouse-and-data-lake/)

[2. data-lake-vs-data-warehouse-vs-database](https://www.mongodb.com/databases/data-lake-vs-data-warehouse-vs-database)