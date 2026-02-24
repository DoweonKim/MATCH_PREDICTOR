# ⚽ MATCH_PREDICTOR

An end-to-end data engineering pipeline that collects football (soccer) match data from API-Football, processes it using Python, and stores structured results in Supabase.

The entire workflow is fully automated and deployed on AWS using Docker, Lambda, and EventBridge.

---

## 🚀 Features

- Collects EPL 2023/24 fixtures, team statistics, and player data from API-Football  
- Transforms raw JSON responses into clean and structured datasets using Pandas  
- Loads processed data into Supabase (PostgreSQL backend)  
- Fully automated daily ingestion with AWS Lambda and EventBridge  
- Containerized with Docker and deployed via AWS ECR  

---

## 📂 Project Structure

api/ # API requests (fixtures, teams, players)
processing/ # Data cleaning and transformation
pipeline/ # Data upload to Supabase
main.py # End-to-end ETL pipeline entry point
Dockerfile # Container configuration for AWS Lambda deployment


---

## 🛠️ Tech Stack

- Python (Pandas, Requests)
- Supabase (PostgreSQL)
- Docker
- AWS Lambda
- AWS EventBridge
- AWS CloudWatch
- AWS ECR

---

## ⚡ Automation

The pipeline runs automatically every day at midnight (CST) using AWS EventBridge, ensuring the Supabase database stays continuously updated with the latest match data.

---

## 📊 Workflow Overview

1. Retrieve football match data from API-Football  
2. Transform and clean raw JSON into structured DataFrames  
3. Load processed data into Supabase  
4. Monitor execution logs and errors using AWS CloudWatch  

---

## 🔒 Environment Variables

Sensitive credentials are securely stored using environment variables defined in a `.env` file.

Example:
