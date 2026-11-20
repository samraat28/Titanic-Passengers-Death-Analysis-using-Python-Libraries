# Titanic Survival Rate Analytics & Prediction
Titanic Survival Rate Analysis &amp; Prediction using Python. Includes data cleaning, exploratory data analysis (EDA), visualization using Matplotlib and Seaborn, and a Logistic Regression model to predict passenger survival based on age, gender, passenger class, fare, and family details.

Dataset Link : 

1. Project Overview

The Titanic Survival Rate Analytics & Prediction project is a Python-based Data Analytics and Machine Learning project that explores passenger information from the historic Titanic disaster to understand survival patterns and predict whether a passenger survived or not.

The project combines Exploratory Data Analysis (EDA), Data Visualization, Data Preprocessing, and Machine Learning to analyze the relationship between passenger characteristics and survival outcomes.

Using Python libraries such as Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn, the project investigates passenger demographics, ticket classes, gender, age, fare prices, and family information to identify patterns associated with survival.

A Logistic Regression classification model is implemented to predict passenger survival based on selected passenger attributes.

2. Project Objectives

The primary objectives of this project are:

Understand and explore the Titanic passenger dataset.

Perform data cleaning and preprocessing to handle missing values and inconsistencies.

Conduct Exploratory Data Analysis (EDA) to identify meaningful patterns and relationships.

Visualize passenger demographics and survival-related variables using different visualization techniques.

Understand how factors such as gender, age, passenger class, fare, and family size relate to survival.

Build a Machine Learning classification model using Logistic Regression.

Evaluate model performance using training and testing accuracy.

Generate survival predictions for individual passengers using the trained model.

3. Dataset Description

The project uses the Titanic passenger dataset (tested.csv), containing information about 418 passengers.

The dataset consists of 12 columns describing passenger details and their survival status.

Dataset Attributes

Column

Description

PassengerId

Unique identification number of each passenger

Survived

Survival status (1 = Survived, 0 = Not Survived)

Pclass

Passenger class (1st, 2nd, or 3rd)

Name

Passenger's name

Sex

Gender of the passenger

Age

Age of the passenger

SibSp

Number of siblings or spouses aboard

Parch

Number of parents or children aboard

Ticket

Passenger's ticket number

Fare

Fare paid by the passenger

Cabin

Cabin identification

Embarked

Port of embarkation

Dataset Size: 418 rows × 12 columns.

4. Technologies & Libraries Used

The project is developed using Python and the following libraries:

Technology / Library

Purpose

Python

Core programming language

Pandas

Data manipulation and analysis

NumPy

Numerical operations

Matplotlib

Data visualization

Seaborn

Statistical data visualization

Scikit-learn

Machine Learning model development

Logistic Regression

Binary classification and survival prediction

5. Project Workflow

The project is divided into three major stages:

Stage 1: Data Cleaning & Preprocessing

The first stage focuses on understanding the dataset and preparing it for analysis.

Key activities include:

Loading the dataset using Pandas.

Exploring the first and last few records using head() and tail().

Understanding dataset dimensions using shape.

Examining column names, data types, and non-null values using info().

Generating descriptive statistics using describe().

Identifying unique values using nunique().

Detecting missing values using isnull().sum().

Removing records containing missing values using dropna().

Checking duplicate records using duplicated().

After removing missing values, the dataset is checked again to ensure that no null values remain.

Important: The implementation removes all rows containing at least one missing value, resulting in 87 records being retained from the original 418 records.

Stage 2: Exploratory Data Analysis (EDA) & Visualization

The second stage focuses on understanding the dataset through graphical analysis.

Matplotlib and Seaborn are used to generate different visualizations and explore relationships between passenger attributes.

The project incorporates the following visualizations:

Line Plot: Examines relationships between passenger age and cabin-related attributes.

Bar Plot: Compares age and cabin information across different genders.

Pair Plot: Explores relationships between multiple numerical variables, differentiated by gender.

Line Plot: Examines the relationship between passenger age and the number of siblings/spouses aboard.

Scatter Plot: Explores relationships between different passenger attributes.

Histogram: Examines the distribution of family-related variables against survival status.

Box Plot: Explores the distribution and spread of numerical variables.

KDE Plot: Examines the distribution patterns of passenger attributes.

Correlation Heatmap: Identifies correlations between numerical variables.

These visualizations help explore passenger characteristics and understand the relationships between different variables.

Stage 3: Machine Learning – Survival Prediction

The final stage involves developing a binary classification model using Logistic Regression.

The model predicts whether a passenger survived or did not survive based on selected passenger characteristics.

Step 1: Feature Selection

The following columns are removed because they are not used as predictive features:

PassengerId

Name

Ticket

Cabin

The remaining dataset contains passenger information relevant to the prediction process.

Step 2: Encoding Categorical Variables

Machine Learning algorithms require numerical inputs.

Therefore, the categorical Sex column is converted into numerical values using Scikit-learn's LabelEncoder.

Step 3: Defining Independent and Dependent Variables

The independent variables (X) are:

Pclass

Sex

Age

SibSp

Parch

Fare

The dependent variable (y) is:

Survived

The Embarked column is excluded from the model features.

Step 4: Train-Test Split

The dataset is divided into two subsets:

80% Training Data: Used to train the Logistic Regression model.

20% Testing Data: Used to evaluate model performance on unseen records.

The train_test_split() function is used with random_state=42 to ensure reproducibility.

Step 5: Model Training

A Logistic Regression model is initialized and trained using the training dataset.

Logistic Regression is a supervised Machine Learning classification algorithm suitable for predicting binary outcomes.

In this project, the two possible outcomes are:

1 – Survived

0 – Not Survived

Step 6: Model Evaluation

The model's performance is evaluated using the accuracy_score() function.

The implementation also imports additional evaluation metrics, including:

Confusion Matrix

Classification Report

The recorded results are:

Evaluation Metric

Result

Training Accuracy

100%

Testing Accuracy

100%

Overall Model Score

100%

Note: The testing accuracy is based on only 18 records after data cleaning. Therefore, these results should not be interpreted as evidence of guaranteed prediction performance on new datasets.

6. Individual Passenger Survival Prediction

After training the model, the project demonstrates how to predict the survival status of an individual passenger by providing passenger attributes.

The prediction uses the following input parameters:

Passenger Class

Gender

Age

Number of Siblings/Spouses

Number of Parents/Children

Ticket Fare

Example:

Prediction = model.predict([[1, 0, 26.0, 1, 0, 136.7792]])

if Prediction == 1:
    print("Survived")
else:
    print("Not Survived")

The model generates one of two possible outputs:

Survived

Not Survived

This demonstrates how a trained classification model can be used to make predictions for individual passenger records.

7. Key Learning Outcomes

Through this project, the following concepts are explored and implemented:

Data loading and exploration using Pandas.

Data cleaning and missing-value treatment.

Data preprocessing and categorical encoding.

Exploratory Data Analysis (EDA).

Data visualization using Matplotlib and Seaborn.

Understanding correlations between variables.

Independent and dependent variable identification.

Training and testing dataset preparation.

Supervised Machine Learning.

Logistic Regression classification.

Model accuracy evaluation.

Individual record prediction.

8. Project Structure

The recommended GitHub repository structure is:

Titanic-Survival-Analytics/
│
├── dataset/
│   └── tested.csv
│
├── Titanic_Survival_Analytics.ipynb
│
├── README.md
│
└── requirements.txt

9. How to Run the Project

Follow these steps to execute the project locally:

Step 1: Clone the repository.

git clone <repository-url>

Step 2: Navigate to the project directory.

cd Titanic-Survival-Analytics

Step 3: Install the required Python libraries.

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

Step 4: Open the Jupyter Notebook.

jupyter notebook

Step 5: Open the project notebook, update the dataset file path if required, and execute the cells sequentially.

10. Future Enhancements

The project can be further enhanced through:

Advanced missing-value imputation instead of dropping all incomplete records.

More meaningful survival-focused visualizations.

Feature engineering to derive additional passenger attributes.

Experimentation with other classification algorithms such as Decision Trees, Random Forest, and Support Vector Machines.

Model evaluation using precision, recall, F1-score, and ROC-AUC.

Hyperparameter tuning to improve model generalization.

Development of an interactive web application for real-time passenger survival predictions.

11. Conclusion

The Titanic Survival Rate Analytics & Prediction project demonstrates an end-to-end implementation of a basic Data Analytics and Machine Learning workflow.

Starting from raw passenger data, the project covers data exploration, cleaning, visualization, preprocessing, model training, evaluation, and individual predictions.

It provides practical exposure to Python-based data analysis and supervised Machine Learning while demonstrating how historical datasets can be used to uncover patterns and build predictive models.

Project Domain: Data Analytics | Exploratory Data Analysis | Machine Learning

Programming Language: Python

Machine Learning Algorithm: Logistic Regression
