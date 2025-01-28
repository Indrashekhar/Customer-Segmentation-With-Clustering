# Customer Segmentation with Clustering

# Business context
You are provided an e-commerce data set from a real-world organisation to perform customer segmentation with clustering models to improve marketing efforts (SAS, 2024). It is a transnational data set with customers from five continents (Oceania, North America, Europe, Africa, and Asia) and 47 countries.

The data set contains 951,668 rows, each representing a product a customer ordered. The data set contains details about the customer (e.g. location, product type, loyalty member) and order (e.g. days to delivery, delivery date, order date, cost, quantity ordered, profit) based on orders between 1 January 2012 and 30 December 2016.

As each customer is unique, it is critical to identify and/or create new features for customer segmentation to inform marketing efforts. The data set has 20 features you can choose from:

* **Quantity**: The quantity the customer orders (e.g. 1, 2, 3).
* **City**: Name of the customer's residence (e.g. Leinster, Berowra, Northbridge).
* **Continent**: Name of the continent where the customer resides (Oceania, North America).
* **Postal** code: Where the customer resides (e.g. 6437, 2081, 2063).
* **State province**: State or province where the customer resides (e.g. Western Australia, Quebec, New South Wales).
* **Order date**: The date the order was placed (e.g. 1 January 2012, 20 June 2014).
* **Delivery date**: The date the order was delivered (e.g. 12 April 2014, 19 November 2016).
* **Total revenue**: Total revenue based on ordered items in USD (e.g. 123.80, 85.10).
* **Unit cost**: Cost per unit ordered in USD (e.g. 9.10, 56.90).
* **Discount**: Percentage or normal total retail price (e.g. 50%, 30%).
* **Order type label**: Method in which the order was placed (e.g. internet sale, retail sale).
* **Customer country label**: The country where the customer resides (e.g. Australia, Canada, Switzerland).
* **Customer birthdate**: The date the customer was born (e.g. 8 May 1978, 18 December 1987).
* **Customer group**: Loyalty member group (e.g. internet/catalogue customers, Orion club gold members).
* **Customer type**: Loyalty member level (e.g. internet/catalogue customers, Orion club gold members high activity).
* **Order ID**: Unique order identifier (e.g. 1230000033).
* **Profit**: Total profit is calculated:  Totalprofit=(totalrevenue−unitcost)×quantity  in USD (e.g. 1.20, 0.40).
* **Days to delivery**: The number of days for delivery is calculated:  Deliverydays=deliverydate−orderdate  (e.g. 6, 3, 2).
* **Loyalty number**: Loyal customer (99) versus non-loyal customer (0).
* **Customer ID**: A unique identifier for the customer (e.g. 8818, 47793).

Since we have a transnational data set, which implies customers from different continents, several metrics are important when performing customer segmentation for target marketing. From a marketing perspective, the following five metrics help to understand the nuance of the customer base, buying behaviour, preferences, and value to the business.

* **Frequency** indicates how often a customer purchases over a given period of time. A high frequency indicates a loyal customer, a high level of satisfaction, trust or brand loyalty, and/or effective marketing efforts. Frequency based on purchases guides a business in the effectiveness of target marketing campaigns and how to target less active customers.
* **Recency** measures how recently a customer made a purchase or placed an order. It helps predict customer churn (turnover) and engagement. A customer is a business’s most valuable asset, so securing customer retention is essential. A high recency indicates customer satisfaction and engagement.
* **Customer lifetime value (CLV)** indicates the average or total value a customer contributes to a business over the course of their relationship. In other words, CLV is a metric of the total income a business can expect to generate from a customer as long as said customer remains a loyal client. CLV helps to prioritise marketing efforts and resources as it focuses on customers who are expected to bring the most value over time. Therefore, retaining high-value customers.
* The **average unit cost** indicates if the customer prefers low cost or high cost items. This is related to the profitability of purchases. Customers buying products with a higher average unit cost price should be targeted differently. Customer segmentation assists in identifying these customers.

## Objective
Your task is to develop a robust customer segmentation to assist the e-commerce company in understanding and serving its customers better. This will help to have a more customer-centric focus, improving marketing efficiency. Therefore, you’ll explore the data, employ preprocessing and feature engineering, dimension reduction, and perform customer segmentation with clustering models.

## Solution

![image](https://github.com/user-attachments/assets/096bf4f1-e1c1-47a1-82d4-588f4b8dbe9d)

### View DataFrame and perform EDA

![image](https://github.com/user-attachments/assets/39c7688b-2219-4f51-b084-05ac3fde65a7)

![image](https://github.com/user-attachments/assets/3991fac5-2534-458f-a2b1-b0f495a88968)

![image](https://github.com/user-attachments/assets/bc325d42-e486-401b-ae00-e86529d0a4e9)

![image](https://github.com/user-attachments/assets/dc31316a-5641-4b7f-b543-242efb370bbd)

![image](https://github.com/user-attachments/assets/af55d477-77e8-41f1-af84-9b94ad03ae10)

![image](https://github.com/user-attachments/assets/32c72b0a-ff84-4991-92c8-5f22d14426a7)

![image](https://github.com/user-attachments/assets/2d81c53b-2942-430f-8acd-5c913e94c824)

### Descriptive statistics

![image](https://github.com/user-attachments/assets/2de26616-c83a-440a-834b-448c6b460c4d)

![image](https://github.com/user-attachments/assets/c39c6dd1-0504-4a16-92f1-f37ba710a3ca)

![image](https://github.com/user-attachments/assets/6f59a294-1a7f-436b-a5f5-99733f8668a2)

![image](https://github.com/user-attachments/assets/5b1d03d4-9f29-4fd4-aa03-26abd6500d2e)

### Visualise the data to determine the distribution and extreme values

![image](https://github.com/user-attachments/assets/11727b50-c0ea-4d4f-a13b-7cb9e76e1fe7)

![image](https://github.com/user-attachments/assets/80fd85d7-49d6-4a01-aa71-60295ae20c2f)

### Select k with Elbow method

![image](https://github.com/user-attachments/assets/5d9396b7-f6b1-44fc-9a6b-aca5409e27c2)

As per the elbow method shown above the number of clusters where the rate of decrease in within-cluster variation starts to diminish is 4. This suggests that there should be 4 customer segments that marketing efforts can target to enhance customer satisfaction and drive business growth.

### Feature reduction using PCA and t-SNE

![image](https://github.com/user-attachments/assets/0f8c2f81-8d4a-4aa9-97f0-6ad59ce1239d)

### Select k with Silhouette method

For n_clusters = 2 The average silhouette_score is : 0.4345625183689278
For n_clusters = 3 The average silhouette_score is : 0.4414029300712657
For n_clusters = 4 The average silhouette_score is : 0.4103105664115391
For n_clusters = 5 The average silhouette_score is : 0.38895417199351207
For n_clusters = 6 The average silhouette_score is : 0.3394110821082939

![image](https://github.com/user-attachments/assets/dee5d8b3-cad0-4ff4-9ada-855afd089dcf)

![image](https://github.com/user-attachments/assets/aebdde7e-8aac-4552-ac97-4dfa640b9036)

![image](https://github.com/user-attachments/assets/6c0225b3-61a2-4bf5-b7d5-7ed157b89a45)

![image](https://github.com/user-attachments/assets/bf55ba19-9801-4d80-a100-b0b5b82a9e21)

![image](https://github.com/user-attachments/assets/797c2287-8e52-49ca-b3e8-6a30e5f99bc5)





