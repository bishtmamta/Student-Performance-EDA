# 📊 Student Performance Analysis - Exploratory Data Analysis (EDA) Project

📌 **Project Overview**
This repository contains a comprehensive Exploratory Data Analysis (EDA) and Statistical Testing framework designed to uncover systemic drivers behind student academic performance. Using a dataset of 1,000 students, the project evaluates how demographic characteristics, socio-economic factors, and institutional metrics intersect to dictate a student's final academic tier.

The analytical workflow transitions seamlessly from clean data profiling to rigorous multi-variable statistical validation and uncovers hidden behavioral patterns inside the education domain.

🔍 **Key Findings & Hidden Patterns**
During the deep-dive multivariate exploration, four critical hidden insights were uncovered:

* **The Gender Paradox (Math vs. Literacy):** While female students dominate the aggregate scores overall, a subject-level cross-sectional analysis reveals that male students hold a distinct edge in Math (Mean: 68.72) compared to females (63.63). However, females make a massive leap in language-based metrics (Reading and Writing), which shifts the overall performance equilibrium in their favor.
* **The "Power Combo" Matrix:** Students who belong to the intersection of Standard Lunch (high resource/socio-economic stability) and Completed Test Preparation (academic effort) have the highest probability (22.9%) of graduating into the top-tier 'Best' performance bracket.
* **Test Prep as a Social Equalizer:** Test preparation serves as a powerful equalizer. Students whose parents only completed High School but who completed the test prep course scored significantly higher on average than students whose parents held Bachelor's degrees but did not take the course.
* **Group E's Hidden Dominance:** Despite being a minority segment within the absolute population metrics of the dataset, Group E consistently outscores all other ethnic cohorts across every discrete subject (Math, Reading, and Writing).

🛠️ **Tech Stack & Libraries Used**
* **Language:** Python 3.x
* **Data Manipulation:** pandas, numpy
* **Data Visualization:** matplotlib, seaborn
* **Statistical Analysis:** scipy.stats (T-Test, ANOVA, Chi-Square Testing)

📂 **Project Architecture & Methodology**
### 1. Data Profiling & Cleaning
* Checked for dimensions (1000×8), structural integrity, and duplicated values.
* Verified data completeness: 0% missing values found across all attributes, ensuring high data integrity.

### 2. Feature Engineering
* `average_score`: Continuous variable capturing the arithmetic mean of Math, Reading, and Writing scores.
* `performance_category`: Segmented continuous scores into fixed target tiers:
  * **Best** (>85)
  * **Excellent** (70−85)
  * **Good** (50−70)
  * **Average** (<50)

### 3. Formal Hypothesis Testing (α=0.05)
* **Two-Sample T-Test:** Confirmed that the performance gap between genders is statistically significant.
* **ANOVA (Analysis of Variance):** Proved that Parental Level of Education and Race/Ethnicity introduce genuine non-random variance in performance scores.
* **Chi-Square Test of Independence:** Verified a highly robust relationship between taking the Test Preparation Course and landing in top-tier performance categories.

📈 **Visualizations Included**
The notebook features highly interactive and clean plots following advanced layout styling rules:
* **Histograms & KDE:** To understand the normal distribution of the average_score (Mean=67.77%).
* **Categorical Countplots:** Distribution of performance segments grouped by Gender and Test Prep Status.
* **Boxplots & Barplots:** Displaying the deep impact of structural socioeconomic indicators like Lunch Types.
* **Correlation Heatmap:** Highlighting strong collinearity between Reading and Writing scores (0.95), while Math remains moderately independent (0.80 - 0.82).

🚀 **How to Run this Project**
* **Clone the Repository:**
```bash
git clone [https://github.com/bishtmamta/Student-Performance-EDA.git](https://github.com/bishtmamta/Student-Performance-EDA.git)
cd Student-Performance-EDA
Install Dependencies:

Bash
pip install pandas numpy matplotlib seaborn scipy
Launch the Notebook:

Bash
jupyter notebook "student performance EDA project.ipynb"
🎯 Conclusion
The analysis robustly proves that student outcomes are heavily systemic. Socio-economic boundaries like restricted nutrition (free/reduced lunch) and generational education gaps create true academic barriers. However, the data mathematically establishes that institutional actions—specifically completing a Test Preparation Course—can completely offset these external disparities, making it a vital instrument for social equality in education.

