Readme 
# Lead Scoring with Machine Learning for Marketing Campaigns

## 📌 Project Overview
This project aims to build a **Lead Scoring model** using Machine Learning to predict the probability that a customer will respond to a marketing campaign.

Using historical demographic, behavioral, and campaign interaction data, the model helps marketing teams **prioritize leads**, **optimize campaign targeting**, and **allocate budget more efficiently**.


---

## 🎯 Business Problem
Marketing teams often run campaigns across large customer databases, while only a small fraction of customers actually respond.

**Key question:**
> Can we predict which customers are more likely to respond to a marketing campaign based on historical data?

---

## 📊 Dataset
- Public marketing campaign dataset
- 2,240 customers
- 29 original features
- Data includes:
  - Demographics
  - Purchase behavior
  - Channel interactions
  - Previous campaign responses

**Target variable:**
- `Response`  
  - 1 = customer responded to the campaign  
  - 0 = customer did not respond  

---

## 🧹 Data Cleaning
The following steps were applied:
- Removed missing values in `Income` (24 records)
- Removed extreme income outliers to avoid distortion
- Converted customer enrollment date to datetime format

**Final dataset:**  
- 2,215 customers  
- High data integrity with minimal data loss (~1%)

---

## 🧠 Feature Engineering
Raw variables were transformed into meaningful marketing signals:

- `Age` – derived from year of birth
- `Customer_Tenure_Days` – length of customer relationship
- `Total_Spend` – total monetary value across product categories
- `Total_Purchases` – total number of purchases across channels
- `Total_Accepted_Campaigns` – number of previously accepted campaigns
- `Total_Children` – household context indicator

These features improve interpretability and business relevance.

---

## 🔍 Exploratory Data Analysis (EDA)
Key findings:
- Only ~15% of customers responded to the campaign (realistic marketing imbalance)
- Customers who accepted previous campaigns were **3–5x more likely** to respond again
- Responders tend to:
  - Have lower recency (more recent purchases)
  - Spend more
  - Have longer customer tenure

---

## 🤖 Modeling Approach
- Problem type: **Binary Classification**
- Model: **Logistic Regression**
- Data split:
  - 75% training
  - 25% testing
  - Stratified to preserve class imbalance
- Feature scaling using `StandardScaler`
- Class imbalance handled with `class_weight="balanced"`

Logistic Regression was chosen for its **interpretability** and strong alignment with marketing decision-making.

---

## 📈 Model Insights (Marketing Interpretation)
The most influential drivers of campaign response were:

**Positive impact:**
- Customer tenure
- Previous campaign acceptance
- Online purchase behavior
- High-value product spending

**Negative impact:**
- High recency (long time since last purchase)
- Strong preference for in-store purchases
- Households with teenagers

The model learns **behavioral patterns**, not just demographics.

---

## 💼 Business Actions Enabled
The model can be directly translated into marketing actions:

- **Lead prioritization:** focus sales and budget on high-probability customers
- **Personalized campaigns:** different messaging for loyal, deal-seeking, and inactive customers
- **Channel optimization:** adjust strategy for store-focused vs digital customers
- **Budget efficiency:** avoid over-investing in low-propensity segments

---

## 🚀 Conclusion
This project demonstrates how Machine Learning can move beyond prediction and deliver **actionable marketing insights**, connecting data, modeling, and real business decisions.

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Google Colab

