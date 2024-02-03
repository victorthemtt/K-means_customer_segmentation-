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
Due to non-disclosure agreements, no specific data is provided in this repository. 

#### Method
We are using the RFM method to measure customer's purchase behavior. This method mainly includes three metrics:
1. Recency (R): number of days since a customer's last purchase
2. Frequency (F): number of times a customer purchased within the time frame
3. Monetary (M): total amount of purchase a customer placed within the time frame

After we found the RFM for each customer, we conducted a K-means clustering algorithm based on the RFM metrics to divide the customers into certain groups. 

#### Result and Interpretation
Elbow diagram to choose the optimal k = 4. Divided the customers into 4 groups. 
Visualization of the result. 
Identified certain distinct customer groups such as the loyal ones, the regular engaged ones, and the close-to-churning ones. 

#### Caveats for our analysis
1. We see that a great number of customers purchased a product within five days of the last day in the sales table. We want to know why. This fact plays an important role in understanding the recency of each customer. If there was some incident, such as a massive discount, that caused customer behavior to change, then our model may be biased.
2. The RFM analysis is affected significantly by the chosen dates in the sales table. Thus, to make the model generalizable to customer behavior overall times, it’s better to choose the appropriate time frame of the sales table to conduct the analysis.
3. Can we find a fixed optimal K for every dataset regardless of time? Finding a fixed optimal number of clusters is useful for identifying the general behavior of customers and then designing long-term business decisions accordingly. The RFM analysis involves only clustering on these three metrics and is thus often robust to outliers, which suggests less fluctuation of the optimal k across different datasets. But to find this k, it’s better to run the same analysis across more datasets over time to see if the result changes. If most of the model results suggest that four clusters are optimal, the same as the result we have now, we can say decisively that four clusters are optimal and apply this framework to future sales data.
