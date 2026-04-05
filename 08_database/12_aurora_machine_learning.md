# typical machine learning architecture
- application stores data in aurora
- Data is pushed to s3
- Machine learning model reads from s3 and inference the data
- The ML data is now available via an endpoint
- Application can access the endpoint for ML data

# Aurora machine learning
- WIth aurora machine learning, ML data can be integrated with databse and we can query it using sql queries
- 1. App write to aurora database
  2. Required data is pushed to s3 bucket
  3. AWS Sagemaker autopilor pull data and pre-process and train ML model
  4. ML data is availabel via AWS Sagemake endpoint
  5. The data is now stored in Aurora columna along with data.
  6. App can now query the ML data using sql queries.

<img width="384" height="559" alt="Screenshot 2026-04-05 at 4 33 47 PM" src="https://github.com/user-attachments/assets/bf790418-0d20-4556-a995-f3f6de1d78e3" />
