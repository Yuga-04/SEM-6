# Classification by Backpropagation

Backpropagation is one of the most important algorithms used in **Neural Networks** for **classification and prediction**. It is a supervised learning algorithm used to train multilayer feed-forward neural networks.

The algorithm learns by repeatedly adjusting weights in the network so that the predicted output becomes closer to the actual output. 

---

# Introduction

A **Neural Network** is a collection of interconnected processing units called **neurons**. Each connection between neurons has an associated weight.

During learning:

* Input data is fed into the network.
* The network predicts output.
* The predicted output is compared with the actual output.
* Errors are calculated.
* Weights are adjusted to reduce error.

This learning mechanism is called:

# Backpropagation Learning



---

# Definition

Backpropagation is a neural network learning algorithm that learns by propagating errors backward through the network and updating weights to minimize prediction error. 

---

# Multilayer Feed-Forward Neural Network

Backpropagation works on a:

# Multilayer Feed-Forward Neural Network

The network contains:

1. Input Layer
2. Hidden Layer(s)
3. Output Layer



---

# 1. Input Layer

* Receives input attributes.
* Each neuron represents one attribute.
* Passes input values to hidden layer.

Example:

| Attribute  | Input Node |
| ---------- | ---------- |
| Age        | X1         |
| Salary     | X2         |
| Experience | X3         |

---

# 2. Hidden Layer

* Performs internal computations.
* Identifies hidden relationships and patterns.
* One or more hidden layers may exist.

The hidden layer increases learning capability.

---

# 3. Output Layer

* Produces final classification result.
* Each neuron represents a class label.

Example:

| Output | Class        |
| ------ | ------------ |
| 1      | Buy Computer |
| 0      | Do Not Buy   |

---

# Characteristics of Backpropagation Network

## 1. Feed-Forward Nature

* Data moves only in forward direction.
* No cycles or feedback connections exist.

---

## 2. Fully Connected

* Every neuron in one layer is connected to neurons in the next layer.

---

## 3. Supervised Learning

* Requires training data with known outputs.



---

# Working of Backpropagation Algorithm

The algorithm works in two phases:

1. Forward Propagation
2. Backward Propagation

---

# Phase 1: Forward Propagation

In this phase:

1. Training tuple is fed into input layer.
2. Inputs pass through hidden layers.
3. Each neuron computes weighted sum.
4. Activation function is applied.
5. Output is generated.



---

# Net Input Calculation

For a neuron j:

```text id="f36ls0"
Ij = Σ(wij × Oi) + θj
```

Where:

* wij = weight between neurons
* Oi = output from previous neuron
* θj = bias value



---

# Activation Function

The sigmoid activation function is commonly used.

```text id="f6u52y"
Oj = 1 / (1 + e^-Ij)
```

Where:

* Oj = output of neuron
* Ij = net input

The sigmoid function converts values between 0 and 1.



---

# Phase 2: Backward Propagation

After generating output:

* Predicted output is compared with target output.
* Error is computed.
* Error is propagated backward.
* Weights and biases are updated.

This process minimizes classification error.



---

# Error Calculation for Output Layer

For output neuron j:

```text id="qknrpn"
Errj = Oj(1 − Oj)(Tj − Oj)
```

Where:

* Oj = actual output
* Tj = target output



---

# Error Calculation for Hidden Layer

For hidden neuron j:

```text id="b7v2zd"
Errj = Oj(1 − Oj) Σ(wjk × Errk)
```

Where:

* wjk = weight from hidden neuron j to output neuron k
* Errk = error of output neuron



---

# Weight Update Rule

Weights are updated using:

```text id="g4dgph"
Δwij = l × Errj × Oi
```

New weight:

```text id="qkjh13"
wij = wij + Δwij
```

Where:

* l = learning rate
* Errj = error term
* Oi = previous neuron output



---

# Bias Update

Biases are also updated to improve learning.

```text id="ax76p2"
Δθj = l × Errj
```



---

# Steps in Backpropagation Algorithm

## Step 1: Initialize Network

* Select number of layers.
* Assign random weights and biases.

---

## Step 2: Feed Training Tuple

Input data is fed to input layer.

---

## Step 3: Forward Propagation

Compute outputs layer by layer.

---

## Step 4: Compute Error

Compare predicted output with target output.

---

## Step 5: Backward Propagation

Propagate errors backward.

---

## Step 6: Update Weights

Adjust weights and biases.

---

## Step 7: Repeat

Repeat until minimum error is achieved.

---

# Example of Classification using Backpropagation

Suppose we want to classify students as:

* Pass
* Fail

Input attributes:

| Attribute        | Value |
| ---------------- | ----- |
| Attendance       | 90%   |
| Internal Marks   | 80    |
| Assignment Score | 85    |

The neural network processes these inputs.

Output:

| Output Node | Prediction |
| ----------- | ---------- |
| 1           | Pass       |
| 0           | Fail       |

The network learns from previous student records and predicts future classifications accurately.

---

# Advantages of Backpropagation

## 1. High Classification Accuracy

Provides accurate predictions for complex datasets.

---

## 2. Learns Nonlinear Relationships

Can learn hidden and complex patterns.

---

## 3. Adaptive Learning

Weights automatically improve through training.

---

## 4. Handles Noisy Data

Can classify even with incomplete or noisy data.

---

## 5. Widely Applicable

Used in many real-world applications.



---

# Disadvantages of Backpropagation

## 1. Slow Training

Training large networks takes significant time.

---

## 2. Requires Large Training Data

Accuracy depends on quality and quantity of data.

---

## 3. Difficult to Interpret

Acts as a “black box”.

---

## 4. Trial-and-Error Network Design

Choosing hidden layers and neurons is difficult.



---

# Applications of Backpropagation

* Image recognition
* Medical diagnosis
* Handwriting recognition
* Fraud detection
* Speech recognition
* Weather forecasting
* Email spam filtering
* Stock market prediction

---

# Conclusion

Backpropagation is a powerful neural network learning algorithm used for classification and prediction. It works by propagating inputs forward through the network and propagating errors backward to adjust weights. Through repeated learning, the network minimizes error and produces accurate classifications. Due to its ability to learn complex nonlinear relationships, backpropagation is widely used in modern machine learning and data mining applications. 
