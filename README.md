# Backorders Supply Chain Analysis 
### Goal: 
The goal of this project to minimize backorders by identifying the material at risk of backorder before the event occurs. This gives the business management a suitable time to react and make appropriate changes.

### Result
Analyzed the supply chain process-data of 1.9M product orders and developed ML models using Python that can predict if a given order goes to back order with 89.9% precision and 89.5% recall in Random Forest model.

## OVERVIEW

### What are backorders?
An order placed for a product that is temporarily out of stock with the supplier. A backorder indicates that the demand for the particular product or a service is more than it’s supply.
Backorders are not to be confused with “out of stock”. In the case of “out of stock” the supply or production of the product may be uncertain. On the other hand, backorder are placed for products which are in planned production that have encountered a lag due to several factors.

### Dataset Overview
The dataset for this problem has two classes, positive and negative class. The positive class meaning the product went into backorder and the negative class indicating the opposite. This makes the problem a binary class classification problem. The data is highly imbalanced with a ratio of 1:148 for the positive and negative class respectively for the train set. Majority of the classes are negative i.e, most of the products did not go into backorder. The dataset has 22 features and 1 class label. All the features and thier descriptions are listed below:

sku: Stock Keeping Unit
national_inv: Current inventory level of component
lead_time: Registered transit time
in_transit_qty: In transit quantity
forecast_3_month: Forecast sales for the next 3 months
forecast_6_month: Forecast sales for the next 6 months
forecast_9_month: Forecast sales for the next 9 months
sales_1_month: Sales quantity for the prior 1 month
sales_3_month: Sales quantity for the prior 3 months
sales_6_month: Sales quantity for the prior 6 months
sales_9_month: Sales quantity for the prior 9 months
min_bank: Minimum recommended amount in stock
potential_issue: Indictor variable noting potential issue with item
pieces_past_due: Parts overdue from source
perf_6_month_avg: Source performance in last 6 months
perf_12_month_avg: Source performance in last 12 months
local_bo_qty: Amount of stock orders overdue
deck_risk: General risk flag
oe_constraint: General risk flag
ppap_risk: General risk flag
stop_auto_buy: General risk flag
rev_stop: General risk flag
went_on_backorder: Product went on backorder


Classification Report for Random Forest

![](/classification_report.png)



ROC-AUC Curve for different models
![](/ROC_Curve.png)

Precision Recall Curve for different models
![](/Precision_Recall_Curve.png)
