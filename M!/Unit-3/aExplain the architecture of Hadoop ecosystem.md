# Architecture of Hadoop Ecosystem

The **Hadoop Ecosystem** is a platform or suite that provides different services required to solve big data problems. Hadoop is an open-source framework designed to store and process large datasets using clusters of computers. It enables distributed storage and parallel processing of data. 

The Hadoop ecosystem contains several tools and components that work together to perform **data storage, processing, resource management, and analysis**.

The four major elements of the Hadoop ecosystem are:

1. **HDFS (Hadoop Distributed File System)**
2. **YARN (Yet Another Resource Negotiator)**
3. **MapReduce**
4. **Hadoop Common Utilities**

In addition to these, several other tools such as **Hive, Pig, HBase, Spark, Mahout, Zookeeper, and Oozie** support the ecosystem. 

---

# 1. HDFS (Hadoop Distributed File System)

HDFS is the **primary storage component** of the Hadoop ecosystem. It is responsible for storing large volumes of structured and unstructured data across multiple machines in a distributed environment.

### Components of HDFS

HDFS mainly consists of two core components:

**1. NameNode**

* It is the master node of HDFS.
* It stores **metadata (data about data)** such as file names, file locations, and block information.
* It coordinates the entire Hadoop cluster.

**2. DataNode**

* These are the worker nodes.
* They store the actual data blocks.
* DataNodes perform operations like **reading, writing, replication, creation, and deletion of blocks**.

HDFS stores files by dividing them into **blocks** which are distributed across different DataNodes. This improves reliability and fault tolerance. 

---

# 2. YARN (Yet Another Resource Negotiator)

YARN is responsible for **resource management and job scheduling** in the Hadoop ecosystem.

It manages cluster resources and allocates them to different applications.

### Components of YARN

1. **Resource Manager**

   * Allocates resources for applications in the cluster.

2. **Node Manager**

   * Manages resources like CPU, memory, and bandwidth on each machine.

3. **Application Manager**

   * Acts as a communication interface between the resource manager and node manager.

YARN ensures efficient use of cluster resources. 

---

# 3. MapReduce

MapReduce is the **data processing framework** used in Hadoop for analyzing large datasets using distributed and parallel algorithms.

It processes data using two main functions:

### Map Function

* Performs **sorting and filtering of data**.
* Produces intermediate **key-value pairs**.

### Reduce Function

* Processes the output of the Map function.
* Aggregates and summarizes the data to produce the final result.

MapReduce allows applications to process huge amounts of data efficiently across clusters. 

---

# 4. Hadoop Common Utilities

Hadoop Common contains **libraries and utilities** required by other Hadoop modules. These utilities provide the basic services needed for Hadoop operations.

---

# Additional Components of Hadoop Ecosystem

Apart from the core components, several tools extend Hadoop capabilities.

### Pig

* Developed by Yahoo.
* Uses **Pig Latin language** for analyzing large datasets.
* Simplifies programming by automatically executing MapReduce tasks.

### Hive

* Provides **SQL-like query language (HQL)**.
* Used for reading and writing large datasets in Hadoop.

### HBase

* A **NoSQL database** used for handling large structured data.
* Supports quick data retrieval.

### Spark

* A fast processing platform using **in-memory computing**.
* Suitable for real-time analytics.

### Mahout

* Provides **machine learning algorithms** such as clustering and classification.

### Zookeeper

* Handles **coordination, synchronization, and communication** between Hadoop components.

### Oozie

* A **workflow scheduler** used to schedule Hadoop jobs. 

---

# Conclusion

The Hadoop ecosystem architecture consists of multiple integrated components that enable efficient storage, processing, and analysis of big data. Core modules such as **HDFS, YARN, MapReduce, and Hadoop Common** work together with additional tools like **Hive, Pig, Spark, and HBase** to provide a complete big data processing framework.

---

<img width="537" height="369" alt="image" src="https://github.com/user-attachments/assets/8d229494-30e8-4b2a-9ded-a7413be1f698" />

