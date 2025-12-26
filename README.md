# Time‑Use Survey Finland – Statistical Data Analysis Project

This repository contains the materials for a statistical data analysis project undertaken by students at the University of Turku as part of the **TKO_7093‑3004 Statistical Data Analysis** course.  The project analyses the *Time‑Use Survey* data from Statistics Finland to understand how Finnish residents allocate their time to work, sleep, reading, dining out and visiting libraries.  The work includes data preparation, exploratory analysis, clustering, principal component analysis (PCA) and hypothesis testing.

## 📂 Contents

The repository includes the following main files:

| File | Description |
|---|---|
| `Final Report.pdf` | A PDF document summarising the motivation, methodology and results of the analysis. |
| `SDA_project.ipynb` | The Jupyter notebook used to perform the data cleaning, statistical analysis, clustering, PCA and hypothesis tests. |
| `habits.data` | The raw survey dataset in `;`‑separated format (provided by Statistics Finland). |
| `habits.txt` | A plain‑text version of the dataset used in the notebook. |

## 📊 Project overview

The survey data comprises **780 respondents** from various regions of Finland, with variables covering demographics and activity patterns【855139518878483†L52-L65】.  The demographics include *household ID*, *member ID*, *sex*, *age group*, *living environment* and *day of the week*.  Activity variables measure **minutes spent working, sleeping and reading** and binary indicators for **dining at restaurants** and **visiting libraries**【855139518878483†L52-L69】.

### Goals

The main objectives of the project were:

1. **Data Cleaning & Preparation** – Standardise time formats, convert “?” entries, and handle missing or inconsistent values.  For example, “hh:mm” strings were converted to minutes and “?” values in the dining and library variables were imputed with the mode【855139518878483†L120-L134】.
2. **Descriptive Statistics** – Characterise respondents by sex, age group, day of week and living environment.  Baseline statistics revealed that **52 % of respondents were male** and **48 % female**, and most were aged 45–54 years【855139518878483†L168-L208】.  About **66 % lived in cities**, **16 % in municipalities** and **18 % in rural areas**【855139518878483†L216-L223】.
3. **Exploratory Analysis** – Estimate average daily time spent on working (≈78 min), sleeping (≈529 min) and reading (≈57 min)【855139518878483†L168-L176】 and examine rates of dining out (53.6 %) and library visits (62.95 %)【855139518878483†L232-L243】.  Visualisations explore differences by sex, age, living environment and day of week.
4. **Clustering** – Group individuals based on their time‑use patterns.  Two clusters emerged: **Cluster 1**, a working group with high work minutes and lower sleep/reading, and **Cluster 2**, a non‑working/leisure group with minimal work and more sleep and reading【855139518878483†L253-L276】.
5. **Principal Component Analysis (PCA)** – Reduce the dimensionality of the activity variables (work, sleep, reading).  The first principal component captured ~47 % of the variance, the second 33 % and the third 21 %【855139518878483†L288-L297】.
6. **Hypothesis Testing** – Use non‑parametric tests (Shapiro‑Wilk for normality and Kruskal‑Wallis with Mann‑Whitney U post‑hoc tests) to assess differences in activity minutes by living environment and other demographics.  Significant differences were found in sleep time across living environments (e.g., rural vs city)【855139518878483†L448-L556】.

### Key findings

* **Time allocation:** On average, respondents spent about 4.25 hours working, 8.83 hours sleeping and 1 hour reading (median estimates)【855139518878483†L367-L390】.
* **Dining & library visits:** 53.6 % dined at restaurants and 62.95 % visited libraries【855139518878483†L232-L243】; interestingly, ~7.89 % visited libraries but did not read【855139518878483†L168-L172】.
* **Clusters:** Cluster 1 (working group) allocated more time to work, whereas Cluster 2 (non‑working/leisure) slept and read more【855139518878483†L253-L276】.
* **PCA insights:** The first PCA component indicated that working and sleeping were more prominent than reading, while the second component contrasted reading and sleeping【855139518878483†L288-L300】.
* **Demographic differences:** Municipal residents worked slightly more and rural residents slept/read more【855139518878483†L402-L406】.  Younger adults (20–24) slept longer, while the 25–34 age group worked the most【855139518878483†L407-L417】.  Finns read more on weekends than on weekdays【855139518878483†L419-L427】.

## 🧰 How to run the analysis

1. **Install dependencies** – The notebook uses Python libraries including `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit‑learn` and `scikit‑posthocs`.  Run the following in a new environment:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scikit-posthocs
   ```

2. **Launch the notebook** – Open `SDA_project.ipynb` in Jupyter Notebook or JupyterLab and execute the cells sequentially.  The notebook reads `habits.data`, performs data cleaning, generates tables/plots, conducts clustering and PCA, and runs statistical tests.

3. **Explore the report** – For a high‑level overview of the methodology and results, read `Final Report.pdf`, which summarises the project’s findings and provides context for the code.

## 💬 Contact

This project was completed by **Nouman Bashir**, **Dominic Amoateng Sabeng** and **Saif Ur Rehman** under the supervision of **Juho Heimonen** in October 2025.  For questions or feedback, please open an issue or contact the author at nobash@utu.fi.
