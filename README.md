# 🚗 Automotive Demand Trends & Customer Purchase Behavior Analysis

## Project Overview
This project analyzes automotive customer data to identify vehicle demand patterns, buyer segments, and purchase drivers.

Using Python (Pandas, Seaborn, Matplotlib), the analysis provides actionable insights to support market entry strategy, product positioning, and demand-driven planning.

## Business Problem
Austo is expanding into the U.S. market and needs to understand:

- Which car types are most in demand
- Who the target customers are
- What factors influence purchase decisions

## Dataset
- ~1,600 car buyers
- 14 features including:
  `Make`, `Price`, `Salary`, `Total_salary`, `Age`, `Gender`, `Profession`, `Marital_status`
- 3 car categories: Hatchback, Sedan, SUV

## Tools & Technologies
- **Python** (Pandas, NumPy, Seaborn, Matplotlib)
- **Jupyter Notebook**
- **Tableau**

## Data Processing / Methodology
- Validated dataset (no missing values or duplicates)
- Performed univariate, bivariate, and multivariate analysis
- Conducted correlation and distribution analysis
- Built customer segmentation based on age, income, and purchase behavior

## Key Code Highlights
```python
// Demand distribution by car type
df['Make'].value_counts(normalize=True)
```
```python
// Customer segmentation by age and car type
df.groupby(['Make'])['Age'].mean()
```
```python
// Income vs purchase behavior
sns.relplot(data=df, x='Price', y='Total_salary', col='Make', col_order=['Hatchback', 'Sedan', 'SUV')
```
```python
// Correlation analysis
plt.figure(figsize=(15,7))
sns.heatmap(df.corr(), annot=True, vmin=-1, vmax=1, fmt='.2f', cmap='Spectral');
plt.show()
```

## Visualization / Dashboard
**Python (Jupyter Notebook)**
- 📌 Distribution plots for age, salary, and car prices
- 📌 Multivariate segmentation plots (age vs income vs car type)
- 📌 Car demand by category (Hatchback, Sedan, SUV)
<img width="573" height="306" alt="Bar chart_Gender count1" src="https://github.com/user-attachments/assets/44c6cdee-ddcb-4f78-b8e9-faa0531e6a12" />

- 📌 Correlation heatmaps (income, age, price)
<img width="904" height="525" alt="Heat map_Numerical features3" src="https://github.com/user-attachments/assets/0f60af90-4b57-4ad8-a0c3-937cee9c356c" />

---

**Tableau**
- 📌 Highlight table: Car make distribution across the dataset
- 📌 Bar chart: Average age of buyers across car makes
- 📌 Bar chart: Average car prices across car makes
- 📌 Bar chart: Average buyer salaries across car makes
- 📌 Bar chart: Average partner salaries across car makes
- 📌 Bar chart: Average total salaries across car makes
- 📌 Bar chart: Average number of dependents across car makes

 [**Dashboard Overview**]
 <img width="1366" height="768" alt="Interactive dashboard1" src="https://github.com/user-attachments/assets/be0bb51f-4706-43a8-91b8-db0d45cad840" />

 **[View Live Dashboard on Tableau Public](https://public.tableau.com/views/AutomotiveDemandTrendsCustomerPurchaseBehaviorAnalysis/CarMakesandBuyersProfiles?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)**

## Key Insights
**Demand Trends**
- Hatchback dominates market (56%), followed by Sedan (29%), SUV (15%)
- SUVs are highest priced, Hatchbacks are most affordable

**Customer Segmentation**
- Hatchback buyers:
  → Younger (22–30), lower income
- Sedan buyers:
  → Mid-age (28–45), mid-income
- SUV buyers:
  → Older (35–60), highest income

**Income & Purchase Behavior**
- Strong positive relationship between:
  → Age → Salary → Car Price
- Higher-income customers prefer premium vehicles (SUVs)

**Behavioral Patterns**
- Male customers prefer Hatchbacks
- Female customers prefer Sedans
- SUV buyers typically have no house loans

## Recommendations
- Focus on Hatchback and Sedan segments (85% of demand)
- Target customers aged 22–45 for volume growth
- Position SUVs as premium offerings for high-income segments
- Tailor marketing strategies:
  - → Hatchbacks → younger, price-sensitive buyers
  - → Sedans → mid-income professionals (especially female segment)
  - → SUVs → high-income, financially stable buyers
 
## Outcome / Impact
This analysis enables:

- ✅ Data-driven market entry strategy
- ✅ Optimized product mix and inventory planning
- ✅ Targeted customer segmentation and marketing
- ✅ Improved revenue potential through pricing alignment

# Next Steps
- Build a predictive model for car purchase likelihood
- Develop customer lifetime value (CLV) segmentation
- Create an interactive Tableau dashboard for stakeholders
