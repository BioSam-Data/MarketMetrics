# MarketMetrics: A Deep Dive into Delivery Delays and E-commerce Efficiency

🔗 **Read the full analysis on Medium**: [How I Uncovered Hidden Delivery Gaps in Brazil's E-Commerce](https://biosam-data.medium.com/how-i-uncovered-hidden-delays-and-delivery-gaps-in-a-multi-million-order-dataset-23290d2e84c0)

---

## 🗺️ Brazilian State Abbreviations 
For reference in visualizations:
| Abbreviation | State Name          |
|--------------|---------------------|
| AC           | Acre                |
| AL           | Alagoas             |
| AM           | Amazonas            |
| AP           | Amapá               |
| BA           | Bahia               |
| CE           | Ceará               |
| DF           | Distrito Federal    |
| ES           | Espírito Santo      |
| GO           | Goiás               |
| MA           | Maranhão            |
| MG           | Minas Gerais        |
| MS           | Mato Grosso do Sul  |
| MT           | Mato Grosso         |
| PA           | Pará                |
| PB           | Paraíba             |
| PE           | Pernambuco          |
| PI           | Piauí               |
| PR           | Paraná              |
| RJ           | Rio de Janeiro      |
| RN           | Rio Grande do Norte |
| RO           | Rondônia            |
| RR           | Roraima             |
| RS           | Rio Grande do Sul   |
| SC           | Santa Catarina      |
| SE           | Sergipe             |
| SP           | São Paulo           |
| TO           | Tocantins           |

---

Welcome to **MarketMetrics**, my data analysis project exploring delivery dynamics within Brazil's booming e-commerce sector. This isn’t just a dashboard dump or code showcase—this is the result of digging deep into raw data to answer a simple but important question:

> **Are online deliveries happening on time? And if not, why?**

This project captures my journey through cleaning, exploring, and analyzing real transactional data to uncover patterns in delivery performance and customer satisfaction.

---

## 🧾 Dataset Overview
The dataset comes from the public Olist Brazilian e-commerce platform and includes:

- **Orders** with purchase, approval, and delivery timestamps
- **Customer info** with geolocation
- **Items, payments, and products** with pricing and shipping costs
- **Reviews** with feedback and satisfaction scores

Altogether, this rich dataset provides tens of thousands of real-world records to analyze the delivery pipeline.

---

## 🧹 Step 1: Data Cleaning & Preparation
I started with merging multiple tables to form a complete view of each order. Key steps included:

- **Merging datasets** on order_id to combine timestamps, items, reviews, and products
- **Handling missing values**, especially in reviews and product dimensions
- **Creating new columns** like `delivery_delay`, `delay_status`, `delivery_time`, and `delivery_speed`
- **Standardizing dates** and filtering out orders that lacked key timestamps

I preserved both a **long version** (1 row per item) and a **collapsed version** (1 row per order) for flexibility.

---

## 📊 Step 2: Exploratory Data Analysis (EDA)
With clean data, I turned to visual storytelling. Here’s what I uncovered:

### 1. **Delivery Delays Are Real**
Many orders were delivered **later than estimated**, but some were **surprisingly early** too. I plotted a bar chart of delivery delay categories to understand the balance.

**Insight:** While over 50% of orders arrived on time or early, a significant portion missed their mark.

### 2. **Delivery Speed Is All Over the Place**
We examined the actual number of days it took to deliver each order. The histogram showed a heavy concentration in the 0–20 day range, with some outliers.

**Insight:** Delivery speed varies greatly, making it hard to promise consistency.

### 3. **State-by-State Breakdown**
Using the customer's state, we compared average delivery times.

**Insight:** Some states like SP and RJ enjoy faster deliveries, while more remote states like RR and AM suffer from delays.

### 4. **Customer Sentiment Mirrors Delivery Timing**
We compared review scores against delivery delay status. The result? Late deliveries almost always result in lower ratings.

**Insight:** Timely delivery strongly correlates with customer satisfaction.

---

## 🔍 Final Thoughts & Recommendations
- **Invest in Logistics for Remote States**: Delays in northern states could be tackled with regional hubs or partner carriers.
- **Use Delay Predictions Proactively**: Orders expected to be late should trigger notifications and maybe discounts.
- **Monitor Delivery Speed Variability**: Reducing inconsistencies can boost customer trust.
- **Customer Reviews as Feedback Loops**: Delivery performance should be a KPI tied to customer sentiment tracking.

---

## 🛠️ Tech Stack
- **Python** (Pandas, Seaborn, Matplotlib)
- **Jupyter Notebook**
- **Git & GitHub** for version control and publishing

---

## 📁 Repository Contents
- `MarketMetrics (Delivery Delay Analysis).ipynb` – Full code and analysis
- `datasets/` – Cleaned CSVs used in the project
- `charts/` – Visualizations from multiple analysis in the project
- `README.md` – You’re here!

---

## 📬 Feedback?
If you have suggestions or want to collaborate on future analysis or dashboarding, feel free to reach out. You can also check out the live version on my portfolio:

👉 [biosam-data.github.io/portfolio-website](http://biosam-data.github.io/portfolio-website)

Thanks for reading and feel free to ⭐ the repo if it helped you!

— BioSam 🧠📦
