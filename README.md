# 📶 Customer Churn - Business Intelligence Project
# Introduction
What is customer churn? -- When a customer decides to discontinue their relationship with a business/product. Customer churn is costly for any business. 
In fact, it is far more expensive to "buy" a new customer than retain one. Therefore, it is important for a company to retain customers due to their long-term 
customer value and intervene with customers on the brink of churning. Using a telecommunications company customer data, where each row is 1000 unique customers 
who can subscribe to any combination of the different services, I will build an ML model that will help predict customer churn! 
The ML model will consist of many classification models and ensemble of them using Python to determine the best predictive model.

This project is an extension to the first project in my Business Intelligence class. Using the same telecomm data, I applied a simple Decision Tree model to build a 
accurate churn predicting model. In that project I got overall 69% model accuracy. Not very robust. I decided to revisit this project and apply all the new knowledge that 
I have learned in my Business Intelligence class. The biggest change is of using Ensemble methods which is what I used here. You can see my first project on this github if interested titled 'Customer Churn'. The modified version will be title 'Churn Proj'.


# 📦 Technologies:
- Python on Juypter Notebook
- pandas, Numpy
- Matplotlib , seaborn
- Scikit Learn (Decision Tree, Naive Bayes, KNeighbors, Logistic Regression)
- Scikit Learn Ensemble (Voting, Baggiing, AdaBoost, GradientBoosting, RandomForest
- Scikit Learn Metrics (classification report)

# 👨‍💻 My Approach
1. Data Exploration
2. Visualizations
3. Choosing Variables
4. Preprocessing
5. Model Building
6. Ensemble Evaluation

Throughout the notebook, I have commentary of my thought process.

## Data Exploration
- Looking at variables
- Determining relevant variables
- Assessing data set size (1000 rows, 39 columns)
- Examining spread (five number summary) of numeric variables
- Examining spread of categorical variables 
- Looking for outliers and removing very noticeable outliers
- Checking for nulls or empty strings
- Checking for high correlations of numeric variables

## Visualizations
Using Boxplots to see relationship of variables and churn
- Learned that tenure was a very strong correlator to churn where longer tenure less churn
- Decided to discover what variables lead to longer tenure
- Determine what variables has significance impact on churn or no churn

## Choosing Variables
- Useless variables - Address, region, cust_id, custcat, educational level, Gender, lning and loglong.
- Variables for more tenure - retire, multiline, forward, confer, callwait, marital, and longmon
- Variables for significant churn - age, employ, longten, tollten, callten, equipmon, wiremon, and longmon
- Lastly, churn.

## Preprocessing
- Made of copy of data frame using desired variables
- Converted necessary variables into categorical variables
- Dummy coded the categorical variables into binary
- Split the data into train (70%) and test (30%) data sets
- Balanced the train data set since churn has a 73-27 split so I converted to 50-50
  
## Model Building
I will be stating all the classification models and their respective overall accuracy.
- Decision Tree: 0.80
- Naive Bayes: 0.70
- KNeighbors: 0.73
- RandomForest: 0.85
- LogisticRegression: 0.72
- AdaBoost: 0.87
- Gradient Boost: 0.77

- Voting Classifier using KNeighbors, DecisionTree, RandomForest, AdaBoost: 0.91

## Model and Ensemble Evaluation
 The Voting Ensemble is incredibly robust! 
- A 91% overall model accuracy is amazing. 
- Since we are looking to find customers who will churn, we feel comfortable using this model as it can corretly identify churners 86% of the time.
- The models ability to predict and correctly identify non-churners is strong with an overall accuracy of 94%.
  
 ![image](https://github.com/Scoldingatom205/Customer-Churn/assets/133290178/6fe68818-b92c-4241-982c-ef8cb6f860ea)

Regular marketing conversations are that customer retention costs roughly 5 times less than customer acquisition. This because of the rising costs of marketing and heavy
investment needed to convince a new customer to use your product or service. Obviously, every business needs to find a balance between retention and acquisition. Focus should be
directed to becoming a retention-first business ensuring that our current customer base are satisfied. Satisfied to the point that they dont even consider churning. Finding
the variables and features that have caused customer churn helps the business identify areas in the business that has room for improvement. It is important that the business
has consistently good service. In this case data set some significant factors are longten, longmon, tenure, cardten, and age to name the top 6. These are variables that the 
telecom company should keep in mind when addressing their customer churn issue. With that being said, they are lucky that I have created a incredibly robust machine learning classification model
that will help them identify potential churners.


Thank you for taking the time to read!
