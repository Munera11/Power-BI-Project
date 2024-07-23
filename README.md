# Power-BI-Project

## 🎯 Instructions <br/>
The challenge will be considered complete when you submit the URL of the document you have been working on. Make sure that the URL is in share mode and accessible by the teacher.
If there is no submission option on the exercise, click on the “I’m done” button.

## Insights from E-commerce Data <br/>
### Objective
*In this challenge, you will dive into the intricacies of The Look E-commerce dataset using PowerBI.
This dataset is a comprehensive collection of information related to a fictitious e-commerce clothing retailer, designed to simulate real-world data analytics scenarios you might encounter in the industry.
It includes data on customers, products, orders, logistics, web events, and digital marketing campaigns.
Your task will be to navigate through this dataset to uncover valuable insights that could help drive business decisions.*

## Expected Outcomes
Participants leverage this dataset to:

* **Select an Area of Focus:** Choose a specific aspect of the business to analyze. This could be sales performance, customer behavior, product popularity, or inventory efficiency.
* **Conduct a Detailed Analysis:** Utilize PowerBI to dive deeper into your chosen area. Apply segmentation, calculate KPIs to assess business performance, such as sales revenue, customer acquisition, and conversion rates, and use the visualization techniques you’ve learned to explore the data from multiple angles.
* **Develop Recommendations:** Based on your analysis, craft actionable recommendations for the business. Consider how they can leverage your insights to improve their operations, marketing strategies, product offerings, or customer engagement.

By doing that:

* You will gain hands-on experience in applying PowerBi concepts to real-oriented data.
* Insights derived from the analysis will contribute to informed decision-making within an e-commerce business context.
* The project presentation will showcase participants’ ability to analyze complex datasets and communicate findings effectively.

## Introduction to the Look E-commerce Dataset <br/>
The Look E-commerce Dataset provides a comprehensive view of online retail operations, encompassing various dimensions such as sales transactions, customer information, product attributes, website engagement metrics, logistics and additional metadata.
This dataset serves as a valuable resource for analyzing and understanding the dynamics of e-commerce business activities.

# Getting to Know the Context - 30min / 1H <br/>
## Understanding the Business Context
* Industry Overview: Gain insights into the e-commerce industry, including market trends, competition, and consumer behavior.
* Company Background: Understand the company operating the e-commerce platform, its mission, values, target audience, and unique selling propositions.
* Business Objectives: Identify the overarching business goals and strategic priorities driving the e-commerce operation.
* Operational Processes: Familiarize yourself with key operational processes such as sales, marketing, inventory management, and customer service.
## Identifying Key Business Questions
* Sales Performance:
- How have sales trends varied across different product categories over time?
- What are the top-selling products and their contribution to overall revenue?
- Are there any notable seasonal patterns or trends in sales data?
- How do sales vary between weekdays and weekends?
* Customer Behavior:
- Who are the most frequent buyers, and what is their average order value?
- Can we identify any customer segments based on purchasing behavior or demographics?
- What is the distribution of customer lifetimes, and how does it impact sales?
- Are there any correlations between customer satisfaction ratings and purchase frequency?
* Inventory Management:
- Which products have the highest inventory turnover rates, and which ones are slow-moving?
- Can we predict future inventory requirements based on historical sales data?
- Are there any inventory shortages or excesses that need to be addressed?
- How do inventory levels correlate with sales performance and customer satisfaction?
* Website Performance:
- What are the primary sources of website traffic, and how do they impact conversion rates?
- Is there a correlation between website engagement metrics (e.g., time spent on site, page views) and sales?
- Can we identify any usability issues or barriers to conversion based on website analytics?
- How effective are promotional campaigns in driving website traffic and sales?
* Marketing Effectiveness:
- Which marketing channels (e.g., email campaigns, social media ads) drive the highest ROI?
- Can we analyze the effectiveness of specific marketing campaigns in acquiring new customers?
- Are there any customer segments that respond better to certain marketing strategies?
- How do customer acquisition costs compare across different marketing channels?
# Data Import <br/>
Create a new dataset The Look e-commerce in BigQuery and add all the CSV files from the The Look e-commerce dataset as tables

link to the dataset in BigQuery (click on view dataset)

Instructions to get data:

1. Open PowerBI Desktop and select “Get Data” from the Home tab.
2. Choose “BigQuery” as your data source and connect to The Look e-commerce dataset using the provided project ID.
3. Import the tables

# General Exploratory Data Analysis <br/>
* Take some time to understand the dataset’s tables and relationships (What is the data in each table, what is in each column, what is the type of data, what information could I obtain with it?)
* Explore briefly the dataset
* Identify interesting patterns, trends, and potential areas for analysis.

## Understanding Table Relationships
* Take time to look at the data and make sure you understand the relationships between the different tables.
* Check the relationships in PowerBi > Model view. If necessary change the relationships

## Dataset’s Tables and Relationships
For the Look E-commerce Dataset, we can envision several tables representing different aspects of e-commerce operations. Here’s a hypothetical breakdown of tables and their relationships:

## Tables:
1. distribution_centers:
- This table stores information about distribution centers.
- Fields: id, name, latitude, longitude
2. events:
-This table records various events related to user interactions.
- Fields: id, user_id, sequence_number, session_id, created_at, ip_address, city
3. inventory_items:
- This table maintains a record of inventory items.
- Fields: id, product_id, created_at, sold_at, cost, product_category, product_name, product_brand, product_retail_price, product_department, product_sku, product_distribu
4. order_items:
- This table contains information about items included in orders.
- Fields: id, order_id, user_id, product_id, inventory_item_id, status, created_at, shipped_at
5. orders:
- This table stores data related to orders placed by users.
- Fields: order_id, user_id, status, gender, created_at, returned_at, shipped_at, delivered_at, num_of_item
6. products:
- This table contains information about products available for sale.
- Fields: id, cost, category, name, brand, retail_price, department, sku, distribution_center
7. users:
- This table stores user information.
- Fields: id, first_name, last_name, email, age, gender, state, street_address, postal_code, city, country
## Relationships:
Using the Model view look for the relationship between the different tables
![first_image](https://github.com/user-attachments/assets/871cb318-2c98-4458-9bf7-887fe000c881)

## Additional Considerations:
* Ensure referential integrity by enforcing foreign key constraints between related tables.
* Use appropriate data types and indexing to optimize query performance.
* Consider denormalization techniques for improving query performance in analytical workloads.
* Regularly update and maintain the dataset to reflect changes in e-commerce operations over time.

# Setting Goals and Project Organisation - 30min / 1H <br/>
## Defining Analytical Objectives
IMPORTANT! To begin, choose only two or three points, from the business cases. If you have more time throughout the day, you can continue covering other topics.
Once you have chosen the topics to discuss, identify the main tables that you will use. Those will be the tables you will continue working with. There are different topics and tables to cover, the purpose of the challenge is not to cover them all in one day, but to be able to select which ones are the most relevant to get the job done.

* Define specific analytical objectives based on the business questions identified earlier.
* Use the differents tools from PowerBi to achieve these objectives.
**Some business cases you could explore for the Project related to the key bussiness question:**

1. Sales Performance Analysis:

- Case 1: Product Performance Evaluation: Analyze sales data to identify top-performing and underperforming products. Recommend strategies to promote high-margin products and optimize inventory for slow-moving items.
- Case 2: Seasonal Trends Analysis: Explore seasonal variations in sales and identify peak periods for different product categories. Develop targeted marketing campaigns and promotions to capitalize on seasonal demand fluctuations.

2. Customer Behavior Analysis:

- Case 1: Customer Segmentation: Segment customers based on demographics, purchasing behavior, and engagement levels. Tailor marketing strategies and product offerings to different customer segments to enhance customer satisfaction and loyalty.
- Case 2: Customer Lifetime Value Prediction: Predict the lifetime value of customers using historical purchase data. Implement personalized marketing campaigns and loyalty programs to increase customer retention and maximize lifetime value.

3. Inventory Management Optimization:

- Case 1: Inventory Forecasting: Forecast future inventory requirements based on historical sales data and seasonality patterns. Implement demand-driven inventory management strategies to minimize stockouts and reduce excess inventory holding costs.
- Case 2: Stockout Prevention: Identify products with high stockout rates and analyze the root causes. Implement safety stock policies and supplier management strategies to mitigate stockout risks and improve product availability.

4. Website Performance Enhancement:

- Case 1: User Experience Optimization: Analyze website traffic patterns and user behavior to identify usability issues and bottlenecks in the customer journey. Implement website design improvements and UX enhancements to increase conversion rates and improve customer satisfaction.
- Case 2: Conversion Rate Optimization: Conduct A/B testing and multivariate analysis to optimize website layout, messaging, and call-to-action buttons. Implement targeted landing pages and personalized recommendations to enhance conversion rates and drive sales.

5. Marketing Effectiveness Assessment:

- Case 1: Campaign ROI Analysis: Evaluate the return on investment (ROI) of different marketing campaigns and channels. Allocate marketing budgets more effectively based on the performance of each campaign and channel.
- Case 2: Customer Acquisition Cost Reduction: Identify cost-effective customer acquisition channels and tactics. Implement targeted advertising campaigns, referral programs, and content marketing strategies to reduce customer acquisition costs and increase marketing ROI.

# Exploratory Data Analysis (EDA) 3H / 4H <br/>
## Checking Data Quality< br / >
Checking data quality is crucial because the reliability and accuracy of the data directly impact the outcomes of analyses, decision-making, and business operations. Inaccurate or incomplete data can lead to flawed insights, misguided strategies, and unreliable results, emphasizing the importance of ensuring data quality for trustworthy and impactful outcomes.

Take some minutes to answer this questions

* Are all the columns types good?
* Nomenclature is clear?
* There is some missing data?
* There outliers?
## Data Cleaning <br/>
Cleaning the data is essential to eliminate inconsistencies, errors, and inaccuracies, ensuring that analyses and models are based on reliable information and leading to more accurate and trustworthy insights.
Here is a list of tasks to keep in mind when cleaning the data:

Navigate to the Power Query Editor.
Identify and handle missing values, ensuring to either fill or remove them based on the context.
Correct any inconsistent data entries, such as formatting errors in product names or categories.
Convert data types where necessary, e.g., transforming text dates to datetime format.
Remove duplicate records to maintain data integrity.
## Exploratory Data Analysis <br/>
*Objective: Familiarize yourself with the dataset by exploring the distribution of key variables and summarizing data through basic visualizations.*

1. Identify the top 5 product categories in terms of inventory availability.
2. Visualize sales trends over the last year by month.
3. Compare the average sale price by product category.

## Customer Behavior Analysis <br/>
***Objective:** Dive deeper into customer analytics by examining behavior patterns and demographics.*

1. Segment customers based on their total spending.

2. Analyze the geographic distribution of customers.

To allow PowerBi to print maps you should modify the default settings:
Files > Options and Settings > Options > Security > click on Map and flied Map visuals > OK > refresh
<img width="924" alt="second_image" src="https://github.com/user-attachments/assets/0551222d-1794-44a8-8a1c-c561c0bf9654">

## Product Performance <br/>
***Objective:** Assess product performance.*

1. Determine the products with the highest return rates.

2. Using appropriate graphs, analyze the performance of products, product categories, brands, and anything else that seems relevant to you.
# Getting All Together - 1H <br/>
Create your own report. You will have 10 minutes at the end of the day to present your findings.

A good presentation should include:

* A clear problem statement at the beginning (don’t hesitate to put yourself in a role to explain your objectives and the decisions you’ve made - without going into technical details).
* Relevant data, charts and analysis to address the problem
* A list of recommended actions to take moving forward
**IMPORTANT ! Remember** It’s not about how many charts or how much data you show!
Your role as a Data Analyst is to interpret that data and present your findings for better decision-making.

**Time to Present the Result!**
Good luck with your presentations!
