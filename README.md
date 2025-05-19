# Fraud-Detection-Pipeline

## Overview

The Real-Time Credit Card Fraud Transaction Analytics Pipeline is a comprehensive solution designed to detect real-time fraudulent transactions by analysing historical and streaming transaction data. This project utilizes various AWS services and open-source technologies to efficiently process, analyze, visualize, and monitor credit card transactions.

## Description

This project integrates historical data stored in Amazon S3 with streaming data sourced from Confluent Kafka using Apache Spark. Leveraging Spark's powerful processing capabilities, the system applies predefined conditions to distinguish between fraudulent and genuine transactions in real time. The processed data is then written back to S3 for storage.

To enable seamless data exploration and visualization, the project utilizes AWS Athena for SQL-based queries on the stored data. Furthermore, the insights gained from the processed data are visualized using Tableau, and connected to the data source through a specialized connector.

To streamline the workflow and ensure reproducibility, the entire pipeline is automated using GitHub Actions, with infrastructure provisioning handled by CloudFormation templates (CFT). This end-to-end solution offers a robust, scalable, and automated framework for real-time fraud detection and actionable insights, enhancing decision-making processes.


## Key Components

### Data Sources
- **Historical Data**: Stored in S3, comprising over 8 million rows of transactional data.
- **Streaming Data**: Streamed through Confluent Kafka, representing real-time credit card transactions.

### Technologies Used
- **AWS RDS**: Database for storing unique customer information securely.
- **Apache Spark**: Processes and analyzes streaming and historical transaction data.
- **AWS EMR (Elastic MapReduce)**: Provides a managed big data framework for processing and analyzing large datasets in parallel.
- **AWS S3**: Stores analyzed data and serves as a data source for AWS Glue.
- **AWS Crawler**: Used for crawling data, cataloguing schemas, and preparing data for analysis.
- **Athena**: Enables ad-hoc querying of data stored in S3 via the Glue Data Catalog.
- **Tableau**: Visualizes insights derived from the analyzed data, facilitating interactive exploration.
- **AWS CloudFormation**: Automates the deployment and management of AWS resources.
- **GitActions**: Facilitates continuous integration and deployment processes.

## Workflow

1. **Data Ingestion**: Historical transactional data is fetched from S3, while real-time transaction streams are obtained from Confluent Kafka.
2. **Data Processing**: Apache Spark applies predefined rules to analyze the streaming data against historical transactions.
3. **Data Storage**: Analyzed data, including both genuine and fraudulent transactions, is stored in an AWS S3 bucket.
4. **Schema Management**: AWS Glue crawls the data, cataloguing schemas and making them available in the Glue Data Catalog.
5. **Ad-Hoc Queries**: Athena allows users to run ad-hoc queries against the data stored in S3, leveraging the Glue Data Catalog for schema information.
6. **Visualization**: Tableau connects to Athena using the ODBC Athena connector, enabling real-time visualization of transactional insights.
7. **Automation and Deployment**: The entire pipeline, including infrastructure provisioning and deployment, is automated using AWS CloudFormation and GitActions.

# Architecture
![FinalArchitecture](https://github.com/user-attachments/assets/cd37e506-6c7a-4abb-b8f8-38a0b1825903)

## Conclusion

The Real-Time Credit Card Fraud Transaction Analytics Pipeline delivers a scalable and automated system for identifying fraudulent transactions as they occur. Utilizing AWS services alongside open-source tools, it ensures efficient data processing, insightful analysis, real-time visualization, and continuous monitoring—helping organizations proactively protect against financial fraud.

## Final Single Dashboard:
![image](https://github.com/user-attachments/assets/fb79eb9b-4966-48ae-b2b9-bdeaac77027e)



