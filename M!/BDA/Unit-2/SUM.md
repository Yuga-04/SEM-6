# CART Algorithm – Detailed Example Explanation (Play Cricket Dataset)

## 1. What is CART?

CART stands for:

> **Classification And Regression Tree**

It is a **Decision Tree algorithm** used for:

* **Classification** → predicting categories like Yes/No
* **Regression** → predicting numerical values

In this example, CART is used for **classification**.

---

# 2. Important Idea Behind CART

CART creates a **binary tree** by repeatedly:

1. Selecting the **best attribute**
2. Splitting the dataset into smaller groups
3. Making groups purer and purer

To measure purity, CART uses:

# ✅ Gini Index

---

# 3. Dataset Used (Play Cricket Example)

The dataset decides whether to **Play Cricket** based on weather conditions.

| Outlook  | Temperature | Humidity | Wind   | Play Cricket |
| -------- | ----------- | -------- | ------ | ------------ |
| Sunny    | Hot         | High     | Weak   | No           |
| Sunny    | Hot         | High     | Strong | No           |
| Overcast | Hot         | High     | Weak   | Yes          |
| Rain     | Mild        | High     | Weak   | Yes          |
| Rain     | Cool        | Normal   | Weak   | Yes          |
| Rain     | Cool        | Normal   | Strong | No           |
| Overcast | Cool        | Normal   | Strong | Yes          |
| Sunny    | Mild        | High     | Weak   | No           |
| Sunny    | Cool        | Normal   | Weak   | Yes          |
| Rain     | Mild        | Normal   | Weak   | Yes          |
| Sunny    | Mild        | Normal   | Strong | Yes          |
| Overcast | Mild        | High     | Strong | Yes          |
| Overcast | Hot         | Normal   | Weak   | Yes          |
| Rain     | Mild        | High     | Strong | No           |

---

# 4. Goal of CART

We want to build a tree that predicts:

# 👉 “Play Cricket = Yes or No”

using weather attributes.

---

# 5. Step 1 – Start with Root Node

Initially, the **entire dataset** becomes the root node.

Total records = **14**

Count classes:

* Yes = 9
* No = 5

Now CART checks each attribute to find:

# 👉 Which attribute gives the PUREST split?

---

# 6. Step 2 – Calculate Gini Index

---

# What is Gini Index?

Gini Index measures impurity.

## Formula

[
Gini = 1 - \sum (P_i)^2
]

Where:

* (P_i) = probability of each class

---

# Interpretation

| Gini Value | Meaning       |
| ---------- | ------------- |
| 0          | Pure node     |
| High value | Mixed classes |

---

# 7. Calculate Gini for Attribute = Outlook

The attribute **Outlook** has 3 values:

* Sunny
* Overcast
* Rain

We split dataset based on these.

---

# A) Outlook = Sunny

Records:

| Result |
| ------ |
| No     |
| No     |
| No     |
| Yes    |
| Yes    |

Count:

* Yes = 2
* No = 3
* Total = 5

---

## Calculate Probabilities

[
P(Yes)=\frac{2}{5}
]

[
P(No)=\frac{3}{5}
]

---

## Gini(Sunny)

[
Gini = 1 - \left(\frac{2}{5}\right)^2 - \left(\frac{3}{5}\right)^2
]

[
= 1 - \frac{4}{25} - \frac{9}{25}
]

[
= 1 - \frac{13}{25}
]

[
= \frac{12}{25}
]

[
= 0.48
]

---

# B) Outlook = Overcast

Records:

| Result |
| ------ |
| Yes    |
| Yes    |
| Yes    |
| Yes    |

Count:

* Yes = 4
* No = 0

---

## Gini(Overcast)

[
Gini = 1 - (1)^2 - (0)^2
]

[
= 0
]

# ✅ Perfectly Pure Node

All examples are “Yes”.

---

# C) Outlook = Rain

Records:

| Result |
| ------ |
| Yes    |
| Yes    |
| No     |
| Yes    |
| No     |

Count:

* Yes = 3
* No = 2

---

## Gini(Rain)

[
Gini = 1 - \left(\frac{3}{5}\right)^2 - \left(\frac{2}{5}\right)^2
]

[
= 1 - \frac{9}{25} - \frac{4}{25}
]

[
= 1 - \frac{13}{25}
]

[
= \frac{12}{25}
]

[
= 0.48
]

---

# 8. Weighted Gini for Outlook

Now combine all subsets.

Formula:

[
Gini(Outlook)=\sum \frac{|D_i|}{|D|} \times Gini(D_i)
]

Where:

* (|D_i|) = subset size
* (|D|) = total dataset size

---

## Substitute Values

[
= \frac{5}{14}(0.48) + \frac{4}{14}(0) + \frac{5}{14}(0.48)
]

[
= 0.171 + 0 + 0.171
]

[
= 0.342
]

# ✅ Final Gini(Outlook) = 0.342

---

# 9. Compare with Other Attributes

Similarly calculate Gini for:

* Temperature
* Humidity
* Wind

Suppose results are:

| Attribute   | Gini  |
| ----------- | ----- |
| Outlook     | 0.342 |
| Temperature | 0.44  |
| Humidity    | 0.367 |
| Wind        | 0.428 |

---

# 10. Choose Best Attribute

Rule:

# 👉 Lowest Gini = Best Split

So:

# ✅ Outlook becomes ROOT NODE

because:

[
0.342
]

is the minimum.

---

# 11. Create First Level of Tree

```text
                Outlook
              /    |     \
         Sunny  Overcast  Rain
```

---

# 12. Analyze Each Branch

---

# A) Overcast Branch

All outputs = Yes

So directly make leaf node.

```text
Overcast → Yes
```

No further splitting needed.

---

# B) Sunny Branch

Data:

| Humidity | Result |
| -------- | ------ |
| High     | No     |
| High     | No     |
| High     | No     |
| Normal   | Yes    |
| Normal   | Yes    |

Observe:

* High → all No
* Normal → all Yes

So Humidity perfectly separates data.

---

## Split Sunny Using Humidity

```text
Sunny
   |
Humidity
 /      \
High   Normal
 No      Yes
```

---

# C) Rain Branch

Data:

| Wind   | Result |
| ------ | ------ |
| Weak   | Yes    |
| Weak   | Yes    |
| Strong | No     |
| Weak   | Yes    |
| Strong | No     |

Observe:

* Weak → mostly Yes
* Strong → No

So Wind becomes best split.

---

## Split Rain Using Wind

```text
Rain
   |
 Wind
 /     \
Weak  Strong
 Yes    No
```

---

# 13. Final CART Decision Tree

```text
                     Outlook
                 /      |       \
             Sunny   Overcast    Rain
               |         |         |
          Humidity      Yes       Wind
           /    \                 /   \
        High  Normal           Weak  Strong
         No      Yes            Yes    No
```

---

# 14. How Prediction Happens

Suppose new data:

| Outlook | Humidity | Wind |
| ------- | -------- | ---- |
| Sunny   | High     | Weak |

Traverse tree:

* Outlook = Sunny
* Go to Humidity
* Humidity = High

Prediction:

# 👉 Play Cricket = No

---

# 15. Why Overcast Became Pure?

Because:

All 4 records under Overcast are Yes.

So:

[
Gini = 0
]

Meaning:

# ✅ No impurity

# ✅ Perfect classification

---

# 16. Why CART Uses Binary Splits?

CART internally converts decisions into binary form:

Example:

```text
Outlook = Sunny ?
Yes / No
```

This is why CART is called:

# ✅ Binary Decision Tree

---

# 17. Stopping Conditions in CART

Tree stops growing when:

* Node becomes pure
* No attributes left
* Minimum samples reached
* Maximum depth reached

---

# 18. Advantages in This Example

✅ Easy to understand
✅ Gives clear decision rules
✅ Fast prediction
✅ Handles categorical data well

---

# 19. Disadvantages

❌ Can overfit
❌ Small data changes may create different trees
❌ Greedy algorithm (local optimum only)

---

# 20. Final Conclusion

In this example:

* CART used **Gini Index**
* Calculated impurity for all attributes
* Selected **Outlook** as root because it had minimum Gini
* Repeated splitting recursively
* Produced a final decision tree for predicting cricket play decision

The final tree successfully classifies weather conditions into:

# 👉 Play Cricket = Yes / No
