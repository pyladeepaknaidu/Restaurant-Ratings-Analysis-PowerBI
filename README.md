# 🍽️ Restaurant Ratings Analysis using Power BI

## 📊 Project Overview

This project analyzes restaurant ratings, customer preferences, demographics, dining behavior, and restaurant characteristics using Microsoft Power BI.

The objective is to transform raw restaurant and consumer data into an interactive business intelligence dashboard and generate meaningful insights to support data-driven decision-making.

---

## 🛠️ Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Data Modeling
- Exploratory Data Analysis (EDA)
- Data Visualization
- Business Intelligence

---

## 📁 Dataset

The project contains multiple datasets related to restaurants, consumers, cuisines, and ratings.

### Main Tables

| Table | Description |
|---|---|
| Consumers | Consumer demographic and personal information |
| Consumer Preferences | Consumer cuisine preferences |
| Restaurants | Restaurant information and characteristics |
| Restaurant Cuisines | Cuisine information associated with restaurants |
| Ratings | Food, service, and overall restaurant ratings |

---

# 🧹 Data Cleaning & Transformation

Data cleaning and transformation were performed using **Power Query in Microsoft Power BI**.

## Steps to Import Data

1. Open Power BI Desktop.
2. Select **Get Data → More → Folder**.
3. Select the folder containing the dataset.
4. Click **Connect**.
5. Select **Transform Data**.
6. Load the required datasets.
7. Duplicate the required files where necessary.
8. Expand the **Binary** column to combine and import datasets.
9. Review and correct column data types.
10. Remove unnecessary columns.
11. Handle missing and inconsistent values.
12. Transform the data into analysis-ready formats.
13. Create calculated columns using DAX.
14. Prepare the cleaned data for data modeling and visualization.

---

# 🧮 DAX Calculated Fields

## Age Group

The Age column was transformed into meaningful age categories for demographic analysis.

```DAX
AgeGroup =
SWITCH(
    TRUE(),
    consumers[Age] <= 18, "Children and Adolescents",
    consumers[Age] <= 30, "Young Adults",
    consumers[Age] <= 45, "Adults",
    consumers[Age] <= 60, "Middle-aged Adults",
    "Seniors"
)
