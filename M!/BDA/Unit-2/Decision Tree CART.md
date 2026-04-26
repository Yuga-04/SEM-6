# ✅ CART Decision Tree – DATA WEATHER (15 Marks)

---

## 🔷 1. Given Dataset

| Day | Outlook  | Temperature | Humidity | Play |
| --- | -------- | ----------- | -------- | ---- |
| D1  | Sunny    | Hot         | High     | No   |
| D2  | Sunny    | Hot         | High     | No   |
| D3  | Overcast | Hot         | High     | Yes  |
| D4  | Rain     | Mild        | High     | Yes  |
| D5  | Rain     | Cool        | Normal   | Yes  |

---

## 🔷 2. CART Concept

* CART uses **Gini Index** to split data
* Produces a **binary decision tree**
* Selects attribute with **minimum Gini impurity**

---

## 🔷 3. Gini Formula

```
Gini = 1 - (P(Yes)^2 + P(No)^2)
```

---

## 🔷 4. Step 1: Gini of Dataset

Total = 5
Yes = 3, No = 2

```
Gini(D) = 1 - [(3/5)^2 + (2/5)^2]
         = 1 - (9/25 + 4/25)
         = 12/25
         = 0.48
```

---

## 🔷 5. Step 2: Evaluate Splits

### 🔹 Attribute: Outlook

#### Sunny (D1, D2)

* Yes = 0, No = 2

```
Gini = 1 - (0^2 + 1^2) = 0
```

#### Overcast (D3)

* Yes = 1

```
Gini = 0
```

#### Rain (D4, D5)

* Yes = 2

```
Gini = 0
```

👉 **Weighted Gini = 0 → Best Split**

---

### 🔹 Attribute: Temperature (for reference)

* Mixed classes → higher Gini
  👉 Not optimal

---

### 🔹 Attribute: Humidity (for reference)

* Mixed classes → higher Gini
  👉 Not optimal

---

## 🔷 6. Best Attribute

```
Root Node = Outlook
```

---

## 🔷 7. Decision Tree Construction

```
            Outlook
           /   |    \
       Sunny Overcast Rain
        /        |       \
      No        Yes      Yes
```

---

## 🔷 8. Final Rules

* If Outlook = Sunny → Play = No
* If Outlook = Overcast → Play = Yes
* If Outlook = Rain → Play = Yes

---

## 🔷 9. Conclusion

* CART selects **Outlook** due to **minimum Gini (0)**
* All nodes are **pure → no further splitting needed**
* Final tree perfectly classifies the dataset

---

## 📌 Exam Diagram (Draw This)

```
        Outlook
      /    |     \
   Sunny Overcast Rain
     No     Yes     Yes
```

---

