# Task-4-Integration-With-Python

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: VAYUGANDLA VENKATA SIVA SAI SUSHANTH

*INTERN ID*: CITS0D731

*DOMAIN*: POWER BI

*DURATION*: 8 WEEKS

*MENTOR*: NEELA SANTOSH KUMAR

# 🐍 Power BI Internship – Task 4: Integration with Python

## 📌 Internship Task Description

**Objective:**  
Use Python within Power BI to perform advanced data analysis or visualizations using existing data.

**Task Statement:**  
> Use Python or R scripts within Power BI to perform advanced data analysis or visualizations. Deliverable: A Power BI report showcasing the use of Python or R.

This is the fourth and final task in the 4-week internship program and focuses on integrating external scripting languages (Python in this case) with Power BI, allowing greater flexibility for analytics and visualizations beyond built-in tools.

---

## 📁 Dataset Used

- **File:** `Financial Sample (1).xlsx`
- **Source:** Microsoft Sample Dataset
- **Format:** Excel Workbook (.xlsx)
- **Size:** 700+ rows of transactional sales data

**Key Columns:**
- Product, Segment, Country, Date, Month, Year  
- Units Sold, Sale Price, Profit, Sales, Gross Sales, COGS

---

## 🧰 Tools & Libraries Used

| Tool / Library          | Purpose                                      |
|-------------------------|----------------------------------------------|
| **Power BI Desktop**    | Primary BI tool for visualizations           |
| **Python (in Power BI)**| External scripting for visuals & analysis    |
| **matplotlib**          | Data plotting library for static charts      |
| **seaborn**             | Enhanced statistical visualizations          |
| **pandas**              | Data manipulation and aggregation            |

> ✅ Installed all required libraries using `pip install matplotlib seaborn pandas` from Power BI’s Python environment.

---

## 🧪 Python Visuals Created

The following Python visualizations were embedded inside Power BI:

### 1. 🔹 Sales by Product (Bar Chart)

- import matplotlib.pyplot as plt
- import seaborn as sns

- dataset.columns = [col.replace(" ", "_").replace(".", "_") for col in dataset.columns]
- plt.figure(figsize=(10, 6))
- sns.barplot(x="Product", y="Sales", data=dataset, estimator=sum, ci=None, palette="Paired")
- plt.title("Total Sales by Product")
- plt.xticks(rotation=45)
- plt.tight_layout()
- plt.show()

---

### 2. 🔹 Profit vs Sales (Scatter Plot with Segment Hue)

- plt.figure(figsize=(8, 6))
- sns.scatterplot(x="Sales", y="Profit", hue="Segment", data=dataset)
- plt.title("Profit vs Sales by Segment")
- plt.tight_layout()
- plt.show()

---

### 3. 🔹 Monthly Sales Trend (Line Plot)

- dataset["Month_Name"] = pd.Categorical(dataset["Month_Name"], categories=["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"], ordered=True)
- monthly_sales = dataset.groupby("Month_Name")["Sales"].sum().reset_index()
- 
- plt.figure(figsize=(10, 5))
- sns.lineplot(x="Month_Name", y="Sales", data=monthly_sales, marker='o')
- plt.title("Monthly Sales Trend")
- plt.xticks(rotation=45)
- plt.tight_layout()
- plt.show()

---
## 🧠 Key Learnings

- How to set up Python inside Power BI
- Importing and prepping data using pandas
- Creating compelling visuals with seaborn and matplotlib
- Visual customization in Python for enhanced storytelling
- Debugging script-based errors (e.g., data type issues)

## 📌 Conclusion
- This task showed me the power of extending Power BI’s native capabilities with scripting. Using Python enabled better control over data processing and allowed the creation of custom visuals like grouped bar charts, trend lines, and correlation plots. I now understand how data scientists and analysts can combine Python’s strengths with Power BI’s interactivity to build more insightful and advanced dashboards. This experience prepares me for building hybrid analytical solutions in the real world.
---

## OUTPUT of the task 4:
