# Predicting Depression in University Students Using Machine Learning Techniques

**Jonathan Giraldo Díaz Ortega**  
Master’s Student in Artificial Intelligence & Data Science  
Universidad Autónoma de Occidente, Colombia  
📧 jonathan_gir.diaz@uao.edu.co

---

## Abstract
Depression affects millions of people worldwide and is one of the most prevalent mental health disorders, particularly among young adults. University students are a highly vulnerable group due to academic, work-related, and social stressors. Traditional diagnostic methods rely on clinical assessments conducted at later stages, reducing the intervention window.  
This study proposes a predictive model based on three machine learning classifiers (Logistic Regression, Decision Tree, Random Forest) to identify students at higher risk of depression. Logistic Regression and Random Forest both achieved an **F1-Score of 0.85** and **ROC-AUC of 0.81**, with **recalls exceeding 85%**, demonstrating practical applicability for early warning systems in academic settings.

**Keywords**: Depression, university students, machine learning, classification, public health prevention.

---

## I. Introduction
Depression is a widespread mental health disorder affecting emotional, cognitive, and physical well-being. According to the World Health Organization (WHO), over 300 million people suffer from depression globally, making it a leading cause of disability. University students are especially vulnerable due to academic pressure, financial stress, social transitions, and lack of support networks.

Traditional diagnostic methods, such as clinical interviews or questionnaires, are typically conducted after symptoms appear. Machine learning offers a promising alternative: predictive models that detect risk before full symptom onset.

This project uses machine learning to predict depression risk in university students based on various factors and publicly available data, aiming to support early intervention and improve institutional mental health strategies.

---

## II. Problem Statement
Depression in university settings is often underdiagnosed and stigmatized. Students may avoid seeking help due to discrimination fears, lack of awareness of symptoms, or unawareness of available resources. Early detection enables more effective preventive and intervention programs.

**Objective**: Create a binary classification model that predicts whether a student is at risk of depression using demographic, academic, lifestyle, and personal background data, complementing clinical methods with a data-driven approach to strengthen institutional mental health response.

---

## III. Methodology and Data

### A. Dataset
- **Source**: Kaggle  
- **Records**: 27,900  
- **Features (17)**:
  - Demographic: Age, Gender, City  
  - Academic: CGPA, academic pressure, study satisfaction  
  - Lifestyle: Sleep duration, dietary habits, work pressure, job satisfaction  
  - Additional: Profession, university degree, financial stress, family mental illness history, suicidal thoughts  
- **Target**: `Depression Status` (0 = Not at risk, 1 = At risk)

### B. Data Preprocessing  
1. **Categorical Encoding**  
   - One-hot and label encoding (e.g., suicidal thoughts → binary 0/1)  
2. **Ordinal Conversion**  
   - Dietary habits mapped to numeric scale  
3. **Normalization**  
   - Min-Max scaling for numeric features (age, sleep hrs, study hrs)  
4. **Missing Values**  
   - Imputation using mode or mean to ensure complete dataset  
5. **Train/Test Split**  
   - 75% training / 25% test  
   - Balanced dataset (~58% “at risk”), so no resampling required

### C. Model Selection
- **Logistic Regression** – linear, interpretable, baseline
  
  ![image](https://github.com/user-attachments/assets/410e2e44-0354-4abd-9036-397814e001dd)
- **Decision Tree** – non-linear, interpretable, captures complex relationships
  
  ![image](https://github.com/user-attachments/assets/71ef76ba-1be3-4deb-9879-e58d0c0b5674)
- **Random Forest** – ensemble, robust with high predictive performance
  
  ![image](https://github.com/user-attachments/assets/aba108df-242a-488b-8c28-f365b75c13b7)
---

## IV. Results

### A. Evaluation Metrics  
- **Accuracy**: overall correctness  
- **Recall (Sensitivity)**: ability to detect positive cases  
- **F1-Score**: balance of precision and recall  
- **ROC-AUC**: class discrimination capability

### B. Model Comparison

| Model                | Accuracy | Recall (Depression) | F1-Score | ROC-AUC |
|--------------------|----------|----------------------|----------|---------|
| Decision Tree       | 0.75     | 0.79                 | 0.78     | 0.74    |
| Logistic Regression | 0.82     | 0.88                 | 0.85     | 0.81    |
| Random Forest       | 0.82     | 0.86                 | 0.85     | 0.81    |

### C. ROC Curve Analysis  
- **Random Forest**: strong curve near top-left → high discriminative power  
- **Decision Tree**: curve near diagonal → lower discrimination  
- **Logistic Regression**: also robust near top-left

### D. Interpretation  
- Logistic Regression achieves the highest recall (88%), crucial in mental health where identifying true positives is more vital than false positives.  
- Random Forest balances recall and robustness, avoiding overfitting.

---

## V. Practical Applications
1. Integration into university early warning systems for mental health risk  
2. Support tool for counselors and wellness services  
3. Optimized allocation of institutional resources  
4. Stigma reduction through indirect, automated assessments  
5. Implementation feasible via web-based application integrated with academic systems

---

## VI. Conclusions
- Three classification models were implemented; Logistic Regression and Random Forest stand out with recalls above 85%.  
- Decision Tree model has limitations in generalizability.  
- **Limitations**: dataset representativeness and self-reported data  
- **Future work**:
  - Cross-cultural validation  
  - Longitudinal risk factor studies  
  - Deployment in real institutional environments  
- This study demonstrates machine learning’s potential to support public health initiatives in academic settings.

---

## Acknowledgments
The author thanks Universidad Autónoma de Occidente and the Master’s Program in Data Science and Artificial Intelligence for their support. Special thanks to fellow students and professors for their valuable feedback.

---

## References
1. H. Abdulla M., “Student Depression Prediction Using Machine Learning”, GitHub, 2023. [Online]. Available: https://github.com/HayaAbdullahM/Student-Depression-Prediction-Using-Machine-Learning (Accessed: Jun 9, 2025)  
2. F. Torres Cruz, E. E. Coaquira Flores, S. J. Condori Quispe, “Prediction of Depression Level in University Students through a Naive Bayes based Machine Learning Model”, *arXiv*, Jul 25, 2023. [Online]. Available: https://arxiv.org/abs/2307.14371 (Accessed: Jun 9, 2025)  
3. M. R. Chowdhury, W. Xuan, S. Sen, Y. Zhao, Y. Ding, “Predicting and Understanding College Student Mental Health with Interpretable Machine Learning”, *arXiv*, Mar 11, 2025. [Online]. Available: https://arxiv.org/html/2503.08002v1 (Accessed: Jun 9, 2025)  
4. T. Biswas, D. Bhattacharya, D. Rudrapal, S. Roy, “Machine Learning for Forecasting Depression and Anxiety in University Students”, *SpringerLink (ICTCS 2023)*, Apr 28, 2024. [Online]. Available: https://link.springer.com/chapter/10.1007/978-981-97-0210-7_7 (Accessed: Jun 9, 2025)  
5. A. Lin Luo *et al.*, “Predictors of Depression among Chinese College Students: a Machine Learning Approach”, *BMC Public Health*, Feb 5, 2025. [Online]. Available: https://bmcpublichealth.biomedcentral.com/articles/10.1186/s12889-025-21632-8 (Accessed: Jun 9, 2025)  
6. “EduPsyCare: Predicting Student Depression”, GitHub, 2023. [Online]. Available: https://github.com/GiapDN-13/EduPsyCare (Accessed: Jun 9, 2025)  
7. “In small study, machine‑learning tech can identify suicidal tendencies”, *Axios*, Oct 31, 2017. [Online]. Available: https://www.axios.com/2017/12/15/in-small-study-machine-learning-tech-can-identify-suicidal-tendencies-1513306565 (Accessed: Jun 9, 2025)
