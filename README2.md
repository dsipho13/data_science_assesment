# **Student Performance Prediction using Machine Learning**  

## **Project Overview**  
This project aims to predict **student performance** based on their engagement with the Virtual Learning Environment (VLE) and assessment scores. Using **XGBoost**, we classify students into performance categories (e.g., Pass, Fail, Withdrawn). The goal is to identify at-risk students early, allowing for timely interventions.  

## **Dataset**  
We use the **Open University Learning Analytics Dataset (OULAD)**, which contains data on student interactions with online learning materials, assessment scores, and final results.  

### **Key Data Files**  
- `studentInfo.csv` – Contains student demographics and final results.  
- `studentAssessment.csv` – Includes student scores on various assessments.  
- `studentVLE.csv` – Tracks student interactions (clicks) with the VLE.  

### **Feature Highlights**  
| Feature | Description |
|---------|------------|
| `assessment_score` | Percentage score in assessments |
| `sum_click` | Total number of clicks on VLE activities |
| `number_of_weeks_on_vle` | Duration of student engagement in weeks |
| `activity_count` | Number of different activities accessed |
| `final_result` | Target variable (Pass, Fail, Withdrawn, Distinction) |

## **🛠️ Setup & Installation**  
1. **Clone the repository:**  
   ```bash
   git clone https://github.com/dsipho13/data_science_assesment/tree/assessment
   cd student-performance-prediction
   ```
2. **Install dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```

3. **Create the dataset:**  
   - run `create_sample_data.py` file using python
   - Place the dataset inside the `oulad_data/` directory.  

## ** Usage**
Run the following notebook `assessment_notebook.ipybn` for the followinf
### **1️ Data Preprocessing & EDA**  
   - explore and preprocess the dataset:  
   - generates **EDA visualizations**.  

### **2️ Model Training & Evaluation**  
- This will train an **XGBoost multiclass classifier** and output key performance metrics (accuracy, precision, recall, F1-score).  

### **3️ Model Inference**  
To make predictions on new student data:  
 ---
## Key Findings

1️ **Academic Performance is Crucial for Success**  
   - **Assessment Percentage** and **Assessment Score** have a strong positive correlation with **final results**. Higher scores consistently lead to better performance outcomes, with lower scores corresponding to failure or withdrawal. This underscores the importance of focusing on students' academic performance as a critical predictor of success.

2️ **Engagement Metrics are Strong Predictors**  
   - **Sum of Clicks** and **Activity Count** in the **Virtual Learning Environment (VLE)** show a strong positive correlation with final results. Students who are more engaged (measured by higher activity levels and more interactions on the VLE) tend to perform better, with those less engaged being more likely to fail or withdraw.

3️ **Consistency in Participation Matters**  
   - The **Number of Weeks on VLE** is another significant factor. Although the correlation is weak compared to other features, consistent and sustained participation on the VLE is associated with better outcomes, indicating the value of long-term engagement in academic activities.

4️ **Low Credit Load Does Not Predict Poor Performance**  
   - **Studied Credits** show no significant correlation with final results. This suggests that the number of credits a student takes does not directly influence their success or failure. Students with varying credit loads performed similarly, pointing to other factors playing a more crucial role in predicting performance.

5️ **Previous Attempts Have Minimal Impact**  
   - The **Number of Previous Attempts** does not show a significant relationship with final results, suggesting that students who retry the course do not necessarily achieve better outcomes. This implies that simply allowing more attempts does not guarantee success.

6️ **Key Features Identified by Statistical Tests**  
   - **Spearman's coefficient** analysis and the **Chi-squared test** both highlight **sum clicks** as the most influential feature, followed by **assessment percentage** and **assessment score**. While both tests reinforce the importance of academic performance, **student engagement (sum clicks)** emerges as an especially strong predictor, emphasizing the role of VLE interaction in achieving better student outcomes.

---
## ** Model Performance**  
| Metric | Score |
|--------|-------|
| Accuracy | 99.6% |
| Precision | 99.6% |
| F1 Score | 99.6% |

## ** Feature Importance**  
The most influential features in predicting student outcomes:  
1. **Assessment Scores** (strongest predictor)  
2. **Number of Clicks in VLE** (engagement level)  
3. **Weeks Engaged in Activities** (consistent participation)  
4. **Number of Activities Accessed** (learning diversity)  

## **Future Improvements**  
- Implement early warning models that predict student success **before assessments**.  