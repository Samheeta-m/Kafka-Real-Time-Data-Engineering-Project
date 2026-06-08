# Real-Time Data Pipeline Using Apache Kafka and AWS

## Overview
This project simulates a **real-time data engineering pipeline** using **Apache Kafka** and **AWS**.

A Python-based producer streams stock market data into Kafka topics, while a consumer processes the data and stores it in **Amazon S3** for downstream analytics.  
The project was built as a **hands-on learning exercise** to understand streaming data pipelines and their operational aspects.


**Business framing:** similar pipelines power real-time recommendation engines, 
live pricing updates, and user behaviour tracking in consumer tech platforms.

---

## Architecture
```markdown
Python Producer
      ↓
Apache Kafka (Topics)
      ↓
Python Consumer
      ↓
Amazon S3
      ↓
AWS Glue + Athena (Analytics)
```
| Step | Description |
|------|-------------|
| 1. Produce | Python producer simulates live stock market feed |
| 2. Stream | Messages published to Kafka topic with partitioning |
| 3. Consume | Python consumer reads and processes stream |
| 4. Store | Data stored in Amazon S3 as JSON records |
| 5. Analyse | AWS Glue catalogues data, Athena queries with SQL |
---

## Technologies Used
- Apache Kafka
- Python
- Amazon EC2
- Amazon S3
- AWS Glue
- Amazon Athena

---

## Data
- Simulated stock market data
- JSON message format

---

## Key Features
- Real-time data ingestion using Kafka producers
- Topic-based message streaming
- Consumer-based data processing
- Fault-tolerant message handling using Kafka offsets
- Cloud-based storage and SQL analytics

---

## What I Learned
- Kafka producer–consumer architecture
- Topic creation, partitions, and offsets
- How Kafka enables decoupled and fault-tolerant streaming
- Integrating streaming pipelines with cloud storage
- Querying data using serverless analytics tools

---

## How to Run (High Level)
1. Start Zookeeper and Kafka broker
2. Create a Kafka topic
3. Run the Python producer to stream data
4. Run the Python consumer to process and store data in S3
5. Use AWS Glue and Athena to query the data

---

## Notes
This project focuses on **streaming ingestion and pipeline reliability**, rather than real-time dashboards or alerting systems.
