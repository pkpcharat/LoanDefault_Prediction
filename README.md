 <H1> LoanDefault_Prediction </H1>
 <p> This project aims to build a predictive model for loan default prediction using machine learning techniques. <br>
   The objective is to classify whether a borrower is likely to default on a loan </p>

<H2>Dataset</H2>
<p> import dataset from Kaggle  Therefore, We can dowload dataset from  <br>
  this link : https://www.kaggle.com/datasets/nikhil1e9/loan-default</p>

<H2> Problem statement </H2>
<p> In the banking and financial industry, assessing the risk of loan applicants is crucial to minimizing losses and improving <br>lending efficiency. 
  If financial institutions can predict which customers are likely to default on their loans,they can make informed decisions on loan approvals, 
 adjust interest rates accordingly, and implement risk mitigation strategies.</p>

<H2> Step  </H2>
<H3> Data Preprocessing </H3>
<p> - Loaded the dataset and performed an initial inspection. <br>
    - Read the dataset using pandas. <br>
    - Display the first few rows (df.head()) to understand the structure. <br>
    - Identify data types and missing values using df.info() and df.isnull().sum(). <br> 
</p>
<H3> Statistical Summary </H3>
<p> - Generate summary statistics using df.describe() to check mean, min, max, and quartiles. <br>
    - Look for anomalies in numeric variables
</p>
<H3> Outlier Detection </H3>

#check Outlier <br>
numeric_cols = ["Claim Amount","Category Premium",'Premium/Amount Ratio','BMI'] <br>
fig,axes = plt.subplots(figsize = (18,10), nrows =1 , ncols=4,squeeze = 0) <br>
i = 0 <br>
for ax, col in zip(axes.reshape(-1), numeric_cols):  <br>
 ax.boxplot(df_select[col], tick_labels=[col], sym='k') <br>
plt.tight_layout() <br>

<H3> Feature Engineering </H3>
<p> - Converted objected featured  into numeric values using one-hot encoding (pd.get_dummies) <br>
    - Created a new feature  for  encoding (0,1).
</p>.

<H3>  Model Training and Evaluation </H3>
<p> -Trained multiple machine learning models: <br>
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost </p>
<H3>  Best Model Selection and Final Result </H3>
<p> - In the final result, I selected XGBoost as the best-performing model with an accuracy of 88.41%. <br>
    - In conclusion , This project demonstrates the application of machine learning models to solve classification problems. <br> The XGBoost model showed the best performance in predicting loan default,
  with a testing accuracy of 88.41%.
</p>
