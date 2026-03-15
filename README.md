## Flipkart Customer Support CSAT Score Analysis and Prediction
### Project Overview
This project analyzes a customer support dataset to identify the key factors influencing Customer Satisfaction (CSAT) and builds machine learning models to predict CSAT scores. The analysis helps understand how operational factors such as response time, issue categories, product types, and agent-related attributes affect customer satisfaction.

The objective of this project is to apply data analysis, statistical testing, and machine learning techniques to extract insights and develop a predictive model that can help organizations improve customer support performance and customer experience.

---------------------------------------------------------------------------------------------------------------------------

### Project Type
Machine Learning | Data Analysis | Customer Support Analytics

---------------------------------------------------------------------------------------------------------------------------

### Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Google Colab 

---------------------------------------------------------------------------------------------------------------------------

### Dataset
The dataset contains 85,907 customer support interactions with multiple attributes describing support requests and agent responses.

**Key attributes include:**

**- channel_name –** Customer support channel used

**- category –** Main category of the reported issue

**- Sub-category –** Detailed issue classification

**- Customer_City –** City of the customer

**- Product_category –** Category of the product involved

**- Item_price –** Price of the product

**- Tenure Bucket –** Experience level of the support agent

**- Agent Shift –** Shift during which the agent handled the issue

**- Issue_reported_at** – Time when issue was reported

**- Issue_responded –** Time when the support agent responded

**- CSAT Score –** Customer satisfaction score (target variable)

---------------------------------------------------------------------------------------------------------------------------

### Project Workflow

**1. Data Understanding**
- Loaded dataset and inspected structure
- Checked column data types and missing values
- Identified unique values in each feature

**2. Data Cleaning**
- Removed columns with extremely high missing values
- Handled missing values using median and mode imputation
- Removed extreme outliers using the IQR method

**3. Feature Engineering**
- A new feature was created to represent the response time taken by support agents.
- response_time_hours
- This feature measures the time difference between issue reported time and issue responded time.

**4. Exploratory Data Analysis (EDA)**
- More than 15 visualizations were created to understand patterns in the data.
- Types of analysis performed:
- Univariate Analysis
- Bivariate Analysis
- Multivariate Analysis

**Visualization techniques used:**

- Count plots
- Bar charts
- Box plots
- Correlation heatmaps
- Pair plots

----------------------------------------------------------------------------------------------------------------------------

### Hypothesis Testing
Statistical tests were used to validate relationships between variables.

#### Hypothesis 1

Response time influences customer satisfaction

**Test Used:** ANOVA Test

**Result:**  Response time has a statistically significant impact on CSAT scores.

#### Hypothesis 2

Support channel affects customer satisfaction

**Test Used:** Chi-Square Test

**Result:** Support channel and CSAT score show a significant relationship.

#### Hypothesis 3

Agent experience influences CSAT score

**Test Used:** Chi-Square Test

**Result:** Agent experience level significantly influences customer satisfaction.

---------------------------------------------------------------------------------------------------------------------------

### Machine Learning Models Implemented

**Three machine learning algorithms were implemented and compared:**

1. Logistic Regression
2. Random Forest
3. Decision Tree

**Model Evaluation Metrics**

The models were evaluated using the following metrics:

**- Accuracy**

**- Precision**

**- Recall**

**- F1 Score**

These metrics help measure prediction performance and model reliability.

----------------------------------------------------------------------------------------------------------------------------

### Hyperparameter Tuning

To improve model performance, GridSearchCV was used for hyperparameter tuning.

Examples of tuned parameters:

**Logistic Regression**
- C
- solver

**Random Forest**
- n_estimators
- max_depth

**Decision Tree**
- max_depth
- min_samples_split

----------------------------------------------------------------------------------------------------------------------------

#### Model Comparison

```bash
Model                                              Accuracy
---------------------------------------------------------------                                
Logistic Regression	                                  ~0.46
Random Forest	                                       ~0.68
Decision Tree	                                       ~0.61
```

After comparison, Random Forest was selected as the final model due to its strong performance and stability.

----------------------------------------------------------------------------------------------------------------------------

#### Feature Importance

Using the Random Forest model, feature importance was analyzed to identify which variables most influence CSAT predictions.

**Top influential features include:**

- response_time_hours
- response_time_minutes
- category
- Item_price
- Tenure Bucket

This indicates that faster response times and issue category play a major role in determining customer satisfaction.

----------------------------------------------------------------------------------------------------------------------------

**Key Insights**

- Faster response times are strongly associated with higher CSAT scores.
- Certain issue categories generate more dissatisfaction than others.
- Agent experience has a measurable influence on customer satisfaction.
- Product price and category can influence customer expectations and perceived service quality.

----------------------------------------------------------------------------------------------------------------------------

#### Model Saving

The best performing model was saved using joblib for future use and deployment.

```bash
csat_prediction_model.joblib
```

This allows the trained model to be loaded and used for predicting customer satisfaction for new data.

----------------------------------------------------------------------------------------------------------------------------

#### Project Structure

```bash
flipkart-csat-ml-project
│
├── notebooks
│   └── Sample_ML_Submission_Template.ipynb
|   └── Sample_EDA_Submission_Template.ipynb
│
├── sample_data
│   └── Customer_support_data.csv
│
└── README.md
```

----------------------------------------------------------------------------------------------------------------------------

#### How to Run the Project

**Clone the repository**

```bash
git clone https://github.com/Shravani3001/flipkart-csat-ml-project.git
```

Open the notebook in Google Colab or Jupyter Notebook

Run all cells from top to bottom

Runtime → Run All

The notebook will execute the entire pipeline including:

Data preprocessing

Visualization

Model training

Model evaluation

Model saving

----------------------------------------------------------------------------------------------------------------------------

#### Business Impact

**This predictive system can help organizations:**

- Identify factors affecting customer satisfaction
- Reduce response times in customer support
- Improve support service efficiency
- Detect dissatisfied customers early
- Enable data-driven decision making

----------------------------------------------------------------------------------------------------------------------------

#### Author

**Shravani K**

DevOps | MLOps | AI Enthusiast

[LinkedIn](https://www.linkedin.com/in/shravani3001) 

[GitHub](https://github.com/Shravani3001)
