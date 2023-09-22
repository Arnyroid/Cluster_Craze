# Cluster_Craze : Customer Segmentation Project Using Clustering

## Introduction

This project aims to perform customer segmentation using a dataset containing information about customers, their purchases, and responses to marketing campaigns. Customer segmentation is a critical task in marketing and business analysis as it helps companies tailor their strategies to different customer groups. In this README file, we will provide an overview of the project, including dataset information, data cleaning, data visualization, data preprocessing, and clustering.

## Dataset Information

The dataset consists of information about customers and their interactions with a company. It includes the following categories of data:

### People
- **ID:** Customer's unique identifier
- **Year_Birth:** Customer's birth year
- **Education:** Customer's education level
- **Marital_Status:** Customer's marital status
- **Income:** Customer's yearly household income
- **Kidhome:** Number of children in the customer's household
- **Teenhome:** Number of teenagers in the customer's household
- **Dt_Customer:** Date of customer's enrollment with the company
- **Recency:** Number of days since the customer's last purchase
- **Complain:** 1 if the customer complained in the last 2 years, 0 otherwise

### Products
- **MntWines:** Amount spent on wine in the last 2 years
- **MntFruits:** Amount spent on fruits in the last 2 years
- **MntMeatProducts:** Amount spent on meat in the last 2 years
- **MntFishProducts:** Amount spent on fish in the last 2 years
- **MntSweetProducts:** Amount spent on sweets in the last 2 years
- **MntGoldProds:** Amount spent on gold in the last 2 years

### Promotion
- **NumDealsPurchases:** Number of purchases made with a discount
- **AcceptedCmp1:** 1 if the customer accepted the offer in the 1st campaign, 0 otherwise
- **AcceptedCmp2:** 1 if the customer accepted the offer in the 2nd campaign, 0 otherwise
- **AcceptedCmp3:** 1 if the customer accepted the offer in the 3rd campaign, 0 otherwise
- **AcceptedCmp4:** 1 if the customer accepted the offer in the 4th campaign, 0 otherwise
- **AcceptedCmp5:** 1 if the customer accepted the offer in the 5th campaign, 0 otherwise
- **Response:** 1 if the customer accepted the offer in the last campaign, 0 otherwise

### Place
- **NumWebPurchases:** Number of purchases made through the company’s website
- **NumCatalogPurchases:** Number of purchases made using a catalogue
- **NumStorePurchases:** Number of purchases made directly in stores
- **NumWebVisitsMonth:** Number of visits to the company’s website in the last month

### Target
- The goal is to perform clustering to summarize customer segments.

## Data Cleaning

Data cleaning is a crucial step in preparing the dataset for analysis. The following data cleaning steps were performed:
- Age of customers was calculated using the year when the data was uploaded.
- Product-related columns, Place-related columns, and Promotion-related columns were combined.
- Children count per family was calculated based on columns Kidhome and Teenhome.
- Family size was obtained using the children count and marital status, and it was checked whether the user is a parent or not.
- Users' education level was obtained and classified into UG, Graduate, and PG.
- Unnecessary columns were dropped, including "Response," "Complain," and various other columns.
- Null columns were also dropped.

## Data Visualization

Data visualization is crucial for gaining insights from the dataset. The following visualizations were performed:
- Scatter Matrix was plotted on ["Income," "Cust_for_number_of_days," "age," "Spent_onProd," "chk_Parent"], and outliers were removed based on the visualizations.
- Correlation Matrix was plotted between the remaining columns to understand the relationships.
- The relationship between the level of education and expenditure, age and expenditure, marital status and expenditure, the number of children and expenditure, and offers accepted and expenditure were observed.

## Data Preprocessing

Data preprocessing is essential to prepare the data for clustering. The following preprocessing steps were applied:
- Data was feature scaled to ensure that all features have the same scale.
- PCA (Principal Component Analysis) dimensionality reduction was applied to the feature-scaled data to reduce the number of features while preserving the variance.

## Clustering

Clustering is the primary task of this project. The following clustering steps were performed:
- The Elbow method was used to find the optimal number of clusters, which turned out to be 5.
- K-means++ clustering was applied with 5 clusters, and the results were visualized to identify distinct customer segments.

This README provides an overview of the customer segmentation project, including dataset information, data cleaning, data visualization, data preprocessing, and clustering steps. The project aims to help the company better understand its customer base and tailor its marketing strategies to different customer segments.
