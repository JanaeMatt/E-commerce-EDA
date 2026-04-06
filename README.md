# E-Commerce-EDA
This analysis examines transactional data from a UK-based online retail company specializing in unique all-occasion gifts, with a significant wholesaler customer base. The dataset spans December 1, 2010, to December 9, 2011, capturing a critical year of operations and growth patterns.


# Project Background

Uneven revenue distribution and conversion performance across regions represents a critical challenge for this UK-based online gift retailer, limiting the company's ability to maximize growth and efficiently allocate marketing resources. This analysis examines whether sales trends and conversion rates vary meaningfully across geographic markets,and whether these patterns reveal strategic opportunities to increase total revenue through targeted regional interventions.


Using transactional data spanning December 2010 through December 2011, results show that regional markets exhibit substantial variation in revenue contribution, customer purchasing behavior, and funnel conversion rates. The magnitude and nature of these differences suggest that region acts as a key determinant of commercial performance, with disparities in Average Order Value (AOV), repeat purchase rates, and cart abandonment indicating that market dynamics and customer characteristics shape outcomes beyond product appeal alone.


These findings underscore that maximizing revenue requires more than expanding product offerings—it requires region-specific marketing strategies, tailored customer engagement approaches, and resource allocation aligned with each market's unique conversion dynamics and growth potential. Understanding where customers drop off in the purchase funnel by region, and which markets demonstrate the strongest retention and lifetime value, is essential for prioritizing investments that drive sustainable, profitable growth.


Insights and recommendations are based on the following areas
- Revenue Driven Analysis
- Geographic Performance Context
- Market Segmentation
- Oppurtunity & Risk Assesment


Tableau Dashboard

 SQL Queries
 
Download Dataset


 # Executive Summary

 Revenue generation for this UK-based online gift retailer is highly uneven across geographic markets, with a small number of regions driving the majority of total sales. Using transactional data from December 2010 through December 2011, this exploratory analysis evaluates how revenue contribution, order value, and customer purchasing behavior vary by region to identify opportunities for more effective marketing and operational focus.

 
Results show that the United Kingdom dominates total revenue, but several international markets demonstrate disproportionately high average order values despite lower transaction volumes. This suggests that international underperformance is driven more by limited customer reach and engagement rather than by low willingness to spend. Additionally, regional differences in repeat purchasing behavior indicate that customer lifetime value varies meaningfully by geography, pointing to retention as a key lever for revenue growth.


Together, these findings indicate that revenue growth opportunities lie not only in strengthening the company’s core UK market, but also in selectively investing in high-value international regions through targeted marketing, localized engagement strategies, and customer retention initiatives aligned with regional purchasing behavior.


. The entire interactive dashboard can be viewed 

# Data Structure

The dataset used consists of 4 tables: Invoice, InvoiceItem, Product, and Customer.
The dataset is organized using a relational structure centered on the InvoiceItem table. This table functions as the primary fact table and contains one row per line item purchased, including:

- InvoiceNo

- StockCode

- Quantity

- UnitPrice

  
The Invoice Item table connects to two dimension/reference tables, Invoice and Product, while the Invoice table itself connects to the Customer table:


Invoice -  contains InvoiceNo (PK), InvoiceDate, TotalRevenue, and CustomerID (FK)

Product  -  contains StockCode (PK), Description, and UnitPrice

Customer - contains CustomerID (PK) and Country


Each dimension table contains a primary key that links back to the central transaction record. This normalized structure reduces redundancy, maintains categorical consistency, and enables clean segmentation across product and customer groups. The design resembles a simplified star schema commonly used in retail analytics and business intelligence environments.


The Invoice → Customer relationship is many-to-one, meaning multiple invoices can belong to a single customer. The InvoiceItemtable bridges Invoice and Product in a many-to-many relationship, resolved through a junction table pattern where each row represents a single product line within a given invoice.


Although focused on e-commerce transactions, this structure reflects widely used analytic dimensions across industries, including time (InvoiceDate), geography (Country), product catalog (Product), and measurable outcome variables (Quantity, UnitPrice, TotalRevenue).

<img width="650" height="600" alt="image" src="https://github.com/user-attachments/assets/bede8460-36f1-414d-ba54-7d96b221935c" />

