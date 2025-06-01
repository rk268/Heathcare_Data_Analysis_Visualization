
# 🩺 Primary Care Diabetes Analytics Dashboard – Power BI

![Main Dashboard Screenshot](https://drive.google.com/uc?export=view&id=1_W5S8YKSYxD0_NCpe81q4HuZkxUhoryo)

## 📘 Introduction

Welcome to the **Primary Care Diabetes Analytics Dashboard**, a comprehensive data visualization project designed in **Power BI**. This project simulates a real-world healthcare scenario using a curated diabetes dataset, ideal for professionals and learners in data science, analytics, and public health.

The purpose of this dashboard is to **identify trends, risk factors, and population segments** susceptible to diabetes using visually rich, interactive reports. The entire process—from data ingestion, transformation, DAX modeling, to visualization—was engineered to reflect industry-standard analytics practices in a **hospital's primary care setting**.

---

## 📦 Dataset Overview

- **Source**: Kaggle (Pima Indians Diabetes Database)
- **Patients**: 179 unique records
- **Attributes**:
  - Pregnancies
  - Glucose Level
  - Blood Pressure
  - Skin Thickness
  - Insulin
  - BMI
  - Diabetes Pedigree Function
  - Age
  - Diabetes Outcome (binary target)

The dataset was cleaned and enriched with derived fields like **BMI Categories**, **Age Bins**, and **Risk Categories** using Power BI DAX logic.

---

## 🧠 Objectives

- Perform **predictive analytics** by classifying patients into risk buckets (Low, Medium, High).
- Explore **correlations** between glucose, BMI, and age with diabetes occurrence.
- Build an **interactive dashboard** using cards, charts, slicers, and tables.
- Deliver business insights tailored for **clinical decision-making and public health research**.
- Demonstrate proficiency in **DAX**, **data modeling**, and **interactive storytelling**.

---

## 🔧 Technical Stack

- **Power BI Desktop** for dashboard creation
- **DAX** for measures, calculated columns, and conditional logic
- **Power Query Editor** for data transformation
- **Google Drive** for image hosting
- **Markdown** for this documentation

---

## 📊 Dashboard Features

### 🔹 KPIs
- **Total Patients**: 179
- **Average BMI**: 27.50
- **Average Glucose**: 116.35
- **Average Pregnancies**: 3.79

### 🔹 Visual Components
- Donut Chart: Risk of Getting Diabetes
- Line Chart: Average Glucose by Age
- Horizontal Bar Chart: Blood Pressure by Age
- Matrix Table: Age and BMI-wise Blood Pressure
- Gauge Chart: Diabetes Risk %
- Slicers: Age Bins, BMI Category, Pregnancies Range

---

## 🧮 DAX Logic

```DAX
-- BMI Category
BMI Category = 
SWITCH(TRUE(),
  [BMI] < 18.5, "Underweight",
  [BMI] >= 18.5 && [BMI] < 25, "Normal",
  [BMI] >= 25 && [BMI] < 30, "Overweight",
  [BMI] >= 30, "Obese"
)

-- Age Bins
Age Bin = 
SWITCH(TRUE(),
  [Age] < 30, "Less than 30",
  [Age] >= 30 && [Age] <= 50, "30-50",
  [Age] > 50, "High Age"
)

-- Diabetes Risk Category
Risk Category = 
SWITCH(TRUE(),
  [Glucose] > 140 || [BMI] > 35, "High",
  [Glucose] > 110, "Medium",
  TRUE(), "Low"
)
```

---

## 🔍 Exploratory Insights

- **Glucose vs. Age**: Clear spike in glucose levels post age 50, with max values peaking around 159–161.
- **BMI vs. Risk**: Patients classified as Obese show a disproportionately high diabetes risk.
- **Pregnancies Correlation**: Women with more than 5 pregnancies show higher average glucose levels.
- **Blood Pressure Trends**: Highest average BP (79) found in the 50–60 age group.

---

## 🧱 Data Model

![Data Model View](https://drive.google.com/uc?export=view&id=1zUolcs96PEEueIliBNYN7tdy31EzdBtS)

- Single table model
- Derived columns via Power Query & DAX
- Optimized for slicer performance and quick filter response

---

## 🎛️ User Interactions

![Dropdown Filter Screenshot](https://drive.google.com/uc?export=view&id=1sWsmf5jOvGBcgxKIqmv9iOplN5xM85ZA)

- **Dropdown menus**: Select Age Bins or BMI Categories
- **Sliders**: Filter by Pregnancies
- **Cross-filters**: Interact with one chart to filter others in real time
- **Reset Filters**: Button to bring dashboard to default state

---

## 💼 Business Relevance

This dashboard mimics the exact needs of:

- **Hospital Analysts**: Prioritize patient outreach based on diabetes risk
- **Nurses/Doctors**: Quickly view high-risk demographics
- **Healthcare Executives**: Monitor risk trends across time and optimize treatment protocols
- **Data Scientists**: Test early intervention models with visual guidance

---

## 📈 Impact & Learning

Through this project, I:

- Designed a **multi-dimensional, story-driven dashboard**
- Used DAX to **generate non-trivial logic and derived attributes**
- Gained hands-on experience in **healthcare reporting and data transformation**
- Simulated **data product thinking** for operational BI in hospitals

---

## 📎 Resources

- [Main Dashboard Screenshot](https://drive.google.com/file/d/1_W5S8YKSYxD0_NCpe81q4HuZkxUhoryo/view?usp=sharing)
- [Dropdown Interaction](https://drive.google.com/file/d/1sWsmf5jOvGBcgxKIqmv9iOplN5xM85ZA/view?usp=sharing)
- [Data Model Architecture](https://drive.google.com/file/d/1zUolcs96PEEueIliBNYN7tdy31EzdBtS/view?usp=sharing)
- [Dataset on Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

---

## 📬 Contact

If you're working on healthcare analytics or BI solutions and want to connect, reach out:

- 💼 LinkedIn: [Your LinkedIn](https://www.linkedin.com/in/rupak-kulkarni/)
- 📧 Email: rupakkul97@gmail.com

---


