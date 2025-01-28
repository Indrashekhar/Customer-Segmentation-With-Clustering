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

Your task is to develop a robust customer segmentation to assist the e-commerce company in understanding and serving its customers better. This will help to have a more customer-centric focus, improving marketing efficiency. Therefore, you’ll explore the data, employ preprocessing and feature engineering, dimension reduction, and perform customer segmentation with clustering models.

Prepare a report that illustrates your insights to the prospective stakeholders, showing how your solution will save the business money and build trust with its stakeholders. At this stage of the project, the five main questions you need to consider are:

1. What insights can be gained from the data, and what recommendations can be made to the company based on these insights? 
2. Which features can be deleted, selected, and combined (feature creation) to effectively segment customers based on the five metrics (frequency, recency, CLV, average unit cost)?
3. Are there more features beyond the suggested ones that would help in better segmentation
4. Based on this data set, which statistical or ML technique is the best for determining the optimum number of clusters ( k )?
5. How do the clusters compare based on frequency, recency, CLV, and average unit cost?
6. What did you deduce from the dimensional reduction analysis?
