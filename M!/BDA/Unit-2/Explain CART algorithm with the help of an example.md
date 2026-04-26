Here is a **complete 15-mark answer on CART algorithm** based strictly on your PDF  👇

---

# ✅ CART Algorithm (Classification and Regression Tree)

## 🔷 1. Introduction

CART (Classification and Regression Tree) is a **decision tree algorithm** used for both:

* **Classification** (categorical output)
* **Regression** (continuous output)

👉 It builds a tree using a **recursive partitioning approach**.  (Page 36)

---

## 🔷 2. Key Features of CART

* Produces a **binary tree** (each node splits into two branches)
* Uses **Gini Index** as the splitting criterion
* Works with both **categorical and numerical data**
* Splits data recursively until stopping condition is met

👉 Hence, CART is also called a **Binary Decision Tree**  (Page 36)

---

## 🔷 3. Gini Index (Splitting Measure)

CART uses **Gini Index** to measure impurity.

### 🔹 Formula:

<img width="277" height="63" alt="image" src="https://github.com/user-attachments/assets/db4749d9-5870-4791-a43b-1e617ceaadef" />


Where:

* ( P_i ) = probability of class i

### 🔹 Interpretation:

* Gini = 0 → Pure node
* Higher Gini → More impurity

👉 Used to choose the **best attribute for splitting**  (Page 37)

---

## 🔷 4. Steps in CART Algorithm

1. Start with full dataset (root node)
2. For each attribute:

   * Compute Gini Index
3. Choose attribute with **lowest Gini**
4. Split dataset into two subsets
5. Repeat recursively for each child node
6. Stop when:

   * Node becomes pure OR
   * Stopping criteria reached

---

## 🔷 5. Example from PDF (Play Cricket Dataset)

📍 **Page 36–37**

### 🔹 Dataset Attributes:

* Outlook (Sunny, Overcast, Rain)
* Temperature
* Humidity
* Wind
* Decision (Yes/No)

👉 Table 2.8.18 shows the dataset

---

### 🔹 Step 1: Calculate Gini for Outlook

From Table 2.8.19:

| Outlook  | Yes | No | Total |
| -------- | --- | -- | ----- |
| Sunny    | 2   | 3  | 5     |
| Overcast | 4   | 0  | 4     |
| Rain     | 3   | 2  | 5     |

---

### 🔹 Step 2: Compute Gini Values

<img width="777" height="303" alt="image" src="https://github.com/user-attachments/assets/eac68755-645e-4bb1-87d3-9516e88fe1b6" />


---

### 🔹 Step 3: Choose Best Split

* Attribute with **lowest Gini → Best split**
* Overcast gives **Gini = 0 (pure node)**

👉 So, **Outlook becomes root node**

---

### 🔹 Step 4: Recursive Splitting

* Overcast → directly “Yes” (pure)
* Sunny & Rain → further split using other attributes

👉 Continue process until all nodes are pure

---

## 🔷 6. Final Tree Structure (Concept)

From the PDF flow:

* Root → Outlook

  * Overcast → Yes
  * Sunny → further split
  * Rain → further split

👉 Final result: **Binary decision tree with Yes/No leaves**

---

## 🔷 7. Advantages of CART

* Simple and easy to understand
* Handles both classification & regression
* Works with large datasets
* No need for data normalization

---

## 🔷 8. Disadvantages

* Can overfit
* Sensitive to small data changes
* Greedy approach (not globally optimal)

---

## 🔷 9. Conclusion

* CART builds a **binary decision tree using Gini Index**
* It selects splits based on **minimum impurity**
* From the example, **Outlook is chosen as root** due to lowest Gini
* Widely used due to **simplicity and efficiency**

---

## 📌 Diagrams in Your PDF

* Dataset table → **Page 36**
* Gini calculation table → **Page 37**

---

If you want, I can:
✅ Draw the **final CART tree diagram step-by-step (exam drawing)**
✅ Give a **short 10-mark version**
✅ Provide **quick revision notes (1-page)**
