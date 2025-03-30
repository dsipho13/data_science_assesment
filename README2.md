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

## Key Findings

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