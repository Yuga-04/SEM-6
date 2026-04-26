# ✅ Naïve Bayes Classifier with Real-World Example (15 Marks)

---

## 🔷 1. Introduction

Naïve Bayes is a **supervised classification algorithm** based on **Bayes’ Theorem**.

* It is called *“naïve”* because it assumes that all features are **independent**
* It is widely used in:

  * Email spam detection
  * Sentiment analysis
  * Medical diagnosis

👉 Mentioned as a classification algorithm in your PDF (Page 23)

---

## 🔷 2. Bayes’ Theorem

**Formula:**

```
P(C|X) = (P(X|C) × P(C)) / P(X)
```

**Where:**

* P(C|X) → Posterior probability
* P(X|C) → Likelihood
* P(C) → Prior probability
* P(X) → Evidence

---

## 🔷 3. Naïve Bayes Formula

```
P(C|X) ∝ P(C) × P(x1|C) × P(x2|C) × ... × P(xn|C)
```

👉 Multiply probabilities of each feature assuming independence

---

## 🔷 4. Real-World Example: Email Spam Classification

### 🔹 Problem:

Classify an email as **Spam** or **Not Spam**

---

### 🔹 Training Dataset

| Email | Offer | Money | Class    |
| ----- | ----- | ----- | -------- |
| E1    | Yes   | Yes   | Spam     |
| E2    | Yes   | No    | Spam     |
| E3    | No    | Yes   | Spam     |
| E4    | No    | No    | Not Spam |
| E5    | No    | Yes   | Not Spam |

---

### 🔹 Step 1: Prior Probabilities

```
P(Spam) = 3/5
P(NotSpam) = 2/5
```

---

### 🔹 Step 2: Likelihood Probabilities

**For Spam:**

```
P(Offer=Yes | Spam) = 2/3
P(Money=Yes | Spam) = 2/3
```

**For Not Spam:**

```
P(Offer=Yes | NotSpam) = 0
P(Money=Yes | NotSpam) = 1/2
```

---

### 🔹 Step 3: New Email

```
Offer = Yes
Money = Yes
```

---

### 🔹 Step 4: Apply Naïve Bayes

**For Spam:**

```
P(Spam|X) ∝ (3/5) × (2/3) × (2/3)
          = 12/45
```

**For Not Spam:**

```
P(NotSpam|X) ∝ (2/5) × 0 × (1/2)
             = 0
```

---

### 🔹 Step 5: Final Decision

```
P(Spam|X) > P(NotSpam|X)
```

✅ Email is classified as **Spam**

---

## 🔷 5. Why Naïve Bayes Works Well

* Handles **large datasets efficiently**
* Works well for **text classification**
* Requires **less training data**
* Fast and simple

---

## 🔷 6. Advantages

* Easy to implement
* Fast computation
* Works well with high-dimensional data
* Performs well in real-world problems

---

## 🔷 7. Disadvantages

* Assumes **feature independence** (not always true)
* Zero probability problem (can be solved using Laplace smoothing)
* Less accurate than complex models

---

## 🔷 8. Applications

* Spam detection
* Sentiment analysis
* Medical diagnosis
* Document classification

---

## 🔷 9. Conclusion

Naïve Bayes is a **simple yet powerful probabilistic classifier** that uses Bayes’ theorem.
It effectively classifies data using probability calculations, as shown in the example.

---

