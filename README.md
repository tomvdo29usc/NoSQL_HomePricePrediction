<!-- ABOUT THE PROJECT -->
## About The Project

The project contains the designed MongoDB database schema with optimized collections to store housing data. Extracted, transformed, loaded (ETL) raw home information to build accurate document-oriented data models for advanced analytics.
**Tools**: Python (NumPy, Pandas, statsmodels), MongoDB NoSQL

**Skills**: Data Engineering, Applied Statistics, ETL Pipeline, Database Management

## **1. Exploratory Data Analysis**
![image](https://github.com/user-attachments/assets/1aabcc78-773c-4422-9ba9-13b7157715b0)
![image](https://github.com/user-attachments/assets/1982ca60-9f09-4ba5-a92c-2e239c5864a1)

# 2. Data Strategies

## 2.1 Envision Data and Business Process

Our company currently has the data above stored in an Excel sheet. However, the company goal is to to establish a central database system where stakeholders can collaborate to support their business functions. Therefore, below is our data schema diagram:

![image](https://github.com/user-attachments/assets/94df80cc-7f61-4032-bc41-58b18c04c6f8)
![image](https://github.com/user-attachments/assets/279733ae-897d-4f91-b222-e0810353397d)

## 2.2 Data Schema Technicals

After interviewing 3 stakeholders and understanding their data requirements, we have developed schema for the 3 data collections in MongoDB with validation rules according to the business logics and inputs from stakeholders.

![image](https://github.com/user-attachments/assets/fe9ec267-1b82-4546-819d-6b985d4826d8)

![image](https://github.com/user-attachments/assets/7c7ebc66-f918-4b3a-90aa-867d23afcf67)

![image](https://github.com/user-attachments/assets/0fe8e044-f43c-4352-8c77-6a21c821f75a)

# 3. Analytics and Insights

## 3.1 Query Data from the MongoDB Database

![image](https://github.com/user-attachments/assets/f00ca94c-f91e-4375-85e7-a686ee458beb)

## 3.2 Home Price Predictive Model Development

Obtaining the dataset from MongoDB query, we want to built a statistical model (Linear Regression) to understand how factors influence the home price and try to predict the home price accurately. Our approach is to split the dataset into training set (70%) and testing set (30%). We train the model on the training set and test the model performance on unseen data on the testing set. Below is the process and result of the train-test-split process:

![image](https://github.com/user-attachments/assets/2cab367a-d4a5-4f65-b39d-ba76214b87aa)

## 3.3 Insights from the Model

As the Linear Regression model can yield very high performance in the testing set. We train the model using the entire dataset to understand the interactions. Below is the regression results:

![image](https://github.com/user-attachments/assets/60d9468f-808f-49e2-b994-b7fc38afd746)

> [!NOTE]
> - The expected average land price is $195,476 with no property, ceteris paribus
> - If the size of the home increases by 1 SQFT, the home price will increase by on average of $267.70, ceteris paribus. However,
> - If the total bed rooms in the home increases by 1 unit, the home price will decrease by $24,006.00, ceteris paribus. This might be that we sacrifice other living spaces or bedrooms for another new bedroom within a fixed amount of home size.
> - If the total floors in the home increases by 1 unit, the home price will decrease by $63,866.00, ceteris paribus. This might be that we sacrifice other floors space for another floor within a fixed amount of home size.
> - If the age of the home increases by 1 unit, the home price will decrease by $1,438.2, ceteris paribus. This might be because older home infrastructure is depreciating over time, making the home value to go down.

## 3.4 Business Decisions

Using the model, we can estimate the fair value of a home on the market. If the home price is currently below our estimate price, we should consider buy and invest in flipping the property to make profit.

![image](https://github.com/user-attachments/assets/6d0ef640-d571-44ce-911d-d4fa338e1e82)

**THANK YOU!**
