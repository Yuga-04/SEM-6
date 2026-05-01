# OLAP Operations in Multidimensional Data Model (with Example)

## 1. Introduction

Online Analytical Processing (OLAP) is a technology used in data warehouses to analyze large volumes of data from different perspectives. OLAP uses a **multidimensional data model**, where data is represented as a **data cube** containing dimensions and measures.

* **Dimensions** represent perspectives such as **Time, Location, and Item**
* **Measures** represent numerical values such as **Sales Amount**

OLAP operations help users summarize, filter, and visualize data efficiently for decision-making.

---

# 2. OLAP Operations in Multidimensional Data Model

The major OLAP operations are:

1. Roll-Up
2. Drill-Down
3. Slice
4. Dice
5. Pivot (Rotate)

---

# 2.1 Roll-Up Operation

## Definition

Roll-up (also called drill-up) performs data aggregation by moving up a concept hierarchy or by reducing dimensions.

It summarizes detailed data into higher-level information.

---

## Example

Consider a sales data cube with the location hierarchy:

**City → State → Country**

### Sales Data by City

| City      | Sales |
| --------- | ----- |
| Toronto   | 200   |
| Vancouver | 150   |

### After Roll-Up (Country Level)

| Country | Sales |
| ------- | ----- |
| Canada  | 350   |

### Result

Roll-up aggregates city-level data into country-level data.

---

# 2.2 Drill-Down Operation

## Definition

Drill-down is the opposite of roll-up. It moves from summarized data to more detailed data.

It provides detailed information by descending the hierarchy.

---

## Example

Consider the hierarchy:

**Year → Quarter → Month → Day**

If sales data is summarized quarter-wise, drill-down shows month-wise details.

### Before Drill-Down

| Quarter | Sales |
| ------- | ----- |
| Q1      | 500   |

### After Drill-Down

| Month    | Sales |
| -------- | ----- |
| January  | 200   |
| February | 150   |
| March    | 150   |

### Result

Drill-down increases the level of detail.

---

# 2.3 Slice Operation

## Definition

The slice operation selects a single dimension value from the data cube to create a sub-cube.

It reduces one dimension of the cube.

---

## Example

Consider a sales cube with dimensions:

* Time
* Location
* Item

If we select:

**Time = Q1**

Then only sales data for Quarter 1 will be displayed.

### Slice Result

| Location  | Item     | Sales |
| --------- | -------- | ----- |
| Toronto   | Computer | 200   |
| Vancouver | Phone    | 150   |

### Result

Slice extracts data for a specific dimension value.

---

# 2.4 Dice Operation

## Definition

The dice operation selects data based on multiple dimensions and conditions, creating a smaller sub-cube.

---

## Example

### Selection Conditions

* Location = Toronto or Vancouver
* Time = Q1 or Q2
* Item = Computer or Phone

### Dice Result

| Location  | Time | Item     | Sales |
| --------- | ---- | -------- | ----- |
| Toronto   | Q1   | Computer | 200   |
| Vancouver | Q2   | Phone    | 150   |

### Result

Dice operation allows flexible data selection using multiple conditions.

---

# 2.5 Pivot (Rotate) Operation

## Definition

Pivot (or rotate) changes the orientation of the data cube to provide an alternative view of data.

It rotates the data axes for better visualization.

---

## Example

### Original View

| Location  | Computer | Phone |
| --------- | -------- | ----- |
| Toronto   | 200      | 150   |
| Vancouver | 180      | 120   |

### After Pivot

| Item     | Toronto | Vancouver |
| -------- | ------- | --------- |
| Computer | 200     | 180       |
| Phone    | 150     | 120       |

### Result

Pivot changes the presentation of data without changing the actual data.

---

# 3. Conclusion

OLAP operations such as **Roll-Up, Drill-Down, Slice, Dice, and Pivot** help users analyze multidimensional data efficiently. These operations allow users to summarize, filter, and visualize data from different perspectives, making OLAP an essential tool in **data warehouse analysis and decision support systems**.
