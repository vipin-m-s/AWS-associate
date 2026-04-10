# AWS Athena 
- It is a tool which is used for executing SQL queries on data stored in s3 buckets.
- It is a fully managed service. It is serverless offering.
- Pricing is per query. 5Dollar per 1 TB query.
- We can optimmize the cost by using prefix in s3 bucket.
cost for 6 GB of data without prefix
2026/review/product-x-12
2026/review/product-x-13
2026/review/product-x-14
2026/review/product-x-15


cost only for 1 GB with prefix
2026/review/12/log
2026/review/13/log
2026/review/14/log
2026/review/15/log

We can filter based on where clause. where product = 12. Hence cost is reduced here

- We do not have to manage the server or database.
- It can query structured data such as CSV or semi structured data such as JSON.
- It supports csv, json, columnar data formats such as Parquet etc.
- It integrates witb the Amazon Quick Sight for data vizualization for viewing the graph and dashboards.
