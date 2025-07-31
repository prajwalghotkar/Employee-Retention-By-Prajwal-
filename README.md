# Employee Retention Project
---
**Employee retention is a critical challenge for modern organizations, impacting both financial sustainability and workplace productivity. Recruiting and training new hires are expensive and time-consuming processes—companies often spend 15–20% of an employee’s salary on recruitment, plus experience revenue loss while new hires ramp up.**
---
##### Project Overview
- **Business Challenge**:High employee turnover leads to increased costs, knowledge loss, and operational disruption. Predicting which employees are likely to leave allows proactive retention strategies and cost savings.

- **Role of Prajwal**:As a data scientist at a multinational corporation, Prajwal was tasked by the HR team to develop a predictive model that can identify employees at risk of quitting, enabling targeted interventions.

---

##### Dataset Description
***The HR team provided Prajwal with extensive employee data including key features such as:***

- JobInvolvement
- Education
- JobSatisfaction
- PerformanceRating
- RelationshipSatisfaction
- WorkLifeBalance...and several others crucial for understanding employee engagement and retention.
---
##### Systematic Step-by-Step Process
- **Step 1**: Import Libraries and Data
  - Prajwal imported libraries like pandas, numpy, seaborn, matplotlib, and scikit-learn.
  - The employee dataset was loaded for analysis.

- **Step 2**: Basic Data Checks
  - Prajwal explored the dataset using .info() and .describe() to understand the shape and summary.

- **Step 3**: Data Preparation & Cleaning
  - Converted categorical columns ‘Attrition’ and ‘Overtime’ to integers for modeling.
  - Identified and imputed missing data.
  - Dropped irrelevant columns like EmployeeCount, StandardHours, and Over18 that had no variance.
  - Created histograms to visualize feature distributions.
  ![image](https://github.com/user-attachments/assets/c234fb85-a7e7-4ce2-a417-e1432d2da480)
  ![image](https://github.com/user-attachments/assets/8f4695a5-f99e-4b60-920c-f7a319614fd5)


- **Step 4**: Exploratory Data Analysis (EDA)
  - Prajwal analyzed how many employees left vs. stayed, calculating percentages.
  - Compared means and standard deviations of features such as age, daily rate, and satisfaction scores between stayers and leavers.
  ![image](https://github.com/user-attachments/assets/79bf8246-4330-4278-8bdc-1954b3a30bc8)

  - Visualized important factors using KDE plots, count plots (JobRole, MaritalStatus vs. Attrition), and boxplots (Gender vs. Monthly Income).
  ![image](https://github.com/user-attachments/assets/0f7522dc-7d5b-41b6-8202-f62e10ec247d)
  ![image](https://github.com/user-attachments/assets/4de98cd8-2250-4931-9c12-741c7e755d97)
  ![image](https://github.com/user-attachments/assets/1f68883a-bc1b-411e-8022-723aa02f9397)

  ![image](https://github.com/user-attachments/assets/66360a4e-bbe9-483d-b53e-93d33a033116)
  ![image](https://github.com/user-attachments/assets/e1e0b2cc-e9b2-4e4f-a9a5-4b4f06a9c4c7)
  ![image](https://github.com/user-attachments/assets/efe43f4d-f36d-4677-a7b1-9abda665bf59)

  ![image](https://github.com/user-attachments/assets/a8517a51-ecaf-4a31-a084-dd3c9ecf46a2)
  ![image](https://github.com/user-attachments/assets/cd2def73-d47c-4fcc-9f14-25c31f32afb1)

  - Created a correlation heat map to identify key relationships.
  ![image](https://github.com/user-attachments/assets/69599cfe-e14f-49c2-a248-5d4ace40bb57)
  ![image](https://github.com/user-attachments/assets/bc92e9d4-20ee-44cd-8743-3e82a2062d1d)

- **Step 5**: Feature Engineering & Encoding
  - Applied label encoding and one-hot encoding on categorical variables such as BusinessTravel, Department, EducationField, Gender, JobRole, and MaritalStatus.
  - Split the dataset into independent variables (X) and the dependent variable (Attrition, y).
  - Performed Min-Max scaling for feature normalization.

- **Step 6**: Model Development & Evaluation
  - Prajwal split the data into training and testing sets.
  - Built and tested three models: Logistic Regression, Support Vector Machine (SVM), and XGBoost classifier.
  - Evaluated models using confusion matrices, classification reports, and accuracy scores—achieving approximately 90% accuracy with logistic regression.

- **Step 7**: Model Deployment Prep
  - Saved the best performing model as a pickle file to facilitate integration into HR tools.

---

##### Key Insights
- Employees who stayed tend to be older, live closer to work, have higher job and environment satisfaction, and possess larger stock option levels.
- Insights from the model enable HR to identify high-risk employees and develop personalized retention plans.
---

##### Tools & Tech Stack
- Python (pandas, numpy, seaborn, matplotlib, scikit-learn, xgboost)
- Jupyter Notebook / VS Code

##### How to Run
- Clone or download the repository.
- Place the dataset in the project folder.
- Install dependencies:
pip install -r requirements.txt
- Run the notebook or script to reproduce analysis and model training.

I Have Checked the accuracy of the model using three algorithms. first one is Logistic Regression second Support Vector Machine and third is XGBoost -Classification 👨‍💻 🙂
