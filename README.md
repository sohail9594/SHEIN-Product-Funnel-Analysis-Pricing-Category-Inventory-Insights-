# SHEIN-Product-Funnel-Analysis-Pricing-Category-Inventory-Insights-
 
### Pricing • Discount Strategy • Inventory Insights  

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Plotly](https://img.shields.io/badge/Plotly-Visualization-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 🧠 Overview  
This project analyzes pricing strategies in an e-commerce dataset (SHEIN) using a **funnel-based approach**.  

The goal is to track how products move across pricing stages and identify **drop-offs that impact product visibility and potential conversions**.  

The analysis is extended using **segmentation by category, color, and size** to uncover deeper pricing and inventory patterns.

---

## 🎯 Objectives  
- Build a **pricing funnel** across product lifecycle stages  
- Identify **key drop-offs and inefficiencies** in discount strategy  
- Perform **segmented analysis** (category, color, size)  
- Generate **actionable business insights**  

---

## 🗂️ Dataset  
- 📦 ~1000 products  
- 📊 Features:
  - `initial_price`
  - `final_price`
  - `discount`
  - `category`
  - `color`
  - `size`
  - `in_stock`

---

## ⚙️ Tech Stack  
- **Python** (Pandas, NumPy)  
- **Visualization**: Plotly, Matplotlib  
- **Environment**: Jupyter Notebook / Google Colab  

---

## 🔄 Methodology  

### 1️⃣ Data Cleaning  
- Handled missing values  
- Standardized `in_stock` column  
- Ensured pricing consistency  

---

### 2️⃣ Funnel Definition  

| Stage | Condition |
|------|----------|
| All Products | Full dataset |
| Discounted | `final_price < initial_price` |
| High Discount | ≥30% discount |
| In Stock | Available inventory |

✔️ Each stage is **sequentially filtered** from the previous stage  

---

### 3️⃣ Funnel Results  

| Stage           | Count | Conversion % |
|-----------------|------|--------------|
| All Products    | 1000 | 100%         |
| Discounted      | 609  | 60.9%        |
| High Discount   | 107  | 10.7%        |
| In Stock        | 107  | 10.7%        |

---

## 📊 Visualization  

### 🔻 Pricing Funnel Chart  
![Funnel Chart](screenshots/funnel_chart.png)

> Replace with your actual screenshot  
> (Save your Plotly chart as PNG and place in `/screenshots` folder)

---

### 📉 Conversion Drop-off  
- Major drop: **Discounted → High Discount (~82% drop)**  
- Indicates limited availability of high-discount products  

---

## 🔍 Segmented Analysis  

Funnel extended across:  

- 🧥 **Category** → Apparel, Accessories, etc.  
- 🎨 **Color** → Discount distribution across colors  
- 📏 **Size** → Inventory + discount relationship  

---

## 💡 Key Insights  

- ~61% products are discounted  
- Only ~18% of discounted products qualify as **high discount**  
- **Biggest bottleneck**: Discount → High Discount stage  
- All high-discount items are in stock → **inventory is not limiting**  

---

## 📈 Business Impact  

- Increase **high-discount product share**  
- Improve **visibility of discounted items**  
- Optimize pricing using **category-level strategies**  

---

## 🚀 Future Improvements  

- 📅 Time-series analysis (seasonality)  
- 💰 Sales data integration (true conversion funnel)  
- 📊 Dashboard (Tableau / Power BI)  
- 🤖 ML-based price optimization  

---

## ▶️ How to Run  

```bash
pip install pandas numpy matplotlib plotly
