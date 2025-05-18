# ☕ Coffee Sales Report Dashboard

## Overview

This project presents a descriptive analysis of BeeBean Co.'s coffee sales, designed to provide insights into sales performance across product types, countries, and customers over the period of **2019 to 2022**.

---

## 📊 Dataset Summary

The dataset is provided in an Excel file comprising three worksheets:

* **Orders** – Contains transactional sales data.
* **Customers** – Includes customer demographic and loyalty details.
* **Products** – Holds information about the different coffee products sold.

---

## 🛠 Tools & Techniques

This project was developed using the following Excel functionalities:

* **VLOOKUP**: To connect datasets using key fields such as `Customer ID` and `Product ID`.
* **Pivot Tables**: To generate aggregate summaries of sales performance.
* **Slicers and Timeline**: For interactive filtering by coffee size, roast type, loyalty status, and date.

---

## 🔎 Key Insights

| Metric          
| --------------- 
![Screenshot 2025-05-18 221025](https://github.com/user-attachments/assets/27f988fe-3a72-4caa-adfe-08c3e24df372) |
![Screenshot 2025-05-18 221035](https://github.com/user-attachments/assets/ceb34bcb-2b7a-4826-b2da-a4fc9ac77fab)




### 📌 Top Highlights:
* **Excelsa** and **Liberica** coffees contributed the highest sales, exceeding \$12,000 each.
![Screenshot 2025-05-18 220951](https://github.com/user-attachments/assets/115fd5d7-060a-4cc1-bcbc-33118f463c31)
* **United States** had the highest country sales total, generating **\$35,639**, followed by Ireland and the UK.![Screenshot 2025-05-18 221003](https://github.com/user-attachments/assets/f189ce12-a44d-47bf-bfc8-06778ef01c24)
  
* The top 5 customers contributed significantly to overall revenue, with **Allis Wilmore** leading in purchases.
![Screenshot 2025-05-18 221012](https://github.com/user-attachments/assets/20ab45fa-c3aa-4b7e-bba9-068cf69367a4)

* Sales Trend Over Time
  
Sales varied across different coffee types from 2019 to 2022, showing fluctuating demand patterns throughout the period. Each coffee type experienced distinct peaks and troughs, highlighting changing customer preferences and possible seasonal or promotional impacts.


---

## 📈 Dashboard Preview

The visual dashboard includes:

* **Total Sales Over Time**: A monthly breakdown of sales from 2019 to 2022.
* **Sales by Coffee Type**: Comparing performance across coffee categories (Excelsa, Liberica, Arabica, Robusta).
* **Sales by Country**: Highlighting key markets contributing to revenue.
* **Top 5 Customers by Sales**: Identifying the highest-value customers.

---

## 🔗 VLOOKUP Formulas Used

These formulas were applied to join data and enrich the `Orders` worksheet:

```excel
=VLOOKUP(C2,customers!A:I,2,FALSE)
=IF(VLOOKUP(C2,customers!A:I,3,FALSE)=0, "Not Provided", VLOOKUP(C2,customers!A:I,3,FALSE))
=VLOOKUP(C2,customers!A:I,7,FALSE)
=VLOOKUP(D2,products!A:G,2,FALSE)
=VLOOKUP(D2,products!A:G,3,FALSE)
=VLOOKUP(D2,products!A:H,4,FALSE)
=VLOOKUP(D2,products!A:G,5,FALSE)
=VLOOKUP([@[Customer ID]],customers!A:I,9,FALSE)
=IF(J2="M","Middle",IF(J2="L","Light",IF(J2="D","Dark")))
=IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica"))))
Sales = L2 * E2
```

---

## 🧩 Interactivity Features

* **Slicers**: Allow filtering by `Loyalty Card Status`, `Roasted Type`, and `Size`.
* **Timeline**: Enables filtering across years (2019–2022) for time-based sales analysis.

---



---

## ✅Conclusion
The analysis reveals that BeeBean Co.'s revenue is heavily concentrated in a few key products and regions, with Excelsa and Liberica accounting for the majority of sales and the United States alone generating nearly 80% of total revenue. This indicates a high dependency on limited product lines and geographic markets.

To drive sustainable growth, BeeBean Co. should consider:

1. Expanding marketing efforts for underperforming products like Arabica and Robusta.

2. Exploring new international markets to diversify geographic revenue sources.

3. Leveraging top customer segments through loyalty programs or targeted upselling strategies.

4. These insights will help the company reduce risk, unlock new revenue streams, and enhance customer lifetime value.




Data Source:   https://github.com/mochen862/excel-project-coffee-sales/blob/main/coffeeOrdersData.xlsx
