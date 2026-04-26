# ✅ YARN Architecture (15 Marks Answer)

## 🔷 Introduction to YARN

YARN (Yet Another Resource Negotiator) is a core component of the Hadoop ecosystem responsible for **resource management and job scheduling** across a cluster. It acts as the **operating system of Hadoop**, managing CPU, memory, and other resources efficiently.

👉 As given in your notes:

* YARN manages cluster resources
* It performs **scheduling and allocation of tasks** in Hadoop 

---

## 🔷 Need for YARN

Before YARN, Hadoop used MapReduce (MRv1), which had limitations:

* Single JobTracker → bottleneck
* Poor scalability
* Inefficient resource utilization

YARN solves these problems by separating:

* **Resource management**
* **Job processing**

---

## 🔷 Core Components of YARN Architecture

According to your PDF, YARN consists of **three major components** :

### 1️⃣ Resource Manager (RM)

* Central authority of YARN
* Allocates resources to applications
* Handles scheduling across cluster

**Functions:**

* Resource allocation (CPU, memory)
* Monitoring node status
* Deciding which application gets resources

👉 It is the **master daemon** in YARN.

---

### 2️⃣ Node Manager (NM)

* Runs on each node (slave machine)
* Manages resources at node level

**Functions:**

* Monitors resource usage (CPU, RAM)
* Reports to Resource Manager
* Manages containers on the node

👉 Works like a **local manager** for each machine.

---

### 3️⃣ Application Manager (ApplicationMaster - AM)

* Acts as a **bridge between RM and NM**
* Created per application

**Functions:**

* Negotiates resources from RM
* Communicates with Node Managers
* Manages execution of tasks

👉 Each application has its own ApplicationMaster.

---

## 🔷 Additional Concept: Containers

* A **container** is a unit of resource allocation
* Includes:

  * CPU
  * Memory
  * Network resources

👉 Applications run inside containers.

---

## 🔷 Working of YARN (Step-by-Step)

1. Client submits application to Resource Manager
2. RM allocates a container for ApplicationMaster
3. ApplicationMaster starts and registers with RM
4. AM requests resources (containers)
5. RM allocates containers on different nodes
6. Node Managers launch tasks inside containers
7. AM monitors execution and reports progress
8. After completion, resources are released

---

## 🔷 Advantages of YARN

* ✔ Better scalability
* ✔ Efficient resource utilization
* ✔ Supports multiple processing models (not only MapReduce)
* ✔ Fault tolerance
* ✔ Parallel processing

---

## 🔷 Role of YARN in Hadoop Ecosystem

As per your notes:

* YARN is one of the **four major components**:

  * HDFS → Storage
  * YARN → Resource management
  * MapReduce → Processing
  * Hadoop Common → Utilities 

---

## 🔷 Diagram (Important for Exam)

⚠️ Your PDF **does NOT contain a YARN architecture diagram explicitly**.
(It only lists components and explanation.)

👉 So you should draw this standard diagram in exam:

```
        +----------------------+
        |  Resource Manager    |
        +----------+-----------+
                   |
        -------------------------
        |           |           |
+---------------+ +---------------+ +---------------+
| Node Manager  | | Node Manager  | | Node Manager  |
| + Container   | | + Container   | | + Container   |
+---------------+ +---------------+ +---------------+

        ApplicationMaster interacts with both RM & NMs
```

📌 Since no diagram is present in your PDF →
👉 **Page number: Not available (No diagram given)**

---

## 🔷 Conclusion

YARN is a powerful resource management layer in Hadoop that enables efficient scheduling, scalability, and multi-processing capabilities by separating resource management from data processing.

---
