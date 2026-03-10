# Popular CNN Architectures: LeNet, AlexNet, and VGGNet

Convolutional Neural Networks (CNNs) have evolved through several architectures that improved image classification performance. Popular CNN architectures include **LeNet, AlexNet, and VGGNet**, which introduced improvements in depth, accuracy, and computational efficiency. 

---

# 1. LeNet Architecture

LeNet is one of the **earliest CNN architectures** developed for handwritten digit recognition.

### Features

* Designed for **digit recognition tasks such as MNIST**.
* Uses **convolution layers, pooling layers, and fully connected layers**.
* Small and simple architecture.
* Uses **feature extraction followed by classification**.

### Structure

Typical LeNet architecture:

Input Image → Convolution → Pooling → Convolution → Pooling → Fully Connected → Output

LeNet introduced the basic CNN idea where **convolution layers detect features and fully connected layers perform classification**.

---

# 2. AlexNet Architecture

AlexNet is one of the **first deep CNN models that popularized CNNs for image classification**. It was developed by **Alex Krizhevsky**.

### Key Features

* Contains **8 layers** (5 convolution layers + 3 fully connected layers).
* Uses **ReLU activation function**.
* Uses **dropout regularization** to reduce overfitting.
* Achieved strong performance in image classification benchmarks.

According to the PDF, AlexNet:

* Uses a **simple architecture with 8 layers**
* Applies **ReLU activation and dropout regularization**. 

### Improvements over LeNet

* Deeper architecture.
* Better performance on large datasets.
* Uses modern activation functions and regularization.

---

# 3. VGGNet Architecture

VGGNet was developed by the **Visual Geometry Group (Oxford University)** and is known for its **deep architecture and simple design**.

### Features

* Deep CNN architecture.
* Uses **16 or 19 layers**.
* Uses **small 3 × 3 convolution filters**.
* Stacks multiple convolution layers to learn complex features.

According to the PDF:

* **VGG-16 contains 16 layers**
* **13 convolution layers and 3 fully connected layers**. 

### Structure of VGG-16

* Input layer: **224 × 224 × 3 image**
* Multiple convolution layers
* Max-pooling layers
* Fully connected layers
* Softmax output layer

The architecture learns **hierarchical visual features from simple edges to complex objects**. 

---

# Diagram in Your PDF (Important for Exam)



<img width="1250" height="596" alt="image" src="https://github.com/user-attachments/assets/a53fecaa-f1c6-4eba-9d7d-c413c16aa65c" />



<img width="1250" height="649" alt="image" src="https://github.com/user-attachments/assets/0899aa5f-5643-461b-8d6f-a8c7e5e3b733" />




These diagrams illustrate:

Input → Convolution Layers → Max Pooling → Fully Connected Layers → Softmax Output

---

# Comparison of CNN Architectures

| Architecture | Layers          | Key Features                    | Improvements                                           |
| ------------ | --------------- | ------------------------------- | ------------------------------------------------------ |
| **LeNet**    | Few layers      | Early CNN for digit recognition | Introduced convolution + pooling                       |
| **AlexNet**  | 8 layers        | ReLU activation, dropout        | Deeper network and better accuracy                     |
| **VGGNet**   | 16 or 19 layers | Uses small 3×3 filters          | Much deeper architecture and better feature extraction |

---

# Conclusion

LeNet, AlexNet, and VGGNet represent important milestones in the evolution of CNN architectures. **LeNet introduced the basic CNN concept**, **AlexNet improved performance using deeper networks and ReLU activation**, and **VGGNet further increased depth using small convolution filters**, leading to better feature extraction and higher accuracy in image classification tasks. 

---
