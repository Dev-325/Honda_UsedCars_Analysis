# Honda_UsedCars_Analysis

## 📌 Objective
This project focuses on cleaning and visualizing used Honda car sales data to extract 
insights about pricing trends, model popularity, and other key attributes. 
The workflow includes data preprocessing, transformation, and visual representation to support business and buyer decision-making.

---

## 📂 Dataset Information

- **Rows:** 999  
- **Columns:** 6 (initially)
- **Fields:**
  - `Year` - Year of car manufacturing
  - `kms Driven` - Total kilometers driven
  - `Fuel Type` - Petrol/Diesel/CNG
  - `Suspension` - Manual/Automatic
  - `Price` - Selling price in INR
  - `Car Model` - Full model name

---

## 🧹 Data Cleaning Steps

1. **Missing Data:**  
   - Checked for nulls using `.isnull()`  
   - Dropped any null rows with `dropna(inplace=True)`

2. **Standardizing Formats:**
   - Converted `Price` to float (in INR)  
   - Removed commas from `Price` and `kms Driven`  
   - Converted `kms Driven` to float  
   - Extracted clean `Model Name` from `Car Model`

3. **Outlier Handling:**
   - Visualized through boxplots  
   - Used domain knowledge and visual trends to analyze dispersion

4. **Duplicates:**  
   - Not explicitly present; assumed uniqueness from `Car Model` and other variables

---

## 🔁 Feature Engineering

- Created a new column `Model Name` by extracting the core model from `Car Model`
- Converted `Price` from 'Lakh' and 'Crore' to integer INR
- Cleaned and converted `kms Driven` to numeric format

---

## 📊 Visualizations

1. **Top 10 Most Sold Honda Models**  
   Barplot showing most frequently sold car models.

2. **Price vs Kilometer Driven (By Fuel Type)**  
   Scatterplot showing correlation between price and usage based on fuel type.

3. **Boxplot: Price Distribution of Top 20 Models**  
   Visualized pricing spread and outliers per car model.

4. **Car Sales Over Years**  
   Histogram and KDE plot to show sales volume by year.

5. **Average Price by Manufacturing Year**  
   Line plot showcasing how price varies by model year.

6. **Suspension Type Distribution**  
   Barplot for comparing the number of cars sold with manual vs. automatic transmission.

7. **Categorical Distribution: Fuel Type & Suspension Type**  
   Comparative barplots for categorical variables.

---

## 🧠 Insights

- **City 1.5 S MT** was the most sold Honda model in the dataset.
- Manual transmission has a slightly higher frequency than automatic.
- Petrol cars dominate the dataset; diesel and CNG have low representation.
- Prices decline with older models and high kilometers driven.
- Price outliers exist in high-end models like CR-V and Civic.

---

## 📁 Libraries Used

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
