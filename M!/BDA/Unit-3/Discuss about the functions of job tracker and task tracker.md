# ✅ Functions of Job Tracker and Task Tracker (15 Marks)

## 🔷 Introduction

In the earlier Hadoop MapReduce (MRv1) architecture, **Job Tracker** and **Task Tracker** are the two main components responsible for **job execution and monitoring** in a distributed environment.

* **Job Tracker → Master node**
* **Task Tracker → Slave nodes**

They work together to process large datasets using parallel computation.

---

# 🔷 Job Tracker

## 📌 Definition

Job Tracker is the **master component** that manages and coordinates all MapReduce jobs in the Hadoop cluster.

---

## ⚙️ Functions of Job Tracker

### 1️⃣ Job Scheduling

* Accepts jobs submitted by clients
* Divides jobs into smaller tasks (Map & Reduce tasks)
* Schedules tasks based on resource availability

---

### 2️⃣ Resource Management

* Keeps track of available resources in the cluster
* Assigns tasks to appropriate Task Trackers

---

### 3️⃣ Task Assignment

* Assigns **Map tasks first**, then Reduce tasks
* Tries to assign tasks near data location (data locality)

---

### 4️⃣ Monitoring and Status Tracking

* Continuously monitors execution of tasks
* Receives heartbeat signals from Task Trackers
* Updates job progress

---

### 5️⃣ Fault Tolerance

* Detects failed tasks or nodes
* Reassigns tasks to another Task Tracker

---

### 6️⃣ Maintaining Metadata

* Maintains information about:

  * Job status
  * Task progress
  * Node availability

---

### 7️⃣ Coordination

* Acts as a central coordinator between all Task Trackers

---

# 🔷 Task Tracker

## 📌 Definition

Task Tracker is the **worker node component** responsible for executing tasks assigned by the Job Tracker.

---

## ⚙️ Functions of Task Tracker

### 1️⃣ Task Execution

* Executes Map and Reduce tasks on local machine
* Processes data blocks

---

### 2️⃣ Slot Management

* Has a fixed number of slots:

  * Map slots
  * Reduce slots
* Runs tasks within these slots

---

### 3️⃣ Status Reporting

* Sends **heartbeat signals** to Job Tracker
* Reports:

  * Task completion
  * Failures
  * Resource usage

---

### 4️⃣ Data Handling

* Reads input data from HDFS
* Writes output back to HDFS

---

### 5️⃣ Failure Handling

* If task fails → informs Job Tracker
* Can restart tasks locally if needed

---

### 6️⃣ Local Resource Management

* Manages CPU, memory, and disk usage on node

---

# 🔷 Working of Job Tracker & Task Tracker Together

1. Client submits job to Job Tracker
2. Job Tracker splits job into tasks
3. Job Tracker assigns tasks to Task Trackers
4. Task Trackers execute tasks
5. Task Trackers send progress updates (heartbeats)
6. Job Tracker monitors and reassigns failed tasks
7. Final output is stored in HDFS

---

# 🔷 Advantages

* Parallel processing of large data
* Fault tolerance
* Efficient task distribution

---

# 🔷 Limitations (Important for marks)

* Job Tracker becomes a **single point of failure**
* Scalability issues
* High load on Job Tracker

👉 These limitations led to the introduction of **YARN** 

---

# 🔷 Diagram (Write in Exam)

```
        +------------------+
        |   Job Tracker    |
        +--------+---------+
                 |
      -------------------------
      |           |           |
+------------+ +------------+ +------------+
|TaskTracker | |TaskTracker | |TaskTracker |
|  Map/Reduce| |  Map/Reduce| |  Map/Reduce|
+------------+ +------------+ +------------+
```

📌 **Diagram in PDF:**
❌ Not explicitly present → No page number available

---

# 🔷 Conclusion

Job Tracker and Task Tracker form the core of Hadoop’s MapReduce processing model, where Job Tracker manages and schedules tasks, while Task Trackers execute them in a distributed manner. However, due to scalability issues, this architecture was later replaced by YARN.

---

