Here is a **15-mark answer format** for your question.

---

# Email Spam Classification Using Feature Vector

## 1. Introduction

Email spam classification is a machine learning task used to identify whether an email is **spam or not spam**. In this approach, emails are converted into **feature vectors** based on the presence or absence of specific keywords.

---

# 2. Given Email Record

Email Content:
**“Get free gift cards now!”**

Sender: **[spam@example.com](mailto:spam@example.com)**

Subject Line: **“Exclusive Offer”**

Label: **1 (Spam)**

---

# 3. Selected Keywords (Features)

To classify the email, the following keywords are used:

1. **free**
2. **win**
3. **offer**

Each keyword is represented using **binary values**:

* **1 → keyword present**
* **0 → keyword absent**

---

# 4. Feature Extraction

From the email content and subject line:

| Keyword | Presence                | Value |
| ------- | ----------------------- | ----- |
| free    | Present in content      | 1     |
| win     | Not present             | 0     |
| offer   | Present in subject line | 1     |

---

# 5. Feature Vector Representation

The email can be represented as a **feature vector**:

[
X = (1, 0, 1)
]

Where:

* **X₁ = 1 → free is present**
* **X₂ = 0 → win is absent**
* **X₃ = 1 → offer is present**

---

# 6. Label Representation

The label indicates whether the email is spam or not.

[
y = 1
]

Where:

* **1 → Spam**
* **0 → Not Spam**

---

# 7. Final Data Representation

| Feature Vector | Label |
| -------------- | ----- |
| (1,0,1)        | 1     |

This means the email contains the keywords **free** and **offer**, which are commonly associated with spam emails.

---

# 8. Conclusion

By converting email text into a **feature vector**, machine learning algorithms such as **Naive Bayes, Logistic Regression, or Decision Trees** can analyze patterns in keywords and accurately classify emails as **spam or non-spam**.

---

✅ This structured explanation is suitable for a **15-mark exam answer**.
