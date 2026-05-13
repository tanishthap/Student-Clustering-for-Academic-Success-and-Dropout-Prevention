# Student Clustering for Academic Success & Dropout Prevention

**Name:** Tanishtha Papadkar  

---

## Main Notebook

[Open Notebook](./Student-Clustering-for-Academic-Success_fin.ipynb)

## Data:
find Data at: https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+successLinks to an external site.

 from Studentnfo.csvDownload Studentnfo.csv

Number of Samples: 4424
Number of Features: 36

## Project Overview

This project applies clustering techniques to student profile data in order to identify patterns related to academic success, disengagement, and dropout risk.

Because this is an **unsupervised learning** project, the goal is not to predict a known target variable. Instead, the notebook explores how students can be grouped based on academic performance, demographics, and socio-economic indicators so that institutions can support students more effectively.

---

## Problem Statement

Educational institutions often struggle to identify at-risk students early enough to intervene. Without early detection, students may fall behind academically, disengage from coursework, or drop out entirely.

This project explores whether clustering methods can uncover meaningful student groups that support:

- early intervention
- personalized learning support
- retention improvement
- academic monitoring
- dropout prevention

---

## Why This Matters

Identifying student groups with different performance and engagement patterns can help schools move from reactive support to proactive support.

This is important because it can:
- improve retention rates
- support struggling students earlier
- help advisors prioritize interventions
- guide resource allocation
- improve student outcomes overall

---

## Stakeholders

Several groups can benefit from this analysis:

- **Universities and administrators** — for retention and policy planning
- **Academic advisors** — for targeted student support
- **Students** — for personalized guidance and intervention
- **Policy makers** — for educational planning and support strategy

---

## Dataset Information

The dataset contains student records with 4,424 observations and 36 features.

### Feature Groups
The data includes:
- demographic information
- application and enrollment characteristics
- academic performance indicators
- financial / social indicators
- socio-economic variables such as unemployment, inflation, and GDP

### Important Academic Features
Some of the most informative variables in the clustering process were:
- `Curricular units 1st sem (grade)`
- `Curricular units 2nd sem (grade)`
- `Curricular units 1st sem (approved)`
- `Curricular units 2nd sem (approved)`
- `Admission grade`

### Socio-Economic Features
- `Unemployment rate`
- `Inflation rate`
- `GDP`

---

## Data Understanding and Preprocessing

The notebook includes:
- dataset inspection
- data type review
- missing value checks
- one-hot encoding using `pd.get_dummies`
- feature scaling using `StandardScaler`

There were no missing values in the dataset, which made preprocessing more straightforward.

Because clustering is distance-based, scaling was necessary so that large-valued variables would not dominate the clustering results.

---

## Exploratory Data Analysis

The notebook explores:
- distributions of numeric features
- academic performance patterns
- socio-economic feature distributions
- correlation heatmaps
- scatterplots of semester grades

### Key EDA Findings
- Academic performance features show the strongest structure in the data
- Semester grades and approved units are highly correlated
- Demographic features are often less informative for clustering
- First-semester and second-semester grades show a strong positive relationship
- Some students have zero or very low performance, suggesting disengagement or dropout risk

---

## Clustering Methods Used

This project compares three unsupervised learning approaches:

### 1. K-Means Clustering
K-Means was used to group students into clusters based on overall similarity.

- The elbow method and silhouette score suggested **K = 3**
- The silhouette score was about **0.305**
- K-Means created broad, scalable student segments

### 2. Hierarchical Clustering
Hierarchical clustering was used to explore nested student groupings and gradual transitions.

- A 3-cluster solution was selected
- The silhouette score was about **0.166**
- This method provided more interpretable structure and student progression insight

### 3. DBSCAN
DBSCAN was used to identify dense groups and outliers.

- Best parameters found: `eps = 5`, `min_samples = 15`
- Silhouette score was about **0.220**
- This method was especially useful for identifying unusual or high-risk students

---

## Main Findings

Across all clustering methods, academic performance variables were the strongest drivers of segmentation.

### K-Means Interpretation
- one large cluster of typical students
- smaller clusters representing at-risk or high-performing groups
- useful for scalable grouping

### Hierarchical Clustering Interpretation
- revealed gradual transitions between student types
- useful for monitoring students moving toward risk
- more actionable for early intervention

### DBSCAN Interpretation
- identified dense clusters and outliers
- especially useful for detecting disengaged or unusual student profiles
- helpful for identifying extreme cases needing individual review

---

## Business Insights

This project suggests that universities should focus on early academic indicators rather than relying mainly on demographic information.

### Recommended Actions
- use first-semester grades as an early warning signal
- monitor students with low approved units or zero academic activity
- provide tutoring and advising to at-risk groups
- reward and retain high-performing students
- use outlier detection to flag students needing immediate support

---

## Best Model Discussion

Each clustering method has strengths:

- **K-Means**: best for broad segmentation and scalability
- **Hierarchical Clustering**: best for interpretability and student progression analysis
- **DBSCAN**: best for detecting outliers and unusual student behavior

For early intervention, hierarchical clustering provides especially useful insight. For balanced performance and scalability, K-Means is the strongest general clustering choice.

---

## Conclusion

This project shows that clustering can help universities identify meaningful student groups based on academic engagement and performance.

The results support a data-driven approach to student success:
- identify students early
- target interventions more effectively
- improve retention
- support dropout prevention

Overall, the project demonstrates that academic performance variables are the most important features for segmenting students into useful intervention groups.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook

---

## Final Takeaway Hierarchical Clustering is the best model to use
Rather than applying a one-size-fits-all approach, universities can use clustering to segment students and deliver targeted, data-driven support, ultimately improving retention rates, academic success, and overall institutional performance.

Ultimately, clustering enables universities to move from reactive responses to proactive, data-driven student success strategies, improving retention, performance, and long-term educational outcomes.
---

## Author

Tanishtha Papadkar
