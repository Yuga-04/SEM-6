Here is a **15-mark exam-ready answer strictly from your PDF** 👇

---

# ✅ Sampling of Data Streams (15 Marks)

---

## 🔷 1. Introduction

Sampling in data streams is the process of selecting a **representative subset of data** from a continuous and potentially infinite stream.

* Streams are **unbounded**
* Cannot store entire data
* Sampling helps in:

  * Reducing memory usage
  * Performing analysis efficiently

👉 It provides a **statistically meaningful subset** of the stream. 

---

## 🔷 2. Need for Sampling

Sampling is required because:

* Data streams are **infinite**
* Storage is **limited**
* Full processing is **expensive**

✔ Helps in:

* Estimation
* Approximate analytics
* Quick decision making

---

## 🔷 3. Key Questions in Sampling

According to the document, sampling involves solving:

1. How to traverse a stream efficiently?
2. How to select elements during traversal?
3. How to maintain a **finite sample from infinite data**? 

---

## 🔷 4. Sampling Technique – Bernoulli Sampling

The PDF explains **Bernoulli Sampling** as a simple and effective method.

---

## 🔷 5. Bernoulli Sampling Method

### 🔹 Basic Idea

* Each element in the stream is selected with probability **p**
* Probability range:

<img width="187" height="55" alt="image" src="https://github.com/user-attachments/assets/fc086367-2ef0-455b-8846-7f2b5e50b2d8" />


---

### 🔹 Working

For each incoming element:

* Toss a **biased coin**

  * Probability of heads = **p**
  * Probability of tails = **1 – p**

✔ If **heads** → include element in sample
✔ If **tails** → ignore element

---

### 🔹 Sample Size

If total elements processed = **N**

<img width="338" height="36" alt="image" src="https://github.com/user-attachments/assets/868ea54b-94cb-46e9-8d4c-781cd4144980" />


---

## 🔷 6. Optimized Sampling (Skip Technique)

Instead of checking every element:

* Calculate how many elements to **skip**
* Based on probability formula:

<img width="286" height="82" alt="image" src="https://github.com/user-attachments/assets/728f3ae3-6791-4644-a81e-b558caf2e609" />


Where:

* (U) = random number between 0 and 1

✔ Improves efficiency
✔ Reduces computation overhead 

---

## 🔷 7. Example Concept

* Suppose probability of selection = **5% (p = 0.05)**
* Only some elements are selected randomly
* Others are skipped

✔ Ensures:

* Randomness
* Representative sampling

---

## 🔷 8. Advantages

* Simple to implement
* Works in **real-time streams**
* Memory efficient
* Produces **statistically valid samples**

---

## 🔷 9. Limitations

* Sample size is **not fixed**
* May miss rare events
* Depends on randomness

---

## 🔷 10. Applications

* Data analysis
* Monitoring systems
* Approximate query processing
* Big data analytics

---

## 🔷 11. Conclusion

Sampling is essential in stream processing to handle **infinite and high-speed data**.

The **Bernoulli sampling technique**:

* Selects elements probabilistically
* Maintains a manageable dataset
* Enables efficient and scalable analysis

---
