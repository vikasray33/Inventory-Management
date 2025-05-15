Inventory Management System – Project Report

Table of Contents
1.	Project Overview
2.	Objectives
3.	Approach and Tools Used
4.	Data Model Design
o	Inventory Product ER Diagram
o	Inventory Service ER Diagram
5.	Dimension and Fact Tables
6.	Data Workflow and Automation
7.	Visualization Insights (Power BI)
8.	Conclusion
________________________________________
Project Overview
This Inventory Management System project is developed to manage, track, and analyze both product-based and service-based inventories. It encompasses data related to retailers, wholesalers, agents, warehouses, and customers. The project leverages modern data engineering and analytics tools to provide a complete, scalable solution that supports real-time analytics and business intelligence.
________________________________________
Objectives
•	Design two distinct ER models: one for product inventory and another for service inventory
•	Generate and model realistic synthetic data using Databricks
•	Build well-structured dimension and fact tables to support analytical reporting
•	Implement an automated workflow for data ingestion, processing, and loading
•	Develop Power BI dashboards to present insights and performance metrics
________________________________________
Approach and Tools Used
Databricks was used extensively for data generation, modeling, and automation:
•	Generated synthetic but realistic data sets for both product and service inventory scenarios
•	Built fact and dimension tables following a star schema approach
•	Created ETL pipelines and scheduled workflows for continuous data processing
Power BI was used for developing reports and dashboards:
•	Connected directly to modeled data
•	Delivered interactive and dynamic visualizations for business decision-making
•	Highlighted trends, bottlenecks, and key performance indicators through intuitive visuals
________________________________________
Data Model Design
Inventory Product ER Diagram
The Inventory Product model captures transactional and reference data related to products, their categories, customers, retailers, agents, warehouses, and payment modes. It includes detailed tracking of order statuses and product statuses, offering a full view of the product lifecycle.
Refer to: Inventory Product ER-Diagram (as included in the Excel file)
Inventory Service ER Diagram
The Inventory Service model is focused on service bookings, service types and categories, payment modes, and customer behavior. This model supports analytical use cases such as agent performance, service category trends, and retailer comparisons.
Refer to: Inventory Service ER-Diagram (as included in the Excel file)
________________________________________
Dimension and Fact Tables
Inventory Product Model
Dimension Tables:
•	DimCustomer
•	DimProductCategory
•	DimProduct
•	DimWarehouse
•	DimRetailer
•	DimAgent
•	DimPayment
•	DimDate
•	DimProductStatus
•	DimWholesaler
•	DimOrderStatus
•	DimLocation
Fact Tables:
•	FactProduct
•	FactProductPurchase
•	FactProductStatus
•	FactOrderStatus
Inventory Service Model
Dimension Tables:
•	DimCustomer
•	DimService
•	DimServiceCategory
•	DimDate
•	DimPaymentMode
•	DimAgent
•	DimRetailer
Fact Table:
•	FactInventoryService
Each model is designed using best practices in dimensional modeling to ensure performance and flexibility for analytical queries.
________________________________________
Data Workflow and Automation
Implemented in Databricks, the data workflow includes the following components:
1.	Data Generation
Synthetic datasets were programmatically generated to simulate a real-world business scenario involving inventory products and services. This included randomized but coherent data for dates, customers, transactions, and statuses.
2.	Schema Design
A star schema was followed, with clearly defined fact tables supported by related dimension tables. This structure simplifies analytical queries and improves report performance.
3.	ETL Pipeline
Data was cleansed, transformed, and structured into appropriate dimensional and fact tables using notebooks and job workflows in Databricks. Consistency and integrity checks were applied throughout the process.
4.	Workflow Scheduling
Automated jobs were scheduled within Databricks to ensure timely data refreshes and minimal manual intervention. This ensures the system is ready for real-time and near real-time reporting.
________________________________________
Visualization Insights (Power BI)
Interactive dashboards were developed in Power BI to highlight various analytical insights derived from the product and service models.
Inventory Product Dashboard
Key insights include:
•	Product Category-wise Sales: Charts showing which categories perform the best
•	Retailer and Warehouse Performance: Geographic and tabular breakdowns of inventory movement and order fulfillment
•	Customer Segmentation: Identification of frequent and high-value customers
•	Order and Product Status Trends: Monthly analysis of delivery, cancellation, and return patterns
Inventory Service Dashboard
Key insights include:
•	Service Booking Trends: Time-based trends in customer bookings
•	Agent Performance: Ranking agents by completed services or total value handled
•	Payment Mode Analysis: Usage distribution across different payment methods
•	Retailer-wise Service Breakdown: Comparative analysis of retailers involved in service transactions
Refer to the included images for actual dashboard screenshots.
________________________________________
Conclusion
This Inventory Management System demonstrates the application of modern data engineering practices combined with intuitive analytics and visualization. The following outcomes were achieved:
•	Created structured and scalable models for both product and service inventory management
•	Enabled automation of data pipelines using Databricks, supporting continuous data availability
•	Delivered business-ready dashboards with Power BI for strategic and operational decision-making
The system is modular and scalable, making it easy to extend with additional features such as real-time streaming, anomaly detection, or machine learning-based forecasting in the future.

