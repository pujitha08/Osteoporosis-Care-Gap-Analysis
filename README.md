# Osteoporosis Care Gap Analysis

## Predicting and Preventing Repeat Fractures Through Data Analytics

This project analyzes gaps in osteoporosis follow-up care among fracture
patients and evaluates how improved screening and referral workflows could
help reduce repeat fractures.

The analysis combines predictive modeling, patient segmentation, and
financial impact analysis to identify high-risk patients and translate
analytical findings into actionable healthcare recommendations.

## Business Problem

Many patients receive treatment for an initial fracture without receiving
appropriate follow-up evaluation for underlying bone health.

The project focuses on understanding whether gaps in osteoporosis screening
and follow-up care are associated with repeat-fracture risk and how healthcare
systems can better identify patients who may benefit from intervention.

## Analytical Approach

### 1. Data Preparation

The analysis incorporated patient-level fracture data and clinic/referral
information.

Data preparation included:

- Cleaning and aligning inconsistent headers
- Handling missing numeric and categorical values
- Reviewing BMD, T-score, and age for outliers
- Creating fracture and bone-health indicators
- Encoding categorical variables for modeling
- Addressing class imbalance using balanced class weights

### 2. Logistic Regression

Logistic regression was used to identify factors associated with repeat
fractures while maintaining model interpretability.

The model achieved an ROC-AUC of approximately **0.94**, indicating strong
predictive discrimination.

The analysis identified **care-gap status as the strongest predictor of
repeat-fracture risk**, with T-score, bone mineral density (BMD), age, and
diagnosis status also contributing to risk.

### 3. Random Forest

A Random Forest model was used as a non-linear comparison model and to
evaluate feature importance.

Important contributors included:

- Care-gap status
- T-score
- Bone Mineral Density (BMD)
- Age

This provided an additional perspective on the factors associated with
repeat-fracture risk.

### 4. Patient Segmentation

K-Means clustering was applied using patient characteristics such as age,
BMD, and T-score.

PCA was used to visualize the resulting patient groups.

Three clinically interpretable segments emerged:

**Low-Risk: Normal Bone Health**
- Stronger bone density
- Healthier T-scores
- Lower fracture risk
- Appropriate for continued monitoring

**Undiagnosed Bone Loss (Osteopenia)**
- Early signs of declining bone health
- Many patients may lack formal diagnosis or treatment
- Represents an important opportunity for proactive intervention

**Diagnosed High-Risk Osteoporosis**
- Lowest bone density
- Poorer T-scores
- Higher concentration of clinical risk indicators
- Requires timely follow-up and treatment adherence

## Key Findings

- Missing recommended follow-up care was the strongest signal associated
  with repeat-fracture risk.
- Care gaps appeared across age groups, suggesting that follow-up breakdowns
  are a system-level issue rather than being isolated to one age segment.
- Patient segmentation revealed distinct groups that can support more
  targeted screening and intervention strategies.
- Predictive analytics can help identify high-risk patients before another
  fracture occurs.
- Standardizing referral workflows could help prevent patients from being
  lost between initial fracture treatment and bone-health follow-up.

## Financial Impact Analysis

Referral-improvement scenarios were evaluated at **25%, 50%, and 75%**
adoption levels.

Under the **75% referral-adoption scenario**, the model projected approximately
**44 preventable repeat fractures avoided** and **$1.33 million in estimated savings**,
assuming a cost of **$30,000 per repeat fracture**.

These results are scenario-based projections derived from the analysis code
and illustrate the potential clinical and financial value of improving
osteoporosis screening and referral completion.

These estimates demonstrate the potential value of improving osteoporosis
screening and follow-up workflows.

## Recommendation

The analysis supports integrating **automatic bone-density referral triggers
into the electronic health record (EHR)** for eligible first-time fracture
patients.

A standardized referral process could help move osteoporosis screening from
an inconsistent follow-up activity to a routine component of fracture care.

**Early Referral → Early Prevention → Better Patient Outcomes**

## Repository Contents

- `Osteoporosis_Care_Gap_Analysis.ipynb` – Complete data analysis,
  predictive modeling, clustering, and financial impact analysis
- `README.md` – Project overview, methodology, findings, and recommendations

## Tools & Technologies

Python | Pandas | NumPy | Scikit-learn | Logistic Regression |
Random Forest | K-Means Clustering | PCA | Matplotlib | Seaborn

## Project Focus

Healthcare Analytics | Predictive Modeling | Patient Segmentation |
Risk Stratification | Care Gap Analysis | Financial Impact Analysis