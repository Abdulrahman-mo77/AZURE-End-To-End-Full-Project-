# Azure End-to-End Real-Time Data Engineering Project

## Overview

This project demonstrates a complete end-to-end data engineering pipeline on Microsoft Azure, designed to solve a simulated business problem. It showcases how to ingest data from an on-premises SQL Server, process and transform it in the cloud, and deliver actionable business insights through analytics and visualization tools.

The primary objective of this project is to strengthen practical knowledge of modern data engineering concepts, cloud-native services, and real-time analytics workflows using Azure.

---

## Business Problem

The business lacks visibility into customer demographics, specifically gender distribution, and how these demographics influence product purchasing behavior.

### Key Business Questions
- How do sales vary by gender and product category?
- What are the total sales revenue and product volumes sold?
- How do these metrics change over time?

---

## Business Requirements

1. Sales & Demographics Dashboard
   - Total sales revenue
   - Total products sold
   - Customer gender distribution
   - Product category performance

2. Dynamic Filtering
   - Filter data by date, product category, and gender

3. Self-Service Analytics
   - A user-friendly interface for business stakeholders

---

## Solution Architecture

This solution follows the Medallion Architecture (Bronze, Silver, Gold):

### Data Ingestion
- Extract data from an on-premises SQL Server
- Orchestrate ingestion using Azure Data Factory
- Store raw data in Azure Data Lake Storage (Bronze layer)

### Data Transformation
- Transform and clean data using Azure Databricks
- Move data through Bronze → Silver → Gold layers

### Data Warehousing & Analytics
- Load curated data into Azure Synapse Analytics
- Enable scalable SQL-based analytics

### Data Visualization
- Build interactive dashboards using Power BI connected to Synapse

### Automation
- Schedule daily pipeline executions using Azure Data Factory

---

## Technology Stack

- Azure Data Factory (ADF)
- Azure Data Lake Storage Gen2
- Azure Databricks
- Azure Synapse Analytics
- Power BI
- Azure Key Vault
- Azure Entra ID (Azure Active Directory)
- On-Premises SQL Server

---

## Setup & Deployment

### Prerequisites
- Active Azure subscription
- On-premises SQL Server with AdventureWorks database

### Step 1: Azure Environment Setup
- Create Resource Group
- Provision ADF, ADLS, Databricks, Synapse, and Key Vault

### Step 2: Data Ingestion
- Restore AdventureWorks database
- Build ADF pipelines to ingest data into Bronze layer

### Step 3: Data Transformation
- Mount ADLS in Databricks
- Develop transformation notebooks

### Step 4: Data Loading & Reporting
- Load Gold data into Synapse
- Build Power BI dashboards

### Step 5: Automation & Monitoring
- Schedule pipelines
- Monitor runs via ADF and Synapse

### Step 6: Security & Governance
- Configure RBAC using Azure Entra ID
- Secure secrets with Azure Key Vault

### Step 7: End-to-End Testing
- Insert new source data
- Validate pipeline execution and dashboard updates

---

## Conclusion

This project provides a production-style, scalable data engineering solution on Azure. It demonstrates industry best practices for data ingestion, transformation, analytics, automation, and security.
