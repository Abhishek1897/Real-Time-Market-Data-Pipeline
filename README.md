# Real-Time Data Pipeline using AWS Kinesis and Snowflake

## 📌 Project Overview

This project demonstrates the end-to-end implementation of a **real-time streaming data pipeline** using AWS services and Snowflake. The pipeline ingests global food market data through an API, transforms it in real-time using AWS Kinesis Firehose and Lambda, loads it into an S3 bucket, and finally processes and stores cleaned data in Snowflake for analytics and visualization in Power BI.

---

## 🚀 Use Case

Analyze **global food market trends** across 36 countries and 2,200 markets from 2007–2023 using real-time data ingestion and processing. The data includes:
- Country and market metadata
- Food item prices (open, high, low, close)
- Inflation and trust indicators

---

## 🔧 Tech Stack

| Layer              | Technologies Used |
|-------------------|-------------------|
| **Programming**   | Python, SQL        |
| **ETL/Streaming** | AWS Kinesis Data Streams, Kinesis Firehose |
| **API Layer**     | FastAPI via AWS App Runner |
| **Storage**       | AWS S3             |
| **Compute**       | AWS Lambda         |
| **Data Warehouse**| Snowflake (Snowpipe, Snowpark, Stored Procedures) |
| **Visualization** | Power BI           |
| **Libraries**     | `boto3`, `requests`, `pandas`, `fastapi`, `uvicorn` |

---

## 🛠 Architecture Workflow

1. **Raw Data Layer**:
   - Store raw dataset (CSV) in AWS S3 bucket.
   - Deploy FastAPI via AWS App Runner to expose filtered data from S3.
   - API queries data using filters like `year`, `country`, `market`.

2. **Streaming Layer**:
   - Use AWS Kinesis Data Streams to ingest real-time API data.
   - Transform JSON logs into CSV using AWS Lambda.
   - Send transformed data to S3 via AWS Kinesis Firehose.

3. **Transformation Layer**:
   - Ingest data from S3 into Snowflake using **Snowpipe**.
   - Clean and transform data using **Snowpark Python Sessions**.
   - Automate transformations with **Stored Procedures** and **Tasks**.

4. **Analytics Layer**:
   - Use Power BI connected to Snowflake for visualizing cleaned data.
   - Build dashboards showing trends by country, item, inflation, etc.

---

## 🧰 Setup Instructions

1. **Pre-requisites**
   - AWS Account
   - Snowflake Account
   - Power BI Desktop
   - GitHub for App Runner Deployment

2. **Steps Summary**
   - Upload raw data to S3.
   - Deploy FastAPI via AWS App Runner.
   - Set up Kinesis Data Stream + Firehose + Lambda.
   - Create Snowpipe and transformation scripts in Snowflake.
   - Build Power BI dashboard from Snowflake dataset.

---

## 📊 Sample Outputs

- Transformed CSV files in S3 bucket.
- Cleaned data tables in Snowflake (e.g., `RAW_DATA`, `CLEANSED_FOOD_DATA_NEW`).
- Power BI reports by country and market trends.

---

## 🔄 Automation Highlights

- **Lambda Triggered Transformations**: Converts streaming JSON logs to CSV.
- **Snowpipe + SQS Integration**: Auto-ingests new data to Snowflake.
- **Snowflake Tasks**: Runs Snowpark cleaning scripts daily.
- **App Runner Auto-deployment**: GitHub integration for API updates.

---

## ✅ Key Takeaways

- Practical use of **AWS Kinesis** for real-time streaming.
- Real-time **ETL pipeline** without managing servers.
- Hands-on with **Snowflake’s Snowpark** for Python transformations.
- Real-time dashboards in **Power BI**.
- End-to-end automation using cloud-native services.

---

## 📎 References

- [AWS Kinesis Documentation](https://docs.aws.amazon.com/kinesis/)
- [Snowflake Docs](https://docs.snowflake.com/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [Power BI](https://powerbi.microsoft.com/)

---

## 📬 Contact

For questions or contributions, feel free to reach out or fork this repository.

