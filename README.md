# Ecommerce-Shipping-Predictive-Modeling
## **Project Overview** 
• Seek insight from the dataset with Exploratory Data Analysis <br>
• Performed data cleansing, data processing, data engineering to prepare data before modeling <br>
• Built a model to predict whether the shipping deliveries will be received late or on time by the customers <br>
• Developt  recommendations & benefit analysis based on insights and model prediction 
<br>
## **Background & Problems**
An international e-commerce company that sells electronic products want to discover key insights from their customer database. Currently, most of the shipping deliveries are late. 
<br>
## **Exploratory Data Analysis**
| Variable | Type | Definition | Example |
| ----------- | ----------- | ----------- | ----------- |
| ID | Nominal | Customer ID Number | 10, 15, 10995, 10996
| Warehouse_block | Nominal | Warehouse to Store the Product | A, B, C, D, F
| Mode_of_Shipment | Nominal | Mode of Product Shipping | Flight, Road, Ship
| Customer_care_calls | Discrete | Number of Calls Made | 1, 2, 5, 6
| Customer_rating | Ordinal | Company Rating by Customers | 5: Best - 4: Better - 3: Neutral - 2: Bad - 1: Worst
| Cost_of_the_Product | Discrete | Cost of Product in US Dollars | 177, 216, 236, 182
| Prior_purchases | Discrete | Number of Prior Purchase | 3, 2, 6
| Product_importance | Ordinal | Product Importance Parameter | Low, Medium, High
| Gender | Nominal | Customer Gender | Male, Female
| Discount_offered | Discrete | Product Discount in US Dollars | 65, 10, 16
| Weight_in_gms | Continous | Product Weight in grams | 4953, 5676, 2171
| Reached.on.Time_Y.N | Nominal | Target Variable, 1: NOT reached on time - 0: REACHED on time | 1, 0

1. 59.7% of e-commerce shipping deliveries are late received by the customers (6.563 of 10.999 customers).
![image](https://user-images.githubusercontent.com/80570935/126962808-11ff1d40-e71b-4d71-b0ed-e561ae408e3a.png)

2. Ship & Warehouse F has the highest frequency of delivery. But it looks almost the same based on the percentage. There's an assumtion that the late is influenced by other factors.
![image](https://user-images.githubusercontent.com/80570935/126960264-5f61c973-91f9-4ab3-b1a3-ca4f236ec0a4.png)

3. Every product that gets a discount above 10 is confirmed Late. There is an assumption that this happens in specific months, but needs further checking. 
![image](https://user-images.githubusercontent.com/80570935/126960668-055ad318-7bd9-4674-a2c5-73211b8215e6.png)

4. Shipping delivery is confirmed late when the product weight is between 2-4 kg.
![image](https://user-images.githubusercontent.com/80570935/126961078-28049344-6c62-4168-b92e-c347c8b80930.png)

<br><br>
## **Data Processing**<br>
• Check missing & duplicate values<br>
• Remove outliers for `Purchase` feature by IQR limit & replace outliers for `Discount` feature with IQR limit<br>
• Ordinal encoding for `Importance` column & feature encoding the rest of categorical columns<br>
• Select best features for modeling<br>
• Normalize all selected features <br>
<br><br>
## **Modeling**<br>
• Split features & target
• Split data into data train & data test
• Train model with 5 different algorithm such as Logistic Regression, Random Forest, XGBoost & AdaBoost
• Validate model with 
•
•
•
