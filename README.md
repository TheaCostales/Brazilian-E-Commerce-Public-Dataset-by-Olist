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

ERD Summary:
The ERD visualizes the relationships between tables, with key fields such as order_id, customer_id, and product_id linking the datasets to facilitate comprehensive analysis and visualization.
