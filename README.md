## Chocolate Company Dashboard Insights

# Overview

The Chocolate Company Dashboard provides an in-depth analysis of sales performance, shipment costs, and market trends. By leveraging Power BI and DAX calculations, this dashboard enables leadership to make data-driven decisions efficiently. The dashboard highlights key business metrics such as top-performing salespersons, highest revenue-generating countries, shipment costs, and product performance. With a structured data model and robust data cleaning processes, this dashboard serves as a crucial tool for optimizing operations and maximizing profitability.


![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/1.png)

![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/report%20-3.png)

 

# Data Cleaning & Preparation

To ensure accurate insights, the dataset underwent rigorous data cleaning, including:
•	Handling Missing Values: Filled missing shipment costs and sales data where applicable.
•	Data Standardization: Normalized product names, salesperson names, and country identifiers.
•	Removing Duplicates: Eliminated duplicate sales entries to prevent inflated metrics.
•	Data Validation: Checked consistency in dates, product categories, and numerical fields.

![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/Screenshot%202025-03-21%20164736.png)

 
# Data Modeling

The dashboard follows a structured Star Schema model with the following key tables:
•	Fact Table: Shipments (contain total amount, total boxes, shipment cost, etc.)
•	Dimension Tables:
o	Location: Country and region details.
o	Person: Salespersons and team details.
o	Products: Product names, category, and pricing.
o	Calendar: Date-based analysis for trend identification.
This model ensures optimized relationships and efficient performance in Power BI.


![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/data%20model.png)


 
# Key Performance Metrics

1.	Total Shipment Cost Calculation
o	DAX Formula: Total Shipment Cost = SUMX (Shipments, Shipments [Cost per Box] * Shipments [Total Boxes])
o	Insight: Helps in understanding the overall expenditure on shipments.

![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/kpi.png)


3.	Top Purchasing Countries
o	DAX Formula: Top Countries by Purchase = SUM (Shipments [Total Amount])
o	Insight: Identifies the regions contributing most to revenue.

5.	Total Cost Per Box
o	DAX Formula: Total Cost per Box = DIVIDE (SUM (Shipments [Total Amount]), SUM (Shipments [Total Boxes]))
o	Insight: Determines the average cost incurred per box.
6.	Total Number of Boxes Sold
o	DAX Formula: Total Boxes Sold = SUM (Shipments [Total Boxes])
o	Insight: Shows the volume of sales across all regions. 
7.	Top Performing Salesperson
o	DAX Formula: Top Salesperson = MAXX (VALUES (Person [Sales_person]), SUM (Shipments [Total Amount]))
o	Insight: Highlights the highest-performing salesperson based on revenue.

![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/report-2.png)

 
9.	Salespersons Who Reached $2M Target
o	DAX Formula: Reached Target = IF (SUM (Shipments[Total Amount]) >= 2000000, "✔", "✖")
o	Insight: Identifies salespersons who achieved or exceeded the $2M revenue target.
10.	Salespersons Who Did Not Reach $2M Target
o	DAX Formula: Not Reached Target = IF (SUM (Shipments [Total Amount]) < 2000000, "✔", "✖")
o	Insight: Helps in assessing underperformance for potential coaching.
11.	Total Sum of Products Sold
o	DAX Formula: Total Products Sold = SUM (Products [Product Count])
o	Insight: Displays the total quantity of products sold across all categories.


![![image](https://user-images.githubusercontent.com/97775044/215146486-101d3195-4313-4c29-b88e-b8758d513911.png)
](https://github.com/riyareddy07/Chocolate-Company-Dashboard/blob/main/report%20-4.png)

 
# Business Impact

•	Leaders can easily identify high-performing regions and salespersons.
•	Helps in decision-making regarding product pricing and shipment cost optimization.
•	Assists in setting sales targets and strategizing for underperforming areas.
•	Provides a clear overview of sales trends for future forecasting and budgeting.
This dashboard effectively streamlines insights, making leadership decisions data-driven and actionable.

# Conclusion

The Chocolate Company Dashboard serves as a powerful analytical tool, enabling leadership to make data-driven decisions with precision. By leveraging advanced DAX calculations, the dashboard provides actionable insights into sales performance, shipment costs, and market demand. It simplifies complex datasets into intuitive visualizations, ensuring transparency in operations.
With clean and well-structured data, leaders can:
•	Optimize sales strategies by identifying high-performing salespeople and regions.
•	Control costs by monitoring shipment expenses and cost per box.
•	Track market demand to enhance inventory planning and product development.
•	Set realistic sales targets and provide necessary support to underperforming sales personnel.
This dashboard ensures continuous improvement in business performance, facilitating strategic decision-making and boosting overall profitability.

