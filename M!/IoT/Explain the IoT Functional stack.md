### IoT Functional Stack (15 Marks Answer)

The **IoT Functional Stack** describes the basic structure of an IoT system and explains how smart devices communicate, process data, and provide services to users. It defines the **main functional layers that enable IoT devices to interact with networks and applications**.

According to the simplified IoT architecture, the **Core IoT Functional Stack consists of three main layers**:

1. Things Layer (Sensors and Actuators)
2. Communications Network Layer
3. Applications and Analytics Layer. 

These layers work together to collect data from the environment, transmit the data through networks, and provide intelligent services through applications.

---

# Diagram of Core IoT Functional Stack

*(Diagram available in the PDF)*

**Diagram Page Number:** **Page 10** 

Simple representation:

```
Applications
-----------------------
Communications Network
-----------------------
Things (Sensors & Actuators)
```

---

# 1. Things Layer (Sensors and Actuators Layer)

The **Things layer** is the **lowest layer of the IoT functional stack**. It consists of physical objects such as sensors, actuators, and smart devices that interact with the environment.

These smart objects collect data and perform actions based on instructions received from the IoT system. The devices are called “things” because they represent real-world objects connected to the internet.

### Functions

* Collect environmental data
* Monitor physical conditions
* Perform automated actions
* Communicate with network systems

### Examples

* Temperature sensors
* Motion detectors
* Smart meters
* Wearable health devices

The design of IoT devices depends on several characteristics such as:

* **Power source** (battery-powered or external power)
* **Mobility** (mobile or fixed devices)
* **Reporting frequency** (how often data is sent)
* **Data complexity** (simple or rich data). 

These characteristics determine the communication method and performance of the IoT device.

---

# 2. Communications Network Layer

The **Communications Network layer** enables communication between IoT devices and the rest of the system. It provides connectivity and ensures that data collected by sensors is transmitted to processing systems or cloud platforms.

This layer includes several networking technologies and protocols used to connect IoT devices.

### Functions

* Transfer data from sensors to gateways
* Enable communication between devices
* Provide internet connectivity
* Manage network operations

### Sublayers in Communication Network

The communications layer can be divided into several sublayers:

#### 1. Access Network Sublayer

This is the **last-mile connectivity** between IoT devices and the network.

Examples:

* Wi-Fi
* Bluetooth
* ZigBee
* LoRa
* IEEE 802.15.4

These technologies connect sensors to gateways or routers. 

---

#### 2. Gateways and Backhaul Network Sublayer

Gateways collect data from multiple sensors and forward it to central processing systems.

Functions of gateway:

* Aggregates sensor data
* Converts communication protocols
* Sends data through backhaul networks to central servers. 

---

#### 3. Network Transport Sublayer

This layer uses **network protocols** to ensure reliable communication.

Examples:

* IP (Internet Protocol)
* UDP
* TCP

These protocols help transmit data across different networks.

---

#### 4. IoT Network Management Sublayer

This sublayer manages communication between sensors and applications.

Examples of protocols:

* MQTT
* CoAP

These protocols enable efficient message exchange between devices and IoT platforms. 

---

# 3. Applications and Analytics Layer

The **Applications and Analytics layer** is the top layer of the IoT functional stack. It processes the data received from devices and provides meaningful services to users.

### Functions

* Analyze collected data
* Provide user interfaces
* Control IoT devices
* Generate insights and reports

Applications may run on cloud platforms, data centers, or edge systems.

### Types of Applications

#### Analytics Applications

These applications process collected data and provide insights.

Examples:

* Weather prediction systems
* Smart agriculture monitoring
* Industrial performance analysis.

#### Control Applications

These applications control the behavior of IoT devices based on analyzed data.

Example:

* A pressure sensor detecting low pressure may trigger a pump to increase speed. 

---

# Role of Analytics in IoT Applications

Analytics plays an important role in IoT systems. Two main types are:

### Data Analytics

Processes data collected from sensors to generate meaningful insights such as trends, patterns, or predictions.

Example:

* Predicting storms using environmental sensor data.

### Network Analytics

Monitors the performance of the IoT network itself and detects connectivity issues or failures. 

---

# Conclusion

The **IoT Functional Stack** provides a structured model for designing IoT systems. It consists of three major layers: **Things layer, Communications Network layer, and Applications layer**.

The **Things layer collects data**, the **network layer transfers the data**, and the **application layer analyzes the data and delivers intelligent services**. This layered architecture helps developers build scalable, efficient, and intelligent IoT solutions for various applications such as smart homes, healthcare systems, and industrial automation. 

---

