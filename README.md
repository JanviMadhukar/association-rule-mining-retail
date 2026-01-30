

# 📦 Market Basket Analysis – Online Retail Dataset

## 📌 Project Overview

This project implements **Market Basket Analysis** on an online retail transaction dataset to uncover hidden purchasing patterns among customers.
Using the **Apriori algorithm**, the project identifies **frequently co-purchased products** and generates **association rules** ranked by **support, confidence, and lift**, enabling actionable business insights.

---

## 🎯 Objectives

* Analyze customer purchasing behavior
* Identify frequently bought product combinations
* Generate and rank association rules for strategic decision-making

---

## 📂 Dataset

* **Source:** Online Retail Transactions Dataset
* **Format:** CSV
* **Description:** Transaction-level retail data containing invoice numbers, product codes, quantities, and product descriptions

---

## 🛠️ Tools & Technologies

* **Language:** Python
* **Libraries Used:**

  * pandas
  * numpy
  * mlxtend
  * matplotlib
* **Algorithm:** Apriori (Association Rule Mining)

---

## 🔁 Workflow

### 1️⃣ Load Transaction Data

Retail transaction logs are loaded from a CSV file using **pandas**.

### 2️⃣ Data Cleaning

The dataset is cleaned through the following steps:

* Remove canceled orders (invoice numbers starting with `'C'`)
* Remove rows with missing product descriptions
* Remove invalid or non-product stock codes
* Remove non-positive quantity values
* Remove duplicate products within the same invoice

### 3️⃣ Basket Creation

* Group products by invoice number
* Convert transactions into a binary (one-hot encoded) format using **TransactionEncoder**

### 4️⃣ Frequent Itemset Generation

* Apply the **Apriori algorithm** to generate frequent itemsets
* A minimum support threshold is applied to filter meaningful itemsets

### 5️⃣ Association Rule Mining

* Generate association rules based on:

  * Support
  * Confidence
  * Lift
* Sort and rank rules by lift, confidence, and support

### 6️⃣ Final Output

* Extract the **Top 10 association rules**
* Export results to CSV format for easy interpretation

---

## 📊 Output

* **File:** `outputs/top10_rules.csv`

**Columns Included:**

* Antecedents
* Consequents
* Support
* Confidence
* Lift

---

## 📁 Project Structure

```
association-rule-mining-retail/
├─ data/
│  └─ online_retail.csv
├─ notebooks/
│  └─ market_basket_analysis.ipynb
├─ outputs/
│  └─ top10_rules.csv
├─ README.md
├─ requirements.txt
└─ .gitignore
```

---

## ▶️ How to Run

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Open the Jupyter Notebook:

```bash
jupyter notebook notebooks/market_basket_analysis.ipynb
```

Run all cells to reproduce the results.

---

## ✅ Deliverables Checklist

✔ Jupyter Notebook with itemset mining and rule generation
✔ Cleaned transaction data
✔ Apriori-based association rules
✔ Sorted Top 10 rules with key metrics
✔ Exported CSV output

---

## 📌 Key Takeaway

This project demonstrates how **association rule mining** can be effectively used to extract meaningful insights from retail transaction data.
The results help businesses understand **product affinities**, **cross-selling opportunities**, and **customer buying patterns**, enabling data-driven decision-making.

---

