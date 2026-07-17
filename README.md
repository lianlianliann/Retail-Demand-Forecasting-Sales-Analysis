# Retail Demand Forecasting & Sales Analysis

## Objective
To analyze historical retail sales data, identify operational bottlenecks, and forecast future demand using ARIMA to optimize inventory management.

## Data Source
*Synthetic Retail Dataset ([Link to Kaggle/Source](https://www.kaggle.com/datasets/anirudhchauhan/retail-store-inventory-forecasting-dataset))*

## Tools Used
* **Python**: pandas, numpy (Data manipulation)
* **Visualization**: plotly.express (Interactive EDA)
* **Modeling**: statsmodels (ARIMA forecasting)

## Methodology: OPTD(R) Framework
The Exploratory Data Analysis (EDA) is structured around business questions using the OPTD framework:
* **Overview**: Macro baseline metrics.
* **Pain Points**: Operational bottlenecks and worst-performing segments.
* **Trends**: Time-based and event-driven patterns.
* **Details**: Root-cause cross-checks and distribution anomalies.
* **Recommendations**: Data-driven business suggestions.

## Key Insights
1. **Uniform Pain Points**: Stockouts, overstock, and store-level underperformance are evenly distributed across the network. There are no isolated geographic or categorical bottlenecks.
2. **The December Anomaly**: December consistently shows the lowest average sales across both years. This is not explained by a lack of promotions (which remain constant at ~50%).
3. **Inventory as a Ceiling**: Cross-checking inventory levels against units sold reveals a hard structural cap. Sales drop to zero only when inventory is depleted, meaning stock availability is actively bottlenecking potential revenue.
4. **Data Artifacts**: Price is uniformly distributed (no clustering around $9.99/$19.99), and discount tiers are perfectly balanced (exactly 5 tiers). This strongly indicates the dataset is synthetic.

## Forecasting Results
* **Model**: ARIMA(p,d,q)
* **Performance**: Achieved a Mean Absolute Error (MAE) of X units, establishing a strong baseline for automated replenishment.
