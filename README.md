# Reddit ETL Pipeline

A data pipeline to extract Reddit data from [r/dataengineering](https://www.reddit.com/r/dataengineering/).

Output is a Google Data Studio report, providing insight into the Data Engineering official subreddit.

## Motivation

Project was based on an interest in Data Engineering and the types of Q&A found on the official subreddit.

It also provided a good opportunity to develop skills and experience in a range of tools. As such, project is more complex than required, utilising dbt, airflow, docker and cloud based storage.

## Architecture

<img src="images/architecture.png" width=100% height=100%>

1. Extract data using [Reddit API](https://www.reddit.com/dev/api/)
1. Load into [AWS S3](https://aws.amazon.com/s3/)
1. Copy into [AWS Redshift](https://aws.amazon.com/redshift/)
1. Transform using [dbt](https://www.getdbt.com)
1. Create [PowerBI](https://powerbi.microsoft.com/en-gb/) or [Locker Studio](https://lockerstudio.google.com) Dashboard
1. Orchestrate with [Airflow](https://airflow.apache.org) in [Docker](https://www.docker.com)
1. Create AWS resources with [Terraform](https://www.terraform.io)

## Report

[DEMO](https://lookerstudio.google.com/reporting/99b501fd-ef53-4b35-8b67-511c3ff65d4a)

<img src="images/Report_Reddit.png" width=100% height=100%>

## Setup

Follow below steps to setup pipeline. I've tried to explain steps where I can. Feel free to make improvements/changes.

As AWS offer a free tier, this shouldn't cost you anything unless you amend the pipeline to extract large amounts of data, or keep infrastructure running for 2+ months. However, please check [AWS free tier](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all) limits, as this may change.

First clone the repository into your home directory and follow the steps.

```bash
git clone https://github.com/nits302/Reddit_ETL_Pipilne.git
```

### Getting Started

To begin using the project, follow these steps:

1. [Overview](instructions/overview.md)
1. [Reddit API Configuration](instructions/reddit.md)
1. [AWS Account](instructions/aws.md)
1. [Infrastructure with Terraform](instructions/setup_infrastructure.md)
1. [Configuration Details](instructions/config.md)
1. [Docker & Airflow](instructions/docker_airflow.md)
1. [dbt](instructions/dbt.md)
1. [Dashboard](instructions/visualisation.md)
1. [Final Notes & Termination](instructions/terminate.md)
1. [Improvements](instructions/improvements.md)

## More Details

Project Structure: The project's structure includes directories for infrastructure (Terraform), configuration (AWS and Airflow), data extraction (Python scripts), and optional steps like dbt and BI tools integration.

Customization: Feel free to customize the project by modifying configurations, adding new data sources, or integrating additional tools as needed.

## 🚀 Video DEMO

[Demo Project Reddit ETL Pipeline](https://youtu.be/GuAIBefWA94)
