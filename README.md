# Wind Damage Analysis – Excel Project

## Overview

This project analyzes wind-related damage costs across U.S. states between 1994 and 2016. The objective is to study how wind-related damage costs correlates across states and to identify groups of states that tend to be affected simultaneously.

The analysis was conducted entirely in Microsoft Excel and includes inflation adjustment, correlation analysis, hierarchical clustering, and 3D geographic visualization.

---

## Data

The dataset consist of monthly wind-related damage-costs for states in the U.S derived from NOAA storm event records.

Processing steps:
- Extracted wind-related event types  
- Aggregated damage costs monthly per state  
- Replaced missing observations with zero  
- Adjusted monetary values to October 2016 price level using CPI data  

---

## Methods

### Inflation Adjustment
Damage amounts were converted to constant 2016 dollars to ensure comparability over time.

### Correlation Analysis
Two correlation measures were applied:
- Pearson correlation (linear correlation)
- Spearman correlation (rank-based correlation)

Correlation matrices were visualized using conditional formatting (heat map).

### Hierarchical Clustering
States were clustered manually using the distance metric:

Distance = 1 − Correlation

Clusters were formed using a threshold of 0.65.

### Visualization
- Correlation heat maps  
- Scatter plots of clustered state pairs  
- 3D geographic bar visualization of total damage per state  

---

## Key Findings

- Wind-related damage costs are highly right-skewed, characterized by many zero-damage months and occasional extreme events. This distributional structure significantly affects dependence measures.

- Pearson correlation identified multiple clusters and suggested strong co-movement across several states. However, visual inspection of scatter plots indicates that these correlations are largely driven by simultaneous extreme events and shared zero periods rather than stable linear relationships over time.

- Spearman correlation produced fewer and more concentrated clusters. Because it is based on rank rather than magnitude, it is less sensitive to extreme values and therefore provides a more robust measure of dependence in this zero-inflated dataset.

- The comparison demonstrates how the choice of correlation metric materially influences clustering outcomes in skewed data. In this case, Spearman correlation appears better suited for capturing structural co-movement rather than tail-driven dependence.
---

## Excel Skills Demonstrated

- Excel formulas (CORREL, OFFSET & more)
- Data cleaning and transformation
- Hierarchical clustering
- Conditional formatting (heat maps)
- 3D geographic visualization (Power Map)
- Statistical interpretation of correlation measures

---
## Excel Sheet
[Wind_Damage_Analysis.xlsx](Wind_Damage_Analysis.xlsx)

## Screenshots

### 3D Damage Map
![3D Map](images/3d_map.png)

---

## Reflection

This project demonstrates how correlation measures behave differently in skewed datasets dominated by extreme values and zero observations. It highlights the importance of selecting appropriate statistical tools when analyzing real-world economic data.
