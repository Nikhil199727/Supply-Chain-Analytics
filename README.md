# Supply-chain-Analytics
## Introduction

In today’s fast-paced and competitive business environment, managing inventory and supply chain operations is critical for profitability and customer satisfaction. This project aims to explore the dynamics of inventory management, fulfillment efficiency, and demand forecasting to improve decision-making. By analyzing historical data on sales, inventory, shipments, and demand, we seek to uncover insights that can lead to more efficient inventory stocking, better profit margins, and reduced delays in order fulfillment.

Our approach involved merging data from different aspects of the business — orders, fulfillment, inventory, and demand — and conducting detailed analysis using descriptive statistics, visualizations, and time series forecasting models. The ultimate goal was to provide actionable insights into how the business can optimize its supply chain processes and prepare for future demand fluctuations.

---

## Dataset Description

The project utilized three key datasets:
1. **Orders and Shipments Dataset**: This dataset contains detailed information about customer orders, including order quantity, customer country, shipment dates, profit margins, and more.
2. **Inventory Dataset**: This contains product-specific inventory data, such as the number of units in the warehouse, inventory cost per unit, and product names.
3. **Fulfillment Dataset**: This data describes order fulfillment statuses, including shipment days and fulfillment metrics.

The datasets were sourced from internal business records, representing real-world business operations. Here’s an overview of each dataset:

### Orders Dataset
- **Rows**: 12,000+
- **Variables**: 
  - `Order Quantity`, `Order Processing Time`, `Customer Country`, `Gross Sales`, `Profit`, `Shipment Day`
  - Measurement Types: Nominal (Country), Numerical (Sales, Profit)
  - Data quality: No major missing values, minor inconsistencies in country names (corrected), handling of special characters and null values was essential.

### Inventory Dataset
- **Rows**: 500+
- **Variables**: 
  - `Warehouse Inventory`, `Inventory Cost Per Unit`, `Product Name`
  - Measurement Types: Numerical (Inventory Count), Ordinal (Inventory Cost)
  - Data quality: Clean dataset with no missing values, suitable for analysis.

### Fulfillment Dataset
- **Rows**: 1,000+
- **Variables**: 
  - `Fulfillment Status`, `Shipment Day`, `Scheduled Shipment Day`
  - Measurement Types: Nominal (Fulfillment Status), Ordinal (Shipment Days)
  - Data quality: Clean with minimal missing data, but careful handling of shipment timing was necessary.

---

## Objectives of the Project

### Content-Related Objectives
1. **Inventory Management**: Understand the balance between sales and warehouse inventory and identify trends of overstock or understock.
2. **Shipment Delays**: Investigate shipment delays across products and countries to identify bottlenecks in order fulfillment.
3. **Profit Analysis**: Analyze profit margins per product and identify key drivers of profitability.

### Statistical Objectives
1. Forecast future demand using time series modeling and calculate optimal inventory levels.
2. Quantify shipment delays and correlate them with order processing time and inventory levels.
3. Explore relationships between inventory to sales ratio, demand, and profit margins.

---

## Tools

- **Programming Language**: Python
- **Libraries Used**:
  - **Pandas**: For data manipulation and cleaning.
  - **NumPy**: For numerical operations.
  - **Matplotlib & Seaborn**: For data visualization.
  - **Plotly Express**: For interactive time-series visualizations.
  - **Statsmodels**: For time-series analysis and SARIMAX forecasting.

---

## Insights

### 1. **Inventory and Sales Analysis**
- We analyzed the **Inventory to Sales Delta** by comparing warehouse stock levels to actual sales. Products were classified as either **Overstocked** or **Understocked**, which can indicate inefficiencies in managing product availability.
- **Top 10 Products by Overstock**: The majority of products had more inventory than necessary for sales, signaling potential over-purchasing or slow sales cycles.

![download](https://github.com/user-attachments/assets/de28e128-3b2f-445a-9a58-c5250c2f2005)

### 2. **Shipment Delays**
- **Shipment Delay Analysis** revealed the average number of days delayed per product. Some products consistently showed delays, which can be correlated with poor inventory levels or long lead times.
- The visualizations highlighted the top 10 products that faced the highest delays, which can be an actionable area for improvement in fulfillment processes.

![download](https://github.com/user-attachments/assets/b4adc1a7-da05-4323-8af7-c38284a0661f)

### 3. **Profit Margins**
- **Top 10 Products by Profit Margins**: The analysis provided insights into which products yielded the highest return on sales. Products with high margins could be prioritized for promotions or scaling up sales efforts.

  ![download](https://github.com/user-attachments/assets/7b96c94a-2ecb-4b36-b932-05ba555d2d3e)


### 4. **Demand Forecasting**
- We used **SARIMAX** time-series modeling to predict future demand, and the results highlighted periods of high demand in the near future. This analysis helps businesses stay ahead by ordering products in time to meet customer demand without overstocking. (the chart can be seen in the code)
  


## Recommendations and Future Analysis

### Recommendations:
1. **Overstock and Understock Monitoring**: Implement better demand forecasting to reduce overstock situations while ensuring stock availability for understocked products.
2. **Optimize Shipment Processes**: Focus on products with significant shipment delays to improve customer satisfaction and streamline operations.
3. **Leverage High-Margin Products**: Increase the sales of products with the highest profit margins through marketing and promotions.
4. **Forecast Future Demand**: Continuously monitor demand forecasts to optimize future order quantities, ensuring that inventory is aligned with predicted customer demand.

### Future Analysis:
- **Lead Time Optimization**: Analyze lead times to explore the impact of different suppliers or shipping options on order fulfillment.
- **Customer Segmentation**: Segment customer data by region, profitability, and buying behavior to identify targeted marketing opportunities.
- **Advanced Demand Forecasting**: Refine the demand forecasting model using external factors (like seasonal trends or economic conditions) to improve prediction accuracy.

This analysis provides a solid foundation for improving inventory management, profit optimization, and demand forecasting. Continued refinements and regular monitoring of these insights will ensure that business operations remain efficient and profitable.
