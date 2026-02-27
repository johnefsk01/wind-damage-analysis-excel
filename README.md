# Wind Damage Analysis – Excel Project

## Overview

This project analyzes wind-related damage costs across U.S. states between 1994 and 2016. The objective is to study how wind-related damages co-move across states and to identify groups of states that tend to be affected simultaneously.

The analysis was conducted entirely in Microsoft Excel and includes inflation adjustment, correlation analysis, hierarchical clustering, and 3D geographic visualization.

---

## Data

The dataset consist of monthly wind-related damage costs per U.S. state derived from NOAA storm event records.

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
Two dependence measures were applied:
- Pearson correlation (linear dependence)
- Spearman correlation (rank-based dependence)

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

- Pearson correlation produced more clusters and suggested strong co-movement between several states.
- Results were heavily influenced by extreme damage events and shared zero periods.
- Spearman correlation produced fewer and more geographically coherent clusters.
- For this skewed dataset, Spearman provided a more robust measure of dependence.

---

## Excel Skills Demonstrated

- Advanced Excel formulas (CORREL, OFFSET, aggregation)
- Data cleaning and transformation
- Manual hierarchical clustering
- Conditional formatting (heat maps)
- 3D geographic visualization (Power Map)
- Statistical interpretation of correlation measures

---

## Screenshots

### Correlation Heat Map
![Heatmap](images/heatmap.png)

### 3D Damage Map
![3D Map](images/3d_map.png)

### Example Scatter Plot
![Scatter Plot](images/scatter.png)

---

## Reflection

This project demonstrates how correlation measures behave differently in skewed datasets dominated by extreme values and zero observations. It highlights the importance of selecting appropriate statistical tools when analyzing real-world economic data.
