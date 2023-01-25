# Azure Data Lake Storage 
Azure Data Lake Storage or a short name Data Lake is a system or repository of a huge quantity of data in a structured or unstructured form that is stored in its natural format

Azure Data Lake Storage Gen2 is a set of capabilities dedicated to big data analytics, built on Azure Blob Storage.

It is a part of the Microsoft Azure public cloud platform, which is a cloud platform that supports big data storage and analytics of any kind and size.

Each data lake service underneath always has a **container**.

That container is very often called a **file system** and just like any file system it has folders and files within it which is fully scalable and secure that supports **HDFS semantics** while working with the **Apache Hadoop ecosystem**.

Some notable features of Azure data lake storage Gen2 are as follows

* **Hadoop compatible access**: Data Lake Storage Gen2 allows you to manage and access data just as you would with a Hadoop Distributed File System (HDFS). The new ABFS driver (used to access data) is available within all Apache Hadoop environments. These environments include Azure HDInsight, Azure Databricks, and Azure Synapse Analytics.

* **A superset of POSIX permissions**: The security model for Data Lake Gen2 supports ACL and POSIX permissions along with some extra granularity specific to Data Lake Storage Gen2. Settings may be configured through Storage Explorer or through frameworks like Hive and Spark.

* **Cost-effective**: Data Lake Storage Gen2 offers low-cost storage capacity and transactions. Features such as Azure Blob Storage lifecycle optimize costs as data transitions through its lifecycle.

* **Optimized driver**: The ABFS driver is optimized specifically for big data analytics. The corresponding REST APIs are surfaced through the endpoint dfs.core.windows.net.
# Azure data lake storage gen2 vs blob storage

* Data Lake gen 2 allows granular access control on a higher level as compared to the blob storage because it supports ACL permissions.
* ADLS is a hierarchical file system that possesses a hierarchical namespace. If we have a look at the blob storage, we will find a flat namespace. This is a dig into the performance of blob storage when we are talking about big data analytics.
* ADLS gen2 is Hadoop friendly and they can use the data which is available in storage while the blob storage is not compatible with it

# Azure Data Lake Gen1 vs Azure Data Lake Gen2
|Gen1|Gen2|
|---|---|
|In the azure data lake storage Gen1, you can store literally any amount of data of any size for any amount of time. So basically you will run analytic jobs using data lake analytics on the data stored in the data lake store.|Whereas talking about Azure data lake storage gen2, this advanced version will have both the options for storage that is the file system storage as well as the object system storage.|
|According to the Azure data lake storage gen1, the user will be able to store the data in the form of file storage which is separated into blocks giving you performance & security. This can be dependent on the Azure data lake storage hierarchy|Whereas Azure Data Lake Gen2 provides you with safety as well as healthy and smooth performance. When we talk about object storage, it is there for scalability.|
|Azure Data Lake Gen1 does not support Hot/Cold and Redundant storage| Whereas Azure Data Lake Gen2 supports Hot/Cold and Redundant storage|

# Reference
[1. Azure Data Lake Or ADLS Gen1 vs Gen2, Detailed Comparison | 2022](https://beetechnical.com/cloud-computing/azure-data-lake-storageadls-gen1-vs-gen2-complete-guide-2021/#:~:text=Azure%20data%20lake%20storage%20gen2%20vs%20blob%20storage,the%20blob%20storage%20because%20it%20supports%20ACL%20permissions.)

[2. Microsoft doc](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction)
