# Home-Credit-Indonesia-Score-Card
Project Based intern as data scientist at Home Credit Indonesia cooperates with Rakamin Academy

Business Problem : 
1. Home Credit Indonesia wants to create machine learning to help the team determine whether the loan applications from customers will experience problems in the credit repayment process or not.
2. From the existing data, Home Credit Indonesia wants to find out what customer criteria are that have not problems in the credit repayment process to help increase revenue.

Business Insight :

![image](https://user-images.githubusercontent.com/94748637/210195051-0909dfa1-a85c-4c46-9d6f-d57db69e373e.png)

The jobs with the most customers are accountant, so we need to create a campaign as a way of thanking them, then we need to make promotions for the other jobs in graph (There are HR Staff, IT staff and Realty agent) because the percentage of customers that have no problem paying the loans is quite high but the number of customer from that three job is still small

Machine learning Model :
1. Replace unknown data

![image](https://user-images.githubusercontent.com/94748637/210195364-c1029231-f643-4d2e-ac60-82b69083360d.png)

XNA maybe is a null data which is caused by an error in inputting data so null data is written as xna.

2. Make a new column

![image](https://user-images.githubusercontent.com/94748637/210195434-d2d0e9f5-2511-47e2-9ccb-439a4fc1fc95.png)

I do it because I think the data from this new column is influential in determining whether the customer has a problem paying or not.

3. Feature Engineering
3A. Numeric Feauture.
A. Remove outlier

![image](https://user-images.githubusercontent.com/94748637/210195547-44a69a30-624f-4e02-a20c-de3461dfcb4d.png)

I remove a outlier at CNT_CHILDREN because I think the number of children above 7 is abnormal data

B. Normalize Data

![image](https://user-images.githubusercontent.com/94748637/210195628-dc83cc6b-c43b-49d4-9ad8-23f60a0fea86.png)

![image](https://user-images.githubusercontent.com/94748637/210195645-ea2cfcd4-8929-4cdc-b1b5-b3712a1bfd86.png)

I divide the column with the numeric data type into 2, namely numeric which contains only 2 unique values ​​(ie 1 and 0) and numeric which contains more than 2 unique values, this is done because in my numeric data which contains 2 unique values it represents true and false values.
so i just normalize numeric data with >2 unique value.

3B. Object Feature

![image](https://user-images.githubusercontent.com/94748637/210195837-7cbd1001-014b-4629-8636-96942d70fe7a.png)


I divide it into 2 group, first one will be one hot encoding because it have more than 2 unique value and second one will be label encoding because it have 2 unique value.

A. One hot encoding
![image](https://user-images.githubusercontent.com/94748637/210195841-c85fcb55-5063-4a83-845b-cffcba3e1c43.png)

B. Label Encoding
![image](https://user-images.githubusercontent.com/94748637/210195850-fc961797-cf76-4917-9d1a-bdfc79b8e680.png)

4. Over sampling and undesampling
Because we have imbalanced data, so we need to balanced it with oversampling or undersampling to make the model have a better accuracy value.

![image](https://user-images.githubusercontent.com/94748637/210195902-b15a31db-1295-403e-bf20-08031e462327.png)

5. Train Model
A. Logistic Regression
![image](https://user-images.githubusercontent.com/94748637/210195917-ad0165b2-374b-4819-be83-4e9be3052433.png)

B. XGBoost
![image](https://user-images.githubusercontent.com/94748637/210195943-c7740677-7d81-4a3b-be84-efbf6e6606dc.png)

C. Random Forest

![image](https://user-images.githubusercontent.com/94748637/210195952-0fcb0e21-f11c-4a46-bda9-7680a54f188a.png)

6. Result of model

![image](https://user-images.githubusercontent.com/94748637/210195960-8e63c7f5-0421-4b9d-a8fe-367f13cf21e8.png)

Random forest was the best model in this case because it have highest accuracy, precison,recall and F1-Score than others.

7. Summary 
A. For Revolving loans contract, we have to find customers with income types of businessmen, maternity leave, students and unemployed.
B. It’s recommended to create campaigns for customers who work as accountants because accountants is the largest of number of customers and percentage of successful payments/
C. Create advertisement or promotions for HR staff, IT staff and realty agents to apply for credit.
D. Random forest is the machine learning model chosen to help the team determine whether a customer has a problem paying off a loan or not.

