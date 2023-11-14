# Modern Analytics with Microsoft Fabric and Azure Databricks DREAM Lab

**The estimated time to complete this lab is 45-60 minutes.**

## Table of contents

### Exercise 1: Data Engineering experience, Data ingestion from a spectrum of analytical data sources into OneLake

- Task 1.1: Create a Microsoft Fabric enabled workspace

- Task 1.2: Create/Build a Lakehouse

- Task 1.3: Data ingestion
    -   Using Data Pipelines/Data Flow ‘No Code-Low Code experience’
	-   Using ‘New Shortcut’ option from external data sources
    -   Using Spark Notebook ‘Code-first experience’

### Exercise 2: Explore an analytics pipeline using open Delta format and Azure Databricks Delta Live Tables. Stitch data (landed earlier) to create a combined data product to build a simple Lakehouse and integrate with OneLake

- Task 2.1: Set up an Azure Databricks environment

- Task 2.2: Create a Delta Live Table pipeline

- Task 2.3: Explore SQL Analytics with Lakehouse SQL-endpoint

### Exercise 3: Data Science experience, explore Machine Learning and Business Intelligence scenarios

- Task 3.1: Build ML models, experiments, Log ML model in the built-in model registry using MLflow and batch scoring

### Exercise 4: Data Warehouse experience, explore SQL Analytics with Data Warehouse

- Task 4.1: Create a Data Warehouse

- Task 4.2: Load data in the warehouse

- Task 4.3: Create virtual Data Warehouses 

### Exercise 5: Power BI reports with Direct Lake

- Task 5.1: Leverage Power BI to derive actionable insights from data in Lakehouse using Direct Lake mode

### Exercise 6 (OPTIONAL): Real-time Analytics experience, explore Streaming data using KQL DB for a near real-time analytics scenario

- Task 6.1: Create a KQL Database

- Task 6.2: Ingest real-time/historical data into KQL DB

- Task 6.3: Analyze/discover patterns, identify anomalies and outliers using Kusto Query Language

- Task 6.4: Create a Real-time Power BI report using KQL DB/KQL Query


## Overview

![Showcase Image](media/architectureDiagramFabric.png)

This lab showcases Modern Analytics with Microsoft Fabric and Azure Databricks, featuring a cost-effective, performance-optimized, and cloud-native Analytics solution pattern. This architecture unifies our customers' data estate to accelerate data value creation. The visual illustrates the real-world example for Contoso, a fictitious company. Contoso a retailer with thousands of brick-and-mortar stores across the world. They also have an online store. Contoso is acquiring Litware Inc. Litware has curated marketing data and sales data processed by Azure Databricks and stored in the gold layer in ADLS Gen 2. During our exercises, we will see how they leveraged the power of Microsoft Fabric to ingest data from disparate sources, combine data with their existing data from ADLS Gen 2, derive meaningful insights. You will witness how the team used a shortcut to reference the existing Litware Inc data from ADLS Gen 2. You will also see how they mounted the OneLake endpoint in Azure Databricks to derive meaningful insights using the compute in Azure Databricks.

The lab scenario starts on January 30th. The company's new CEO, April, recently noticed negative trends in their KPIs, including:

* High customer churn
* Declining sales revenue
* High bounce rate on their website
* High operating expense
* Poor customer experience

April talks to Rupesh, the Chief Data Officer to create a data driven organization and reverse these adverse KPI trends. Rupesh talks to his technical team including Eva the data engineer, Miguel the data scientist and Wendy the business analyst to design and implement a solution pattern to realize this dream of a data driven organization. Our story is centered around Rupesh and his team. They recognize that the existence of data silos within Contoso's various departments presents a significant integration challenge.

During this lab you will execute some of these steps as a part of this team to reverse these adverse KPI trends.

Here are the Microsoft Fabric workloads showcased in this solution along with Azure Databricks.

**1. Synapse Data Engineering:**

Combines the best of the data lake and warehouse, removing the friction of ingesting, transforming, and sharing organizational data, all in an open format. Users can choose from various ways of bringing data into the Lakehouse including dataflow & pipelines, and they can even use shortcuts to create virtual folders and tables without any data movement between the storage accounts.

**2. Data Factory:**

Data Factory empowers users with modern data integration experience to ingest, prepare and transform data with intelligent transformations, and leverage a rich set of activities implementing dataflows and pipelines. Dataflows provide a low-code interface for ingesting data from hundreds of data sources, with 300+ data transformations. Data pipelines enable powerful workflow capabilities to build complex ETL and data factory workflows that can perform many different tasks at scale, refresh dataflow, move PB-size data, and define sophisticated control flow pipelines.

**3. Synapse Data Science:**

Microsoft Fabric offers Data Science experiences, all the way from data exploration, preparation and cleansing to experimentation, modeling, model scoring and serving of predictive insights to BI reports. Synapse Data Science in Microsoft Fabric allows data science practitioners to work seamlessly on top of the same secured and governed data that has been prepared by data engineering teams, thus eliminating the need to copy data. The open Delta Lake support allows data science users to version datasets to create reproducible machine learning code.

**4. Synapse Data Warehouse:**

Microsoft Fabric introduces a lake centric data warehouse built on an enterprise grade distributed processing engine that enables industry leading performance at scale while eliminating the need for configuration and management. The Warehouse is built for any skill level - from the citizen developer through to the professional developer, DBA or data engineer. The rich set of experiences built into Microsoft Fabric workspace enables customers to reduce their time to insights by having an easily consumable, always connected dataset that is integrated with Power BI in Direct Lake mode.

**5. Power BI:**

Power BI is standardizing open data formats by adopting Delta Lake and Parquet as its native storage format to avoid vendor lock-in and reduce data duplication and management. Direct Lake mode unlocks incredible performance directly against OneLake, with no data movement. Power BI datasets in Direct Lake mode enjoy query performance on par with import mode, with the real-time nature of DirectQuery. And the data never leaves the lake.

**6. Synapse Real-time Analytics:**

Real-time Analytics is seamlessly integrated into Microsoft Fabric's suite of products, facilitating data loading, transformation, and advanced visualization. It ensures swift access to data insights through automatic data streaming, indexing, data partitioning, and on-demand query generation and visualizations. Data loaded into a KQL database can be accessed in OneLake and is exposed to other Microsoft Fabric experiences. A KQL queryset to run queries, view, and customize query results on data. The KQL queryset allows you to save queries for future use, export, and share queries with others. It includes the option to generate a Power BI report.
