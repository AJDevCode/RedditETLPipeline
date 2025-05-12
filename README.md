# Reddit Data Pipeline with Airflow, Celery, PostgreSQL, S3, AWS Glue, Athena, and Redshift

This repository contains a full-stack ETL (Extract, Transform, Load) data pipeline that ingests Reddit data and transforms it into structured insights within an Amazon Redshift data warehouse. This architecture is designed for scalability, automation, and robust data processing, leveraging a combination of industry-standard tools and AWS services.



## Key Features
The pipeline is designed to:

- Real-time Data Extraction: Retrieves data from Reddit using its API.
- Scalable Orchestration: Manages workflows and task distribution using Apache Airflow and Celery.
- Efficient Data Storage: Temporarily stages data in PostgreSQL and archives raw data in S3.
- Automated Data Transformation: Processes raw data using AWS Glue and Athena for efficient querying.
- Comprehensive Analytics: Loads structured data into Amazon Redshift for advanced analytics and business intelligence.

## Design
1. Reddit API : Data source for extracting posts and comments.
2. Apache Airflow & Celery:  Orchestration for the entire ETL pipeline.
3. PostgreSQL:  Temporary staging and metadata management.
4. Amazon S3 : Long-term raw data storage.
5. AWS Glue : Automated ETL and data cataloging.
6. Amazon Athena : SQL-based data transformation and analysis.
7. Amazon Redshift –: Scalable data warehousing for complex analytics.

## Prerequisites
- Reddit API credentials : Data Extraction
- AWS Account with the following service permissions:
   - S3, Glue, Athena, and Redshift
- Docker : For containerized deployment
- Python 3.9+ :  For the pipeline and related scripts

## Getting Started
1. Clone the repository.
   ```bash
    git clone https://github.com/AjDevCode/RedditETLPipeline.git
   ```
2. Create a virtual environment.
   ```bash
    python3 -m venv venv
   ```
3. Activate the virtual environment.
   ```bash
    source venv/bin/activate
   ```
4. Install the dependencies.
   ```bash
    pip install -r requirements.txt
   ```
5. Rename the configuration file and the credentials to the file.
   ```bash
    mv config/config.conf.example config/config.conf
   ```
6. Starting the containers
   ```bash
    docker-compose up -d
   ```
7. Launch the Airflow web UI.
   ```bash
    open http://localhost:8080
   ```

