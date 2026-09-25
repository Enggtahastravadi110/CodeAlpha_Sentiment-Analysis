# CodeAlpha Data Analytics Internship — EDA & Data Visualization

## 📌 Overview
This repository covers two tasks completed as part of the **CodeAlpha Data Analytics Internship**, both built on the same food delivery order dataset:
- **Task: Exploratory Data Analysis (EDA)** — understanding the dataset's structure, trends, and data quality
- **Task: Data Visualization** — turning those findings into a clear, portfolio-ready set of visuals (Python notebook + Power BI dashboard)

## 📊 Dataset
- **File:** `Order_delivery.csv`
- **Size:** 100,002 food delivery orders across 7 Egyptian cities
- **Fields:** item, quantity, price, order/delivery timestamps, restaurant, driver vehicle, payment method, delivery distance, traffic level, order status

## 🛠 Tools & Libraries
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Power BI Desktop (DAX measures, slicers, KPI cards)

## 📁 Project Structure
```
├── Codealpha_Task1_Polished.ipynb        # EDA notebook
├── CodeAlpha_DataVisualization.ipynb     # Visualization notebook
├── Codealpha_Task2.pbix                  # Power BI dashboard
├── README.md
└── images/                               # Chart screenshots and dashboard exports
```

---

## Part 1 — Exploratory Data Analysis

### ❓ Questions Answered
1. Which food items and cities generate the most orders and revenue?
2. What is the typical delivery duration, and does traffic level affect it?
3. Which payment methods and vehicle types are most common?
4. Are there outliers in delivery distance or duration that need investigation?
5. How reliable is the delivery process (cancelled vs. delivered orders)?

### 🔍 Process
1. Data overview — shape, data types, summary statistics
2. Data cleaning — checked for nulls and duplicates (none found)
3. Item & city analysis — revenue and order volume by category
4. Hypothesis testing — tested whether traffic level affects delivery duration
5. Outlier detection — boxplots on distance and duration, with interpretation of flagged points
6. Correlation analysis — heatmap across quantity, price, duration, and distance

### 📈 Key Findings
- **Top performer:** Shawarma leads in both quantity ordered and revenue generated
- **City demand:** Zagazig has the highest order count and revenue, but demand is fairly evenly spread across all 7 cities
- **Delivery time:** averages ~37–38 minutes, ranging from 15 to 60 minutes
- **Traffic has no measurable effect** on delivery duration — nearly identical averages (~37–38 min) across Low, Medium, and High traffic, rejecting the initial hypothesis
- **No strong correlations** between quantity, price, duration, and distance — these fields vary independently
- **Payment and vehicle use** are split almost evenly across categories
- **Order reliability:** ~85% delivered, ~10% cancelled — flagged as an area worth further investigation
- **Data quality:** no missing values, no duplicates, no genuine anomalies in distance/duration

---

## Part 2 — Data Visualization

### 📈 What's Visualized
- Total revenue by item
- Order volume by city
- Delivery duration distribution
- Average delivery duration by traffic level
- Order status breakdown (Delivered / Cancelled / In Transit)
- Payment method split
- Driver vehicle split
- Delivery distance vs. duration relationship
- Daily order volume trend

### 🧭 Key Metrics (Power BI Dashboard)
- **Total Revenue:** 26.89M
- **Average Delivery Time:** 37.52 minutes
- **Cancellation Rate:** 9.81%

### 📖 Data Story
1. **What's driving revenue** — items and cities are close in performance; no single item or city dominates
2. **How reliable delivery is** — consistent delivery windows (15–60 min); traffic level does not meaningfully affect delivery time
3. **Who uses the platform** — payment methods and vehicle types are each split almost exactly evenly
4. **The one metric to watch** — a ~10% cancellation rate is the clearest area for further investigation

### 🔍 Power BI Build Notes
- KPI cards use DAX measures for Total Revenue, Average Delivery Duration, and Cancellation Rate
- Slicers on `City` and `Traffic_Level` allow interactive filtering
- Scatter chart (distance vs. duration) uses "Don't summarize" on both axes to plot one point per order, with reduced marker size/opacity for readability at scale

---

## 📷 Visuals
*(Add screenshots to the `images/` folder — recommended: duration histogram, traffic vs. duration boxplot, correlation heatmap, full dashboard view, revenue by item chart, distance vs. duration scatter)*

```
![Duration Distribution](images/duration_distribution.png)
![Traffic vs Duration](images/traffic_boxplot.png)
![Correlation Heatmap](images/correlation_heatmap.png)
![Dashboard Overview](images/dashboard_overview.png)
![Revenue by Item](images/revenue_by_item.png)
![Distance vs Duration](images/scatter_distance_duration.png)
```

## 🚀 How to Run

**EDA / Visualization notebooks:**
1. Place `Order_delivery.csv` in the same folder as the notebooks
2. Install dependencies:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
3. Open either `.ipynb` file in Jupyter and run all cells in order

**Power BI dashboard:**
1. Open `Codealpha_Task2.pbix` in Power BI Desktop
2. If prompted, point the data source to your local copy of `Order_delivery.csv`
3. Use the slicers to explore by city or traffic level

## 🎓 Internship
These projects were completed as part of the **CodeAlpha Data Analytics Internship**.
🔗 [CodeAlpha](https://www.codealpha.tech)
