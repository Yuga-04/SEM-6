# Feed Forward and Back Propagation to Find Minimum Loss in a Neural Network

## 1. Introduction

A **Feed Forward Neural Network (FFNN)** is a type of artificial neural network where information flows only in the **forward direction from input layer to output layer**. There are no cycles or feedback connections.

Training a neural network involves two main processes:

1. **Feed Forward propagation** – computing the output.
2. **Back Propagation** – updating weights using gradients to minimize the loss function. 

The objective of training is to **minimize the loss (error) between predicted output and actual output**.

---

# 2. Feed Forward Process

In feed forward propagation, the input passes through the hidden layer and output layer.

### Step 1: Calculate Weighted Sum

For each neuron:


<img width="634" height="243" alt="image" src="https://github.com/user-attachments/assets/5a3998bd-e7f8-484a-86c1-9a35e71074b7" />


---

### Step 2: Apply Activation Function

Example (ReLU or sigmoid):


<img width="125" height="83" alt="image" src="https://github.com/user-attachments/assets/dfa830d0-9c8b-4ca2-a6bf-5f73c18d3718" />


This produces the **neuron output**.

---

### Step 3: Compute Network Output

The output from the hidden layer becomes the input to the **output layer**, and the final predicted output ( \hat{y} ) is obtained.

---

# 3. Loss Function

The difference between predicted output and actual output is measured using a **loss function**.

Example: **Mean Squared Error (MSE)**


<img width="602" height="243" alt="image" src="https://github.com/user-attachments/assets/40e19abc-fb69-4795-81b8-4ba203d05feb" />


The goal of training is to **minimize this loss**.

---

# 4. Example: Feed Forward Calculation

### Given

<img width="682" height="327" alt="image" src="https://github.com/user-attachments/assets/dc345b5d-6d86-4efd-9a83-91ef0cb2f4d6" />


---

### Step 1: Weighted Sum


<img width="355" height="123" alt="image" src="https://github.com/user-attachments/assets/a51c0e53-42ed-485a-9226-6d3ce859b30b" />


---

### Step 2: Activation Function (ReLU)


<img width="632" height="222" alt="image" src="https://github.com/user-attachments/assets/09f64b63-1df3-4339-8373-bcc10622531d" />


---

### Step 3: Compute Loss

Assume actual output

<img width="614" height="301" alt="image" src="https://github.com/user-attachments/assets/96cf18ba-8781-4ea6-81cb-2f95a5466bae" />


---

# 5. Back Propagation

Back propagation updates weights by computing the **gradient of the loss with respect to weights**.

### Step 1: Compute Gradient

<img width="692" height="238" alt="image" src="https://github.com/user-attachments/assets/648975ad-6ace-46b8-8880-7302046ffc46" />


---

### Step 2: Weight Update (Gradient Descent)

<img width="681" height="223" alt="image" src="https://github.com/user-attachments/assets/3d4f790c-7966-40ff-8f7f-9767d176135c" />


---

# 6. Iterative Training

The process repeats:

1. Feed Forward
2. Compute Loss
3. Back Propagation
4. Update Weights

After many iterations, the loss **gradually decreases and reaches a minimum value**.

---

# 7. Advantages of Back Propagation

* Efficient training of deep neural networks
* Automatically adjusts weights
* Minimizes loss through gradient descent

---

# 8. Conclusion

Feed forward propagation computes the predicted output of a neural network, while back propagation updates the weights to minimize the loss function. By repeatedly applying these steps using gradient descent, the neural network gradually converges to the **minimum loss**, improving prediction accuracy.

---
