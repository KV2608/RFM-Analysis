# RFM-Analysis

**Overview**

This project performs RFM (Recency, Frequency, Monetary) Analysis to segment customers based on their purchase history. This method helps in understanding customer value and is widely used in targeted marketing campaigns.

**Getting Started**

Prerequisites
Python 3.x
Pandas
Plotly

**Data**

The analysis uses a dataset named rfm_data.csv, which should contain the following columns:


CustomerID: Unique identifier for the customer

PurchaseDate: Date of purchase (format: YYYY-MM-DD)

TransactionAmount: Amount spent in the transaction

ProductInformation: Details of the product purchased

OrderID: Unique identifier for the order

Location: Location of the purchase


### 1. **Data Loading**
   - The notebook begins by importing necessary libraries including `pandas` for data manipulation and `plotly` for creating interactive visualizations.
   - It then loads transaction data from a CSV file, `rfm_data.csv`, using pandas. This dataset includes customer transaction details such as CustomerID, PurchaseDate, TransactionAmount, ProductInformation, OrderID, and Location.
   - The first few rows of the dataset are displayed to provide a snapshot of the data structure.

### 2. **Data Preparation**
   - **Date Conversion**: The 'PurchaseDate' column is converted from string format to Python's datetime format to facilitate date calculations. This is crucial for computing the recency of purchases.
   - **Recency Calculation**: Recency is calculated as the number of days between the current date and the last purchase date for each customer. This measure helps in identifying how recently each customer has made a purchase.
   - **Frequency Calculation**: The notebook computes the frequency of transactions for each customer by counting the number of orders (unique OrderIDs) associated with each CustomerID. This reflects how often a customer purchases.
   - **Monetary Calculation**: The monetary value is calculated by summing up the TransactionAmount for each customer, which indicates the total revenue generated from that customer.

### 3. **RFM Table Creation**
   - An RFM table is created by merging the recency, frequency, and monetary values. This table is essential for segmenting customers based on these three metrics.

### 4. **RFM Segmentation**
   - **Segmentation Logic**: Customers are segmented into various groups based on the quantiles of recency, frequency, and monetary values. Typically, customers are scored from 1 to 4 (with 1 being the best or highest value and 4 the lowest) for each RFM metric. The segmentation could also involve more nuanced categories based on business needs.
   - **Label Assignment**: Each customer receives a combined RFM score by concatenating the individual R, F, and M scores, which can then be mapped to segment labels such as 'Champions', 'Loyal Customers', 'Potential Loyalist', 'At Risk', etc., based on predefined criteria.

### 5. **Visualization**
   - Using `plotly`, the notebook visualizes various aspects of the RFM segments. This could include bar charts or scatter plots showing the distribution of customers across different RFM segments, or perhaps visualizing trends in customer behavior over time.
   - These visualizations are interactive and allow for a deeper analysis of the segments, facilitating strategic business decisions like targeted marketing campaigns.

### 6. **Insights and Conclusion**
   - The notebook likely concludes with insights derived from the RFM analysis, discussing the implications of different customer segments for business strategy.
   - Recommendations for future marketing strategies or further analytical steps might also be included.

This elaboration provides a comprehensive view of the notebook’s functionality and the analytical depth of RFM analysis in understanding customer value and behavior.
