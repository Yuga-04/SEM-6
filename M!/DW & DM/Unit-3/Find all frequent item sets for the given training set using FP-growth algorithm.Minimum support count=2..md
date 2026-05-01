<img width="725" height="304" alt="image" src="https://github.com/user-attachments/assets/f64ae59c-7863-44ee-8bce-6e1eb4ef0bea" />
# ✅ FP-Growth Frequent Itemsets – 15 Marks Answer

## Given Transactions

<table>
<tr>
<th>TID</th>
<th>Items</th>
</tr>

<tr>
<td>T1</td>
<td>Pen, Notebook, Eraser</td>
</tr>

<tr>
<td>T2</td>
<td>Pen, Notebook</td>
</tr>

<tr>
<td>T3</td>
<td>Notebook, Eraser</td>
</tr>

<tr>
<td>T4</td>
<td>Pen, Marker</td>
</tr>

<tr>
<td>T5</td>
<td>Pen, Notebook, Eraser</td>
</tr>
</table>

<p><b>Minimum support count = 2</b></p>

---

# Step 1: Count Support of Each Item

<table>
<tr>
<th>Item</th>
<th>Support Count</th>
</tr>

<tr>
<td>Pen</td>
<td>4</td>
</tr>

<tr>
<td>Notebook</td>
<td>4</td>
</tr>

<tr>
<td>Eraser</td>
<td>3</td>
</tr>

<tr>
<td>Marker</td>
<td>1</td>
</tr>
</table>

<p>Since minimum support = 2, Marker is removed.</p>

<p><b>Frequent 1-itemsets:</b></p>

<p>{Pen} = 4</p>

<p>{Notebook} = 4</p>

<p>{Eraser} = 3</p>

---

# Step 2: Arrange Items in Descending Order

<p><b>Order:</b></p>

<p>Pen, Notebook, Eraser</p>

<p>After removing Marker:</p>

<table>
<tr>
<th>TID</th>
<th>Ordered Items</th>
</tr>

<tr>
<td>T1</td>
<td>Pen, Notebook, Eraser</td>
</tr>

<tr>
<td>T2</td>
<td>Pen, Notebook</td>
</tr>

<tr>
<td>T3</td>
<td>Notebook, Eraser</td>
</tr>

<tr>
<td>T4</td>
<td>Pen</td>
</tr>

<tr>
<td>T5</td>
<td>Pen, Notebook, Eraser</td>
</tr>
</table>

---

# Step 3: Construct FP-Tree

<pre>
null
├── Pen:4
│   └── Notebook:3
│       └── Eraser:2
└── Notebook:1
    └── Eraser:1
</pre>

---

# Step 4: Find Frequent Itemsets

## 1-Itemsets

<table>
<tr>
<th>Itemset</th>
<th>Support</th>
</tr>

<tr>
<td>{Pen}</td>
<td>4</td>
</tr>

<tr>
<td>{Notebook}</td>
<td>4</td>
</tr>

<tr>
<td>{Eraser}</td>
<td>3</td>
</tr>
</table>

---

## 2-Itemsets

<table>
<tr>
<th>Itemset</th>
<th>Support</th>
</tr>

<tr>
<td>{Pen, Notebook}</td>
<td>3</td>
</tr>

<tr>
<td>{Pen, Eraser}</td>
<td>2</td>
</tr>

<tr>
<td>{Notebook, Eraser}</td>
<td>3</td>
</tr>
</table>

---

## 3-Itemsets

<table>
<tr>
<th>Itemset</th>
<th>Support</th>
</tr>

<tr>
<td>{Pen, Notebook, Eraser}</td>
<td>2</td>
</tr>
</table>

---

# ✅ Final Frequent Itemsets

<p>{Pen}, {Notebook}, {Eraser}</p>

<p>{Pen, Notebook}, {Pen, Eraser}, {Notebook, Eraser}</p>

<p>{Pen, Notebook, Eraser}</p>

---

# Conclusion

<p>
Using FP-Growth with minimum support count 2, all frequent itemsets are found.
Marker is removed because its support count is only 1.
The frequent itemsets are Pen, Notebook, Eraser and their valid combinations.
</p>
