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
- ## 🏗️ System Architecture  

This project follows a structured **data analytics pipeline**, transforming raw e-commerce data into actionable insights through cleaning, transformation, and visualization layers.  

---

### 🔷 Architecture Diagram  

```mermaid
flowchart LR

A[Raw Dataset (SHEIN Kaggle Data)]
--> B[Data Cleaning & Preprocessing]

B --> C[Feature Engineering]
C --> D[Pricing Funnel Logic]

D --> E[Segmented Analysis]
E --> F[Visualization Layer]

F --> G[Insights & Recommendations]

%% Sub-details
B --> B1[Handle Missing Values]
B --> B2[Standardize Columns]
B --> B3[Fix Data Types]

C --> C1[Discount Calculation]
C --> C2[Stock Normalization]

D --> D1[All Products]
D --> D2[Discounted]
D --> D3[High Discount]
D --> D4[In Stock]

E --> E1[Category Analysis]
E --> E2[Color Analysis]
E --> E3[Size Analysis]

F --> F1[Plotly Funnel Chart]
F --> F2[Conversion Metrics]

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
<img width="1739" height="469" alt="Screenshot 2026-04-27 at 8 52 01 AM" src="https://github.com/user-attachments/assets/47576379-5759-4b9f-a038-75499751752e" />

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
