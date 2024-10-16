**🏢 Predictive Analytics for Employee Retention**



**🔍 Project Overview**
This project addresses the critical challenge of employee attrition within organizations by leveraging machine learning techniques. Employee retention is vital not only for workforce stability but also for business success. Using predictive models and insightful analytics, the goal is to empower HR teams to proactively identify at-risk employees and improve retention strategies.

**🎯 Objective**
The objective of this project is to apply machine learning to predict potential employee resignations and develop actionable insights for HR departments. With historical employee data, the system aims to identify patterns and resignation risks to reduce turnover rates and improve employee satisfaction.

**🛠 Libraries and Tools Required**
Make sure you have the following libraries and tools installed:

pip install scikit-learn pandas numpy matplotlib seaborn nltk

Python
NumPy
Pandas
Scikit-Learn
Matplotlib & Seaborn
NLTK / SpaCy (for text analysis)
Jupyter Notebooks

**📊 Dataset Overview**
The dataset contains 287 records with 25 columns, each capturing important employee attributes. It offers key insights into individual performance, engagement, and career trajectory. Here’s a summary:

Rows: 287
Columns: 25
Memory Usage: ~56.2 KB

**Key Features**
Username: Unique employee identifier
EnterpriseID: Organization-level ID
PerformancePegawai: Performance rating
StatusPernikahan: Marital status
Pekerjaan: Job role
AlasanResign: Resignation reason (if applicable)
TingkatPendidikan: Education level
TanggalHiring: Date of hiring
TanggalResign: Resignation date

**📦 Data Preprocessing**
Effective preprocessing ensures high-quality model performance. Key steps taken:

1.Handling Missing Values:

89% missing values in IkutProgramLOP
23% missing values in AlasanResign

2.Dealing with Skewness:

Median values are used to address skewed data.

3.Inconsistent Data Handling:

Standardized marital status labels to "Other".
Consolidated resignation reasons into broader categories.

4.Feature Engineering:

Extracted employment duration using hiring and resignation dates.
Created age categories: Young, Middle-aged, and Senior.
New feature StatusKerja identifies whether employees are currently working or have resigned.

**📈 Employee Trends Analysis**

**Annual Workforce Trends**
2006-2013: Stable workforce with fewer resignations.
2013-2015: Sharp increase in employee exits.
2018-2019: Severe decline in workforce due to high resignation rates.
Insight: The rise in resignations may indicate dissatisfaction, better opportunities elsewhere, or poor work-life balance.

**Resignation Reasons Analysis**
Working Hours: Long or irregular hours drive many employees to leave.
Career Change: Employees switch jobs for better roles or growth opportunities.
Career Clarity Issues: Lack of transparent career paths affects retention negatively.

**🤖 Machine Learning Models for Prediction**
The following models were evaluated for predicting employee resignation:

Model	Accuracy	Precision	Recall	F1-score	ROC-AUC
Support Vector Machine	0.67	0.00	0.00	0.00	0.50
Gradient Boosting	0.95	0.90	0.95	0.92	0.95
Decision Tree	0.93	0.86	0.95	0.90	0.93
Random Forest	0.91	1.00	0.74	0.85	0.87
Linear Regression	0.67	0.50	0.11	0.17	0.53

**Recommendation:**
The Gradient Boosting model showed the best performance, with 95% accuracy and a 0.95 ROC-AUC score. It is selected as the preferred model for predicting employee attrition.

**🔧 Model Optimization and Hyperparameter Tuning**
The Gradient Boosting model was further fine-tuned using cross-validation to improve performance:

Mean Precision: 0.97 (±0.05)
Mean Recall: 0.96 (±0.07)
Mean ROC-AUC: 0.97 (±0.03)

Best hyperparameters:

Learning Rate: 0.01
Max Depth: 4
Estimators: 50
Subsample: 0.8

**🔍 Feature Importance**

AlasanResign: The reason for resignation is a key indicator of attrition risk.
UsiaKaryawan: Employee age plays a significant role in retention decisions.
LamaMenjabat: Length of employment impacts loyalty and engagement.
Visualization: The ROC curve of the final model achieved a high AUC score of 0.99, indicating excellent prediction capability.

**🛠 Deployment and Insights**
This project provides a user-friendly interface for HR teams to access predictive models. With the right data and insights, companies can adopt data-driven strategies to improve retention and reduce turnover.

**📢 Presenting Insights with SHAP Values**
SHAP values reveal that resignation reasons and employee age are primary factors influencing retention.
The Gradient Boosting model emphasizes job satisfaction and tenure, while the neural network highlights onboarding processes and career clarity as critical elements.

**📂 Project Structure**

Employee_Retention/
│
├── retention_model.py         # Main ML code
├── employee_data.csv          # Dataset
├── README.md                  # Documentation
└── results/                   # Visualizations and model results

**🤝 Contributing**
Contributions are welcome! Follow these steps to contribute:

**Fork the repository**
Create a new branch (feature/new-feature)
Submit a pull request

**📝 License**
This project is licensed under the MIT License. Feel free to use and improve it!

Together, let’s build smarter HR solutions and foster a happier workforce! 🚀
