## Employee Retention

* Hiring and retaining employees are extremely complex tasks that require capital, time and skills.

* “Small business owners spend 40% of their working hours on tasks that do not generate any income such as hiring”.

* “Companies spend 15%-20% of the employee's salary to recruit a new candidate”.

* An average company loses anywhere between 1% and 2.5% of their total revenue on the time it takes to bring a new hire up to speed”.

* Hiring a new employee costs an average of $7645 (0-500 corporation).

* It takes 52 days on average to fill a position.

* You work as a data scientist at a multinational corporation. 

* The HR team collected extensive data on their employees and approached you to develop a model that could predict which employees are more likely to quit.

## The team provided you with an extensive data, here's a sample of the dataset: 
   

* JobInvolvement
* Education
* JobSatisfaction
* PerformanceRating
* RelationshipSatisfaction
* WorkLifeBalance

## A confusion matrix is used to describe the performance of a classiﬁcation model: 

* True positives (TP): cases when classiﬁer predicted TRUE (they have the disease), and correct class was TRUE (patient has disease). 
* True negatives (TN): cases when model predicted FALSE (no disease), and correct class was FALSE (patient do not have disease). 
* False positives (FP) (Type I error): classiﬁer predicted TRUE, but correct class was FALSE (patient did not have disease). 
* False negatives (FN) (Type II error): classiﬁer predicted FALSE (patient do not have disease), but they actually do have the disease
* Classiﬁcation Accuracy = (TP+TN) / (TP + TN + FP + FN) 
* Precision = TP/Total TRUE Predictions = TP/ (TP+FP) (When model predicted TRUE class, how often was it right?) 
* Recall = TP/ Actual TRUE = TP/ (TP+FN) (when the class was actually TRUE, how often did the classiﬁer get it right?)


# Steps

* Import Libraries and Data Set 
* Basic Data Checks 
  * Info ()
  * Describe()

* Replace the 'Attrition' and 'overtime' column with integers
* Check  any missing data
* Create the histogram to check data 
![image](https://github.com/user-attachments/assets/c234fb85-a7e7-4ce2-a417-e1432d2da480)

![image](https://github.com/user-attachments/assets/8f4695a5-f99e-4b60-920c-f7a319614fd5)

* Drop 'EmployeeCount' , 'Standardhours' and 'Over18' since they do not change from one employee to the other.

* How many employees left the company.

* Percentage of employees who left the company 

* Number of employees who did not leave the company (stayed)

* Percentage of employees who did not leave the company (stayed) 

* Count the number of employees who stayed and left 

* Compare the mean and std deviation of the employees who stayed and left 

* 'age': mean age of the employees who stayed is higher compared to who left

* 'DailyRate': Rate of employees who stayed is higher.

* 'DistanceFromHome': Employees who stayed live closer to home  (Create Graph)

* 'EnvironmentSatisfaction' & 'JobSatisfaction': Employees who stayed are generally more satisifed with their jobs- (Create Graph)

* 'StockOptionLevel': Employees who stayed tend to have higher stock option level (Create Graph)

## Create Co relation matrix – Heat Map 

![image](https://github.com/user-attachments/assets/69599cfe-e14f-49c2-a248-5d4ace40bb57)
![image](https://github.com/user-attachments/assets/bc92e9d4-20ee-44cd-8743-3e82a2062d1d)


## Compare Age and Attrition 
![image](https://github.com/user-attachments/assets/79bf8246-4330-4278-8bdc-1954b3a30bc8)

## Count Plot - 'JobRole’ and  'Attrition’

---> sns.countplot(x = 'JobRole', hue = 'Attrition', data = df

## Count Plot – Marital Status and Attrition
![image](https://github.com/user-attachments/assets/0f7522dc-7d5b-41b6-8202-f62e10ec247d)

![image](https://github.com/user-attachments/assets/4de98cd8-2250-4931-9c12-741c7e755d97)
![image](https://github.com/user-attachments/assets/1f68883a-bc1b-411e-8022-723aa02f9397)

## KDE Plot

---> plt.figure(figsize=(12,7))
     sns.kdeplot(left_df['DistanceFromHome'], label = 'Employees who left', shade = True, color = 'r')
     sns.kdeplot(stayed_df['DistanceFromHome'], label = 'Employees who Stayed', shade = True, color = 'b')plt.xlabel('Distance From Home')

![image](https://github.com/user-attachments/assets/66360a4e-bbe9-483d-b53e-93d33a033116)

![image](https://github.com/user-attachments/assets/e1e0b2cc-e9b2-4e4f-a9a5-4b4f06a9c4c7)

![image](https://github.com/user-attachments/assets/efe43f4d-f36d-4677-a7b1-9abda665bf59)

## Boxplot -Gender vs. Monthly Income

![image](https://github.com/user-attachments/assets/a8517a51-ecaf-4a31-a084-dd3c9ecf46a2)

## Boxplot –Monthly income Job Role
![image](https://github.com/user-attachments/assets/cd2def73-d47c-4fcc-9f14-25c31f32afb1)

## Data Cleaning

* Label Encoding and One hot encoding of the following columns

'BusinessTravel', 'Department', 'EducationField', 'Gender', 'JobRole', 'MaritalStatus' 

## Data Cleaning

1) X = Create Independent variable 
2) Y= Create Dependent variable – Attrition 

3) Apply Min Max Scaler 

4) Train Test Split 

5) from sklearn.model_selection import train_test_split
6) X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.25)


# Create Model by prajwal 

Logistic Regression 
confusion_matrix, classification_report

Appx Accuracy – 90 % 

## Create Model 

Support Vector Machine 

confusion_matrix, classification_report

## Create Model 

XGBoost -Classification

confusion_matrix, classification_report

Generate the Pickle File

I Have Checked the accuracy of the model using three algorithms. first one is Logistic Regression second Support Vector Machine and third is XGBoost -Classification 

👨‍💻 🙂


