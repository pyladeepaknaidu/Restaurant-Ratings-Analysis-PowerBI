# 🍽️ Restaurant Ratings Analysis using Power BI

## 📊 Project Overview

This project analyzes restaurant ratings, customer preferences, demographics, dining behavior, and restaurant characteristics using Microsoft Power BI.

The goal is to transform raw restaurant and consumer data into an interactive dashboard and generate meaningful business insights.

## 🛠️ Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Data Modeling
- Exploratory Data Analysis
- Data Visualization
- Business Intelligence

## 📁 Dataset

The project contains data related to:

- Consumers
- Consumer Preferences
- Restaurants
- Restaurant Cuisines
- Ratings

## 🧹 Data Cleaning

Data cleaning and transformation were performed using Power Query.

### Steps

1. Imported datasets into Power BI.
2. Connected to the dataset folder using **Get Data → Folder**.
3. Loaded and transformed the required files.
4. Expanded binary files where required.
5. Checked and corrected data types.
6. Removed unnecessary columns.
7. Handled missing and inconsistent values.
8. Transformed data into analysis-ready formats.
9. Created calculated columns using DAX.
10. Prepared the data for modeling and visualization.

## 🧮 DAX Calculated Fields

### Age Group

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
