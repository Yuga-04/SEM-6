# Architecture of Convolutional Neural Network (CNN)

A **Convolutional Neural Network (CNN)** is a type of deep learning model used for **image recognition, image processing and classification**. CNN automatically extracts important features from input images using filters (kernels). 

---

# Neat Diagram of CNN Architecture

Draw the following simple diagram in the exam:

<img width="1290" height="498" alt="image" src="https://github.com/user-attachments/assets/bb13ac84-79e3-41a9-9e17-754c1214effb" />




<img width="1250" height="557" alt="image" src="https://github.com/user-attachments/assets/89afe52d-f011-4be3-8335-d284f91eba96" />





According to the **CNN architecture diagram in the PDF**, convolution and pooling layers perform **feature extraction**, while fully connected layers perform **classification**. 

---

# 1. Input Layer

* The **input layer receives the image** for processing.
* Example: A grayscale image of size **32 × 32 pixels** can be used as input.
* The image data is passed to the convolution layer. 

---

# 2. Convolutional Layer

The **convolutional layer extracts important features from the input image**.

### Functions

* Applies **filters (kernels)** to the image.
* Detects features such as **edges, textures, and patterns**.
* Produces a **feature map** as output.

### ReLU Activation

* After convolution, **ReLU activation function** is applied.
* It converts negative values to zero and introduces non-linearity.

Example:
Convolution output = `[-1, 2, -3, 4]`
ReLU output = `[0, 2, 0, 4]`. 

---

# 3. Pooling Layer

The **pooling layer reduces the size of feature maps while keeping important information**.

### Purpose

* Reduces computational complexity
* Prevents overfitting
* Retains important features

### Types

* **Max Pooling**
* **Average Pooling**

Example:
Max pooling reduces a **4 × 4 feature map to 2 × 2** by selecting the maximum value in each region. 

---

# 4. Flatten Layer

Flattening converts **multi-dimensional feature maps into a one-dimensional vector**.

Example:
A **3 × 3 × 64 feature map becomes a vector of size 576**. 

---

# 5. Fully Connected Layer

* In this layer, **each neuron is connected to every neuron in the previous layer**.
* It performs **classification of features extracted from previous layers**.

Example:
Features such as **wheels and windows** may be associated with the class **car**. 

---

# 6. Softmax Output Layer

* The **Softmax layer outputs probabilities for each class**.
* The class with the **highest probability is selected as the prediction**.

Example:

| Class   | Probability |
| ------- | ----------- |
| Car     | 0.7         |
| Truck   | 0.2         |
| Bicycle | 0.1         |

The model predicts **Car** since it has the highest probability. 

---

# Conclusion

CNN architecture consists of **convolution, pooling, flattening, fully connected, and softmax layers**. The convolution and pooling layers extract features from images, while the fully connected layer performs classification. CNNs are widely used for **image recognition and computer vision applications**. 

---

✅ **Exam Tip (important):**
Write **diagram + 5 layer explanations** → this alone gives **full 15 marks in most exams**.

---

If you want, I can also give **another 15-mark answer from the same PDF (Transfer Learning or RNN)** that might appear in your exam.
