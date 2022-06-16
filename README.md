# Demand-Forecasting
Demand Forecasting is the key movement which pretty much controls any remaining exercises of Supply Chain Management. It is an important element in planning and decision making in any business/company management. Many reputed companies rely on demand forecasting to make major decisions related to production, expansions, sales, etc. Forecasting is known as an estimation/prediction of an actual value in future time span.

# Description
The transactional sales data of the cement company was pulled into Azure SQL Database. The pulled data was further read into Azure Databricks where predictions were made. These predictions were then exported to the Azure SQL Database from where they were sent to Power BI for visualization. And all of these services were managed in Azure DataFactory.

# Methodology
## Step 1 - Service deployement on cloud:
Deploy all the services to be used within a same resource group on Microsoft Azure, i.e. Azure DataFactory, Azure Storage Account, Azure SQL Database, Azure SQL Server, Azure Databricks, Azure PowerBI.

## Step 2 - Link services:
All the services are linked through Azure DataFactory as an ETL pipeline.

## Step 3 - Data Migration:
Browse the dataset from Local File Storage and import this data in the BLOB storage under the created Storage account.

## Step 4 - Data Processing:
Then, we run SQL queries to import the dataset in a tabular format as a SQL Database. Use the CopyData function in DataFactory to transfer data from Blob to SQL Database.

## Step 5 - Model Predictions: 
This SQL data is used as an input for Azure Databricks, where we develop a model that generate predictions. The input data that we have is from 2015 to 2020. And, the demand forecasting is done for 2021 to 2025. The prediction is done on the basis of the Target value and the Production value.

Predicted Production value = Average of previous 5 years Production values.

Predicted Target value = Average of previous 5 years Production values - Average of previous 5 year Difference value

Where, Difference value = Production value - Target value

## Step 6 - Data Visualization: 
The predictions made are then used as an input to Power BI where predictions are being visualized. 
In Power BI use the following attributes for the visualizations:

Target value, Production value, Plant ID, Year

# Proposed Solution:
![image](https://user-images.githubusercontent.com/47741271/174055236-624a8017-41fe-4e4a-9f8c-dc873be1fc1d.png)

# Languages used
Python/PySpark, SQL

# Technologies/Platforms used
Microsoft Azure (Azure DataFactory, Azure Storage Account, Azure SQL Database, Azure SQL Server, Azure DataBricks, Azure PowerBI), Microsoft Excel.

# Team lead
Mr. Anshul Bhatnagar

# Faculty mentor
Dr. Hitesh kumar sharma
