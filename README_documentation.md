## RFM Analysis Using K-means Clustering for Customer Segmentation Project

#### Introduction
This project was completed in Jan. 2024 by Tiantong (Victor) Mao, and Hanyue (Patrick) Yao, project manager and data scientist at the UC Davis practicum team for Standard Insights. 
Standard Insights is an AI as a Service company that cooperates with UC Davis' MSBA program as an industrial partner (MIP - MSBA industrial partner). 
This notebook is a technical demo presented to Standard Insights which aims to offer a business solution framework for its sister company to better understand its customer behavior. 

#### Data
The dataset used is derived from privately owned daily sales data offered by our MIP. 
There are three tables:
1. customers: information about the customer
2. temp_salesdata: two months of sales information
3. temp_productdata:  product information (not used in this analysis)

#### Method
We are using the RFM method to measure customer's purchase behavior. This method mainly includes three metrics:
1. Recency (R): number of days since a customer's last purchase
2. Frequency (F): number of times a customer purchased within the time frame
3. Monetary (M): total amount of purchase a customer placed within the time frame
