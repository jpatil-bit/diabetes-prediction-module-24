# Predicting 30-Day Hospital Readmission Risk in Diabetic Patients - EDA

## Data Over View
 Data Overview The dataset represents ten years (1999-2008) of clinical care at 130 US hospitals and integrated delivery networks. It includes over 50 features representing patient and hospital outcomes. Information was extracted from the database for encounters that satisfied the following criteria. (1) It is an inpatient encounter (a hospital admission). (2) It is a diabetic encounter, that is, one during which any kind of diabetes was entered into the system as a diagnosis. (3) The length of stay was at least 1 day and at most 14 days. (4) Laboratory tests were performed during the encounter. (5) Medications were administered during the encounter.

The data contains such attributes as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab tests performed, HbA1c test result, diagnosis, number of medications, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc.


## Project Overview

The data shows that early hospital readmission among diabetic patients is driven by a combination of age, hospital utilization intensity, medication instability, and admission context. 
While no single variable explains readmission risk, their combined effect creates predictable patterns. Feature engineering revealed that patients with longer stays, more procedures, and frequent medication changes are significantly more likely to be readmitted within 30 days. 
A baseline Logistic Regression model confirmed that these risks can be quantified using ROC-AUC, supporting the idea that early readmission is not random but a measurable outcome that can inform proactive care planning and resource allocation.

## What problem we are solving 


This analysis demonstrates how historical hospital data can be used to identify diabetic patients at elevated risk of early readmission. Such insights can support targeted follow-up care, medication review, and discharge planning, ultimately reducing avoidable readmissions and improving patient outcomes.

---

## Tools and Libraries Used
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Matplotlib**: For creating static, animated, and interactive visualizations.
- **Seaborn**: For advanced statistical plots and visualization.
- **Jupyter Notebook**: For running and presenting the analysis interactively.
- **colorama** : Exploring this new library for styling and coloring the fonts for the hypothesis.

---

## Dataset
https://github.com/jpatil-bit/diabetes-eda-module-20/blob/main/data/diabetic_data.csv

### Key Features:
* Age
* Gender
* Race
* Time in hospital
* Number of laboratory procedures
* Number of procedures
* Number of medications
* Admission type
* Admission source
* Discharge disposition
* Number of inpatient visits
* Number of emergency visits
* Number of outpatient visits
* Insulin usage
* Diabetes medication indicators
* Medication change count
* Age midpoint (numeric transformation of age ranges)
* Medication change count
* Binary readmission indicator (readmitted within 30 days)

  Excluded Features (to prevent data leakage)

* Patient identifiers (encounter ID, patient number)

* Original readmission category column

## Modeling

* Baseline: Logistic Regression with class weighting (good transparent baseline).

## Metric: 
* Confusion matrix for interpretability.



---

##  Analysis and hypothesis
*** Jupyter file containes all the EDA's and plots ***

[https://github.com/jpatil-bit/customer-coupon/blob/main/customer_coupon_eda.ipynb](https://github.com/jpatil-bit/diabetes-eda-module-20/blob/main/predict-diabetes.ipynb)

########## **EDA , Data ** ##########
1. The model incorporates demographic, hospital utilization, admission context, and treatment-related features to capture both baseline risk and clinical complexity. Engineered variables such as age midpoint and medication change count enhance interpretability and predictive strength. Together, these features allow the model to effectively distinguish patients at higher risk of 30-day readmission while avoiding data leakage from identifiers.
2. The model uses a combination of demographic, clinical, hospital utilization, and treatment-related features to predict 30-day hospital readmission risk among diabetic patients.
3. Diabetic patients with complex hospital stays, unstable medication regimens, prior admissions, and emergency-based care pathways are most likely to be readmitted within 30 days.
---

##  Visualizations

Various visualizations are used in this analysis to uncover insights from the data:

- **Bar Plots**: 

---

##  Getting Started

To run this project locally, follow the steps below:

### Prerequisites

Ensure you have Python 3.x installed and the necessary dependencies:

1. Clone the repository:

   ```bash

   git clone https://github.com/jpatil-bit/diabetes-eda-module-20.git
