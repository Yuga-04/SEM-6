Below is the **15-mark answer derived only from the uploaded Unit-III document** about **Hadoop Distributed File System (HDFS)**. I also included a **simple neat diagram representation** based on the architecture described in the document. 

---

# Hadoop Distributed File System (HDFS)

Hadoop Distributed File System (HDFS) is a distributed file system designed to store and process very large datasets across clusters of commodity computers. It provides high throughput access to application data and is highly fault tolerant. HDFS stores data across multiple machines and allows parallel processing of large data sets. 

In Hadoop, data is stored in a distributed file system instead of a single computer. Files are divided into blocks and stored across different machines called DataNodes. The system is designed using a **master–slave architecture**. 

---

# HDFS Architecture (Neat Diagram)

<img width="1032" height="586" alt="image" src="https://github.com/user-attachments/assets/ee0ee71b-16ab-4067-8558-a2ecfda7d6d8" />
<img width="1033" height="582" alt="image" src="https://github.com/user-attachments/assets/ef4581c5-3076-45bd-88b5-2653575106bb" />
<img width="1227" height="756" alt="image" src="https://github.com/user-attachments/assets/4a4a8924-8fdb-481c-b560-2d25a5e6447a" />


---

# Components of HDFS

The HDFS architecture mainly consists of the following components.

## 1. NameNode

The **NameNode** is the master server of HDFS.

Functions:

* Manages the file system namespace.
* Maintains metadata such as file names, permissions, and block locations.
* Performs operations such as opening, closing, renaming files and directories.
* Controls the mapping of blocks to DataNodes.

Metadata is stored in memory for fast access and also saved on disk for reliability. 

---

## 2. DataNode

DataNodes are the worker nodes in HDFS.

Functions:

* Store the actual data blocks.
* Serve read and write requests from clients.
* Perform block creation, deletion, and replication based on instructions from the NameNode.
* Periodically send block reports and heartbeats to the NameNode.

DataNodes usually run on commodity hardware. 

---

## 3. Secondary NameNode

The **Secondary NameNode** helps the primary NameNode.

Functions:

* Performs periodic checkpoint operations.
* Merges edit logs with file system images.
* Helps reduce load on the NameNode and assists in recovery if failure occurs. 

---

## 4. HDFS Client

The **HDFS client** is the interface used by users or applications to interact with HDFS.

Functions:

* Communicates with the NameNode to locate file blocks.
* Interacts directly with DataNodes to read or write data. 

---

# Block Structure in HDFS

HDFS stores files by dividing them into **large blocks**.

Key points:

* Default block size is **128 MB**.
* Blocks are stored across different DataNodes.
* Each block is replicated (default replication factor is **3**) to ensure fault tolerance.
* The NameNode keeps track of block locations. 

---

# Features of HDFS

Some important features of HDFS include:

* Distributed data storage
* High fault tolerance through replication
* High reliability and availability
* Efficient handling of large datasets
* Uses inexpensive commodity hardware

These features make HDFS suitable for processing large-scale data in Hadoop environments. 

---

# Conclusion

HDFS is a core component of the Hadoop ecosystem designed to store massive datasets across clusters of computers. Its **master–slave architecture, block storage mechanism, and replication strategy** ensure reliable, scalable, and fault-tolerant data storage for big data applications. 

