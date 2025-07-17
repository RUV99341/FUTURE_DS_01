# 📊 E-commerce Sales Dashboard (Power BI)

This project presents an interactive **Power BI dashboard** for analyzing an e-commerce dataset from 2009–2011. It provides insights into sales performance, customer behavior, and returns — helping businesses make informed decisions.

---

## 🔍 Key Insights

- 📈 **Top-selling products** by total quantity and revenue
- 🌍 **Region-wise performance** using map visuals
- 📆 **Sales trends** across months and years
- 📦 **Return analysis** by product, customer type, and country
- 🧑‍🤝‍🧑 **Customer segmentation** (based on presence of Customer ID)

---

## 🧠 Measures Used (DAX Examples)

```dax
Total Revenue = SUMX('Sales', 'Sales'[Quantity] * 'Sales'[Price])
Return Quantity = CALCULATE(SUM('Sales'[Quantity]), 'Sales'[Quantity] < 0)
Return Value = CALCULATE(SUMX('Sales', 'Sales'[Quantity] * 'Sales'[Price]), 'Sales'[Quantity] < 0)
Return Rate = DIVIDE(ABS([Return Quantity]), [Total Sales Qty])
