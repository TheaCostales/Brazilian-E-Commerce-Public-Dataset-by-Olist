Brazilian E-Commerce Case Study: Olist Dataset Analysis
1. Introduction and Objectives
Overview of the Dataset:
This analysis uses the Brazilian E-Commerce Public Dataset provided by Olist on Kaggle. Olist is the largest department store in Brazilian marketplaces, and the dataset contains order data from various marketplaces in Brazil between 2016 and 2018.

Goal of the Analysis:

Understand Customer Behavior: Analyze purchase patterns, customer demographics, and identify key factors influencing customer satisfaction.

Evaluate Sales Performance: Assess sales trends across product categories, identify the most and least profitable products, and analyze revenue distribution across regions.

Examine Logistical Efficiency: Evaluate delivery performance, on-time versus late deliveries, and analyze the impact on customer satisfaction.

2. Methodology
      2.1 Data Preprocessing
      a) Data Acquisition
                  The dataset was downloaded using the Kaggle API, and the following files were imported:
            
            olist_orders_dataset.csv – Order-level information
            
            olist_customers_dataset.csv – Customer details
            
            olist_order_items_dataset.csv – Order items, products, and seller info
            
            olist_products_dataset.csv – Product details
            
            olist_order_payments_dataset.csv – Payment details
            
            olist_order_reviews_dataset.csv – Customer reviews
            
            olist_geolocation_dataset.csv – Geolocation data of customers and sellers
            
            product_category_name_translation.csv – Translation of product categories to English

      b) Data Cleaning and Transformation
      
      Date Format Conversion: Converted datetime columns to facilitate trend analysis.
      
      Categorical Encoding: Translated product category names and ensured consistency across datasets.
      
      c) Data Merging
      Data was merged using order_id, customer_id, product_id, and seller_id as primary and foreign keys. The relationships between tables were mapped through an Entity-Relationship Diagram (ERD), which guided data modeling.

2.2 Data Modeling
The data model follows a star schema consisting of:
            
            Fact Table:
            
            olist_order_items_dataset – Core fact table containing product, seller, and order details.
            
            Dimension Tables:
            
            olist_orders_dataset – Order information
            
            olist_customers_dataset – Customer information
            
            olist_products_dataset – Product details
            
            olist_sellers_dataset – Seller information
            
            olist_geolocation_dataset – Geolocation data
            
            olist_order_payments_dataset – Payment details
2.3 Data Visualization
Dashboards were developed in Power BI to present insights in three key areas:
1. Customer Behavior: Analyzing customer patterns, satisfaction factors, and order trends.
2. Sales Performance: Evaluating revenue, profitability by product categories, and top-performing regions.
3. Logistical Efficiency: Assessing delivery performance, on-time and late deliveries, and their impact on satisfaction.

4. Recommendations
Strategic recommendations based on your analysis
Customer Behavior 
Order peaks in September and December highlight opportunities for seasonal promotions, while urban centers like Sao Paulo and Rio de Janeiro are key markets for customer engagement. Late afternoons and weekends are high-activity periods, making them ideal for targeted promotions. High review scores (4.09) indicate positive customer experiences, but addressing the 14.69% bad ratings and reducing cancellations in high-risk categories can further improve satisfaction.
Sales Performance 
Sales are highest in July and September, driven by top categories like Health & Beauty, Watches & Gifts, and Bed & Bath, while low-performing categories such as CDs/DVDs/Multimedia and Fashion/Clothing show declining trends. Targeted promotions in low-sales months and a focus on high-margin categories can stabilize and grow revenue.
Logistical Efficiency 
With 97.02% of deliveries successful, delivery performance is strong, but long delivery times (12.5 days) and weekend delays impact customer satisfaction. Improvements in weekend processing, faster fulfillment, and predictive demand management can enhance delivery efficiency and overall customer experience.

Areas for Further Study
Churn Analysis: Identify factors contributing to customer churn.


Delivery Route Optimization: Use geolocation data to optimize delivery routes.


Cross-Sell/Up-Sell Strategy: Analyze customer purchase patterns to recommend related products.

4. Conclusion

The analysis highlights strong customer engagement in key urban regions and seasonal purchase peaks, providing opportunities for targeted promotions and enhanced customer satisfaction. Addressing negative reviews and minimizing cancellations in high-risk categories can further strengthen customer loyalty. Sales performance is driven by high-margin categories, with opportunities to boost revenue through strategic promotions during low-sales periods. Despite a high delivery success rate, improving delivery speed and addressing weekend delays can enhance logistical efficiency and overall customer experience. Implementing these recommendations can optimize revenue growth, improve customer satisfaction, and ensure sustained operational efficiency.







