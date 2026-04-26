Here is a **clean 15-mark answer strictly aligned with your document** 👇

---

# ✅ Counting Distinct Elements in a Data Stream

## 🔷 Flajolet–Martin (FM) Algorithm (15 Marks)

---

## 🔷 1. Introduction

In data streams, the **count-distinct problem** is to determine the number of **unique elements** present in a stream.

* Data streams are **large and continuous**
* Storing all elements is **not feasible in memory**
* Hence, we use **approximation algorithms**

👉 The **Flajolet–Martin (FM) Algorithm** is used to estimate the number of distinct elements efficiently. 

---

## 🔷 2. Problem Statement

Given a stream:

```
S = {x1, x2, x3, ..., xn}
```

Find:
👉 Number of **distinct (unique) elements**

---

## 🔷 3. Need for FM Algorithm

* Exact counting requires storing all elements → **O(n) space**
* Not suitable for streaming data

✔ FM Algorithm:

* Uses **hashing + probabilistic approach**
* Requires **O(log n) memory**
* Works in **single pass**

---

## 🔷 4. Key Idea

* Apply a **hash function** to each element
* Observe **number of trailing zeros** in binary form
* Larger number of trailing zeros → indicates more distinct elements

---

## 🔷 5. Algorithm Steps

### Step 1:

Initialize a **BITMAP array of size L** with all values = 0

---

### Step 2:

Select a **hash function h(x)**

---

### Step 3:

For each element **x in stream**:

* Compute hash value → `h(x)`
* Convert to binary → `bin(h(x))`
* Find position of **least significant 1-bit**
* Let position = **i**
* Set `BITMAP[i] = 1`

---

### Step 4:

After processing all elements:

* Find largest index **R** such that `BITMAP[R] = 1`

---

### Step 5:

Estimate distinct elements:

<img width="286" height="82" alt="image" src="https://github.com/user-attachments/assets/bccaa555-729b-4bdf-a8c0-c756f532a6f3" />


Where:

* (\phi ≈ 0.77351) (correction factor)

---

## 🔷 6. Example

Given stream:

```
S = {4, 2, 5, 9, 1, 6, 3, 7}
```

Hash function:

```
h(x) = (3x + 1) mod 32
```

Trailing zeros obtained:

```
{0, 0, 1, 1, 1, 0, 4, 2}
```

👉 Maximum trailing zeros:

```
R = 4
```

👉 Estimated distinct elements:

<img width="102" height="56" alt="image" src="https://github.com/user-attachments/assets/5ce93d2e-5de1-4f62-afe2-dbfce1fe6671" />


✔ Approximate answer = **16** 

---

## 🔷 7. Improving Accuracy

* Use **multiple hash functions**
* Take **average of results**
* Use **bucketing + median**

✔ Reduces error and improves reliability

---

## 🔷 8. Advantages

* Very **less memory usage**
* **Fast and efficient**
* Works in **single scan**
* Suitable for **big data streams**

---

## 🔷 9. Limitations

* Gives **approximate result**
* Accuracy depends on:

  * Hash functions
  * Number of trials

---

## 🔷 10. Conclusion

The **Flajolet–Martin algorithm** is an efficient and scalable method for counting distinct elements in a data stream using:

* Hashing
* Bit patterns
* Probabilistic estimation

It is widely used in **real-time analytics and big data systems**.

---
