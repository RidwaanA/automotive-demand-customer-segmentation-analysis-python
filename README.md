# 🚗 Automotive Demand Trends & Customer Purchase Behavior Analysis

# Project Overview
This project analyzes automotive customer data to identify vehicle demand patterns, buyer segments, and purchase drivers.

Using Python (Pandas, Seaborn, Matplotlib), the analysis provides actionable insights to support market entry strategy, product positioning, and demand-driven planning.

# Business Problem
Austo is expanding into the U.S. market and needs to understand:

- Which car types are most in demand
- Who the target customers are
- What factors influence purchase decisions

# Dataset
- ~1,600 car buyers
- 14 features including:
  Make, Price, Salary, Total_salary, Age, Gender, Profession, Marital_status
- 3 car categories: Hatchback, Sedan, SUV

# Tools & Technologies
- Python (Pandas, NumPy)
- Data Visualization (Seaborn, Matplotlib)
- Jupyter Notebook

# Data Processing / Methodology
- Validated dataset (no missing values or duplicates)
- Performed univariate, bivariate, and multivariate analysis
- Conducted correlation and distribution analysis
- Built customer segmentation based on age, income, and purchase behavior

# Key Code Highlights
### Demand distribution by car type
df['Make'].value_counts(normalize=True)

### Customer segmentation by age and car type
df.groupby(['Make'])['Age'].mean()

### Income vs purchase behavior
sns.relplot(data=df, x='Price', y='Total_salary', col='Make', col_order=['Hatchback', 'Sedan', 'SUV')

### Correlation analysis
plt.figure(figsize=(15,7))
sns.heatmap(df.corr(), annot=True, vmin=-1, vmax=1, fmt='.2f', cmap='Spectral');
plt.show()

# Visualization / Dashboard
- Distribution plots for age, salary, and car prices
- Car demand by category (Hatchback, Sedan, SUV)
- Correlation heatmaps (income, age, price)
- Multivariate segmentation plots (Age vs Income vs Car Type)

# Key Insights
### Demand Trends
- Hatchback dominates market (56%), followed by Sedan (29%), SUV (15%)
- SUVs are highest priced, Hatchbacks are most affordable
### Customer Segmentation
- Hatchback buyers:
  → Younger (22–30), lower income
- Sedan buyers:
  → Mid-age (28–45), mid-income
- SUV buyers:
  → Older (35–60), highest income
### Income & Purchase Behavior
- Strong positive relationship between:
  → Age → Salary → Car Price
  Higher-income customers prefer premium vehicles (SUVs)
### Behavioral Patterns
- Male customers prefer Hatchbacks
- Female customers prefer Sedans
- SUV buyers typically have no house loans

# Recommendations
- Focus on Hatchback and Sedan segments (85% of demand)
- Target customers aged 22–45 for volume growth
- Position SUVs as premium offerings for high-income segments
- Tailor marketing strategies:
  → Hatchbacks → younger, price-sensitive buyers
  → Sedans → mid-income professionals (especially female segment)
  → SUVs → high-income, financially stable buyers
