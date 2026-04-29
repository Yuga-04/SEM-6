# ✍️ **Steps to Set Up and Program an Arduino UNO**

## 🔹 Introduction

**Arduino UNO** is an open-source microcontroller-based development board used to build IoT and embedded system applications. It can read inputs from sensors and control outputs like LEDs, motors, etc.

---

# 🔹 1. Software Installation (Arduino IDE)

### Steps:

1. Visit the official Arduino website and download the **Arduino IDE**.
2. Install the IDE on your system (Windows/Mac/Linux).
3. Connect the Arduino UNO board to the computer using a USB cable.
4. Install drivers (if required):

   * Go to **Device Manager → Ports**
   * Select **Arduino UNO (COMxx)**
5. Open Arduino IDE.
6. Select:

   * **Tools → Board → Arduino UNO**
   * **Tools → Port → COMxx**

---

# 🔹 2. Understanding Arduino UNO Hardware

* **Microcontroller** – Executes the program
* **Digital Pins (0–13)** – Input/Output (HIGH/LOW)
* **Analog Pins (A0–A5)** – Read analog values
* **USB Port** – For programming and power
* **Power Pins (5V, 3.3V, GND)** – Supply power

---

# 🔹 3. Basic Programming Concepts

### 🔸 Arduino Program Structure

Every Arduino program (sketch) has two main functions:

```cpp
void setup() {
  // runs once
}

void loop() {
  // runs repeatedly
}
```

---

### 🔸 Key Concepts

#### 1. Variables

Used to store data
Example:

```cpp
int ledPin = 13;
```

#### 2. Data Types

* int (integer)
* float
* boolean

#### 3. Input/Output Functions

* `pinMode(pin, mode)` → define pin as INPUT/OUTPUT
* `digitalWrite(pin, HIGH/LOW)` → output
* `digitalRead(pin)` → input
* `analogRead(pin)` → read analog values

#### 4. Control Statements

* if, else
* for loop
* while loop

#### 5. Delay Function

```cpp
delay(1000); // 1 second
```

---

# 🔹 4. Writing and Uploading Program

### Steps:

1. Open Arduino IDE
2. Write the program
3. Click **Verify (✓)** to compile
4. Click **Upload (→)** to send code to Arduino
5. Observe output on the hardware

---

# 🔹 5. Simple Example: Blinking LED

### 🔸 Circuit:

* Connect LED to pin 13
* Connect resistor and GND

---

### 🔸 Code:

```cpp
int ledPin = 13;

void setup() {
  pinMode(ledPin, OUTPUT);
}

void loop() {
  digitalWrite(ledPin, HIGH); // LED ON
  delay(1000);                // wait 1 second
  digitalWrite(ledPin, LOW);  // LED OFF
  delay(1000);                // wait 1 second
}
```

---

### 🔸 Working:

* LED turns ON for 1 second
* Then OFF for 1 second
* This repeats continuously

---

# 🔹 6. Testing the Setup

* Use built-in example:
  **File → Examples → Basics → Blink**
* Upload and check LED blinking
* If working → setup is successful

---

# 🔹 Conclusion

Setting up Arduino UNO involves installing the IDE, configuring the board, understanding basic programming concepts, and uploading code. With simple programs like LED blinking, beginners can easily start building IoT and embedded system projects.

---

