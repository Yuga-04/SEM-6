# Rectified Linear Unit (ReLU) Activation Function and its Variants

## 1. Introduction

Activation functions play an important role in neural networks by introducing **non-linearity** so that complex patterns can be learned. One of the most widely used activation functions in deep learning is the **Rectified Linear Unit (ReLU)** because of its simplicity, computational efficiency, and ability to reduce the **vanishing gradient problem**. 

---

# 2. Rectified Linear Unit (ReLU)

The **Rectified Linear Unit (ReLU)** is an activation function that outputs the input directly if it is positive, otherwise it outputs zero.

### Mathematical Formula


<img width="231" height="109" alt="image" src="https://github.com/user-attachments/assets/d9e84b1e-0c8b-4f49-878b-0255b0f25c87" />




<img width="356" height="160" alt="image" src="https://github.com/user-attachments/assets/725d32f4-0d46-4f89-a512-37264f4a9249" />


### Characteristics of ReLU

1. **Simple and Efficient**

   * ReLU performs only a threshold operation, making computation faster.

2. **Non-Linearity**

   * Although the function is piecewise linear, it still introduces non-linearity.

3. **Sparse Activation**

   * Negative inputs produce zero output, so only some neurons activate.

4. **Prevents Vanishing Gradient Problem**

   * The derivative of ReLU is simple and allows gradients to flow effectively during backpropagation. 

### Derivative of ReLU


<img width="356" height="160" alt="image" src="https://github.com/user-attachments/assets/49164166-5426-404b-b6d2-06c5c4fa125a" />


---

## Diagram to Draw in Exam

Draw the **ReLU graph**:

* X-axis → Input (x)
* Y-axis → Output (f(x))

Graph shape:

* Flat line at **0 for negative values**
* Straight line **y = x for positive values**



<img width="672" height="389" alt="image" src="https://github.com/user-attachments/assets/20345007-0e0a-4227-9074-cd6f7ab0b838" />


---

# 3. Variants of ReLU

To overcome some limitations such as the **dying ReLU problem**, several improved versions of ReLU were introduced.

---

## 3.1 Leaky ReLU

Leaky ReLU allows a **small non-zero output for negative inputs**, preventing neurons from becoming inactive.

### Formula


<img width="318" height="142" alt="image" src="https://github.com/user-attachments/assets/9969ac08-6bf5-445d-a848-73c27669f414" />


<img width="342" height="89" alt="image" src="https://github.com/user-attachments/assets/ca639fab-aa5a-4a81-bd1b-9676fc81bf66" />


### Advantages

* Solves the **dying ReLU problem**
* Maintains gradient flow for negative inputs


<img width="654" height="374" alt="image" src="https://github.com/user-attachments/assets/155e625a-4afb-417f-a168-04242e443163" />


---

## 3.2 Parametric ReLU (PReLU)

Parametric ReLU is an improved version of Leaky ReLU where the slope for negative inputs is **learned during training**.

### Formula


<img width="323" height="114" alt="image" src="https://github.com/user-attachments/assets/52087d70-1b5b-48d2-a9b9-04778288416e" />


<img width="283" height="83" alt="image" src="https://github.com/user-attachments/assets/0bf59aff-ddcc-4a69-9217-a2645a48d589" />


### Advantages

* Learns the best slope for negative inputs
* More flexible than Leaky ReLU


<img width="619" height="354" alt="image" src="https://github.com/user-attachments/assets/fc4890ca-de51-45e5-988b-c90bf4d6cb00" />


---

## 3.3 Exponential Linear Unit (ELU)

ELU improves ReLU by introducing **smooth negative outputs**, which helps reduce bias shift and improves convergence.

### Formula

<img width="381" height="152" alt="image" src="https://github.com/user-attachments/assets/3fb05d12-0ed6-40a1-8a80-ff5c2a042b28" />


<img width="248" height="95" alt="image" src="https://github.com/user-attachments/assets/b93af6c2-e5c6-4e64-95b6-79446853840b" />

### Advantages

* Smooth negative values
* Faster convergence in deep networks

📌 **Diagram in PDF:** Page **23**. 

---

# 4. Comparison: ReLU vs Sigmoid vs Tanh

| Feature            | ReLU                      | Sigmoid                         | Tanh                            |
| ------------------ | ------------------------- | ------------------------------- | ------------------------------- |
| Output Range       | (0,\infty)                | (0,1)                           | (-1,1)                          |
| Gradient Problem   | Avoids vanishing gradient | Suffers from vanishing gradient | Suffers from vanishing gradient |
| Output Centering   | Not zero centered         | Not zero centered               | Zero centered                   |
| Computational Cost | Low                       | High                            | High                            |
| Common Usage       | Hidden layers             | Binary classification output    | Hidden layers                   |

Sigmoid and tanh compress input values into small ranges, causing **very small gradients**, which leads to the **vanishing gradient problem** during backpropagation. 


<img width="558" height="385" alt="image" src="https://github.com/user-attachments/assets/024148f4-49ae-4597-8c22-4a2f3b7e8c91" />


---

# 5. Conclusion

The **ReLU activation function** is widely used in deep learning because it is simple, efficient, and helps mitigate the vanishing gradient problem. Variants such as **Leaky ReLU, Parametric ReLU, and ELU** improve performance by addressing limitations like the dying ReLU problem. Compared to **sigmoid and tanh**, ReLU provides faster training and better gradient propagation in deep neural networks.

---
