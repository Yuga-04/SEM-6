### Simplified IoT Architecture (15 Marks Answer)

A **Simplified IoT Architecture** provides a basic framework that explains how IoT systems are designed and how different components interact to collect, process, and use data. The architecture simplifies complex IoT systems into essential building blocks so that designers and developers can understand the structure and operation of IoT networks. 

This architecture is commonly represented using **two parallel stacks**:

1. **Core IoT Functional Stack**
2. **IoT Data Management and Compute Stack**

These stacks work together to enable communication between devices, processing of data, and delivery of intelligent services. 

---

# Diagram: Simplified IoT Architecture

*(Diagram is shown in the PDF)*
**Page Number for the Diagram: Page 10** 

The diagram on page 10 shows the **Core IoT Functional Stack** and the **IoT Data Management and Compute Stack** aligned side by side with **security applied across all layers**.

Structure shown in the diagram:

```
Core IoT Functional Stack        IoT Data Management & Compute Stack

Applications                     Cloud
Communications Network           Fog
Things (Sensors & Actuators)     Edge
```

---

# 1. Core IoT Functional Stack

The **Core IoT Functional Stack** consists of three main layers that define the basic functioning of an IoT system.

### 1. Things Layer (Sensors and Actuators)

This is the **lowest layer** of the IoT architecture.

* It contains **physical devices**, sensors, and actuators.
* Sensors collect data from the environment such as temperature, humidity, motion, or pressure.
* Actuators perform actions such as switching devices on/off or controlling machines.
* These smart objects gather data and send it to the network for further processing. 

Example:

* Temperature sensor in a smart home
* Motion sensor in a security system
* Smart meters in energy monitoring

---

### 2. Communications Network Layer

This layer provides **connectivity between devices and the IoT system**.

Functions:

* Transfers data from sensors to processing systems
* Enables communication between IoT devices and external networks
* Uses wired or wireless communication technologies.

Common technologies:

* Wi-Fi
* Bluetooth
* ZigBee
* Cellular networks (4G/5G)
* LoRa

The network layer may also include **gateways and routers** that collect data from multiple devices and forward it to central processing systems. 

---

### 3. Applications Layer

This is the **top layer of the IoT architecture**.

Functions:

* Processes and analyzes collected data
* Provides user interfaces such as mobile apps or dashboards
* Generates insights and controls IoT devices based on analytics.

Applications may include:

* Smart home automation
* Healthcare monitoring systems
* Smart city traffic management
* Industrial automation systems. 

---

# 2. IoT Data Management and Compute Stack

Parallel to the functional stack is the **Data Management and Compute Stack**, which manages data processing and storage.

### 1. Edge Layer

* Data processing occurs **close to the IoT devices**.
* Reduces latency and network load.
* Example: Data filtering inside sensors or local gateways.

### 2. Fog Layer

* Intermediate processing layer between edge and cloud.
* Performs **data aggregation and temporary storage**.
* Often implemented in gateways or local servers.

### 3. Cloud Layer

* Centralized platform for **large-scale data storage and analysis**.
* Performs advanced analytics, machine learning, and long-term storage.
* Enables remote monitoring and control of IoT systems. 

---

# Security in Simplified IoT Architecture

Security is applied **across all layers** of the IoT architecture.

It includes:

* Device authentication
* Data encryption
* Secure communication protocols
* Access control mechanisms

Security ensures that IoT systems remain safe from cyber attacks and unauthorized access.

---

# Conclusion

The **Simplified IoT Architecture** provides a clear framework for designing IoT systems by dividing the architecture into the **Core IoT Functional Stack** and the **IoT Data Management and Compute Stack**.

The functional stack manages **devices, communication, and applications**, while the compute stack manages **data processing from edge to cloud**. This layered architecture enables scalable, efficient, and intelligent IoT systems for various applications such as smart homes, healthcare, industry, and smart cities. 

---

<img width="489" height="302" alt="image" src="https://github.com/user-attachments/assets/bce65337-29b8-4b96-a3b9-d6da13020233" />
