# 🛍️ Customer Behavior Analysis  
!()[6616c33c-1478-4b09-851b-1dfba6a1639c.jpeg]
## 📌 Project Overview  

The **Customer Behavior Analysis** provides actionable insights into purchasing patterns, preferences, and behavior. By examining key metrics such as churn, return rates, and payment methods, businesses can make data-driven decisions to improve customer satisfaction and revenue growth.  

This dashboard includes interactive visuals and KPIs designed for effective decision-making.  

---

## 📊 Dashboard Features and Visual Insights  

### **1️⃣ Total Revenue and Consumer Metrics**  

- **Total Revenue (552M):** Represents total earnings generated across all transactions.  
- **Total Consumers (202K):** The number of unique customers who engaged with the platform.  
- **Active Consumers (162K):** Consumers actively making purchases.  

**Insight:**  
The business has a strong revenue base, but only **80% of consumers** are active, leaving **20% inactive**.  

**Recommendation:**  
- Implement re-engagement campaigns (emails, discounts) to target inactive customers.  
- Introduce loyalty programs to retain active consumers.  

---

### **2️⃣ Churn Analysis**  

- **19.94% Churn Rate**  
- **162K Active Consumers**  
- **40K Inactive Consumers**  

**Insight:**  
While a churn rate below 20% is reasonable, understanding why **40K customers** become inactive can help improve retention. Common reasons may include dissatisfaction with products or first-time buyers who do not return.  

**Recommendation:**  
- Conduct feedback surveys to understand dissatisfaction drivers.  
- Use predictive analytics to identify at-risk customers and provide personalized offers.  

---

### **3️⃣ Return Rate Analysis**  

- **49.79% Failed Transactions**  
- **50.21% Successful Transactions**  

**Insight:**  
A nearly equal split between successful and failed transactions highlights potential issues in the purchasing process, such as payment failures or product cancellations.  

**Recommendation:**  
- Improve product quality and descriptions to align with customer expectations.  
- Streamline the return process and provide tutorials to minimize failed transactions.  

---

### **4️⃣ Payment Methods by Sales**  

- **Credit Card (226K):** Most popular payment method.  
- **PayPal (179K):** Widely used, indicating customer preference for digital wallets.  
- **Crypto (54K):** Lowest adoption rate.  

**Insight:**  
Credit cards dominate, but the rising use of digital wallets like PayPal highlights the need for secure, flexible payment options.  

**Recommendation:**  
- Promote crypto payment discounts to encourage adoption.  
- Ensure seamless integration of digital wallets to enhance convenience.  

---

### **5️⃣ Monthly Sales Trends**  

- **Consistent Sales (2020–2022):** Average of 41.3M per month.  
- **2023 Sales Decline:** Dropped to 29.6M.  

**Insight:**  
The decline in 2023 suggests reduced customer engagement or market slowdown.  

**Recommendation:**  
- Launch seasonal campaigns or new product lines to re-engage customers.  

---

### **6️⃣ Leading Customers by Sales and Product Category**  

- **Top Customers:**  
  - Michael Johnson (Books, 22K)  
  - Michael Smith (Clothing, 18K)  

**Insight:**  
High-value customers primarily purchase books and clothing, driving significant revenue.  

**Recommendation:**  
- Focus on VIP programs for top customers.  
- Expand offerings in high-performing categories.  

---

### **7️⃣ Sales by Product Category**  

- **Clothing and Books (46M each):** Top categories.  
- **Electronics and Home (31M each):** Lagging behind.  

**Insight:**  
Clothing and books dominate sales, while electronics and home categories present growth opportunities.  

**Recommendation:**  
- Invest in marketing campaigns for underperforming categories.  
- Bundle electronics and home products to drive cross-category purchases.  

---

## 🔍 Conclusions  

1. **Customer Retention Needs Attention:** A churn rate of 19.94% highlights untapped potential in inactive customers.  
2. **Failed Transactions Impact Revenue:** Addressing a high failure rate of 49.79% is critical for improving customer satisfaction.  
3. **Consistent Revenue Streams:** Clothing and books are reliable revenue drivers despite a sales drop in 2023.  

**Key Recommendations:**  
- Re-engage inactive customers through targeted campaigns.  
- Optimize the purchasing process to reduce transaction failures.  
- Diversify focus on electronics and home products for growth.  

---

## 🛠️ Technical Implementation Details  
![](Screenshot(110)_040328.png)
Screenshot (110)_040328.png
### **1️⃣ Power BI Visuals Used**  

- **Pie Charts:**  
  - Churn Analysis (Active vs. Inactive Customers).  
  - Return Rate (Successful vs. Failed Transactions).  
- **Bar Charts:**  
  - Payment Methods by Sales.  
  - Sales by Product Category.  
- **Line Charts:**  
  - Monthly Sales Trends.  
- **Column Charts:**  
  - Leading Customers by Sales and Product Category.  

---

### **2️⃣ Conditional Columns (Power Query Editor)**  

- **Churn Rate Calculation:**  
  ```Power Query
  - *Churn Status*:
    - If `Churn` = 0, return "Active"
    - If `Churn` = 1, return "Inactive"
- *Age Category*
    - If `Age` `≤``30`, `return "Gen Z"`
    - If `Age` ≤ 50, return "Middle Age"
    - If `Age` ≤ 70, return "Adult"

### **3️⃣ Measures

	•	Total Revenue: SUM(Sales[Amount])
	•	Churn Rate: DIVIDE(COUNTROWS(Churn[Inactive Customers]), COUNTROWS(Customers))
	•	Return Rate: DIVIDE(COUNTROWS(Returns[Failed Transactions]), COUNTROWS(Sales))
	•	Calendar Date (Month, Year, Quarter, Day):

### **4️⃣ Data Transformation Techniques
Power Query Editor: Cleaned and reshaped data for analysis.
Relationships: Built relationships between purchase date and calender returns datasets for accurate analysis 
