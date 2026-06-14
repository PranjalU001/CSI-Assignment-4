# CSI-Assignment-4
# Week 4 Assignment

# Azure Cloud Fundamentals and Data Pipeline Implementation using Azure Data Factory

---

## Objective

To understand Azure cloud fundamentals and build a complete data pipeline using Azure Storage Account and Azure Data Factory.

---

# Assignment Overview

This Week 4 Assignment demonstrates the implementation of an end-to-end Azure Data Factory (ADF) pipeline. The project reads a CSV file from Azure Blob Storage, validates file metadata using the Get Metadata activity, and copies the file to a new destination location using the Copy Data activity.

The assignment covers:

- Azure Resource Group
- Azure Storage Account
- Azure Blob Storage
- Azure Data Factory (ADF)
- Linked Service
- Source and Destination Datasets
- Get Metadata Activity
- Copy Data Activity
- IAM Role Assignment
- Pipeline Validation and Execution

---

# Technologies Used

- Microsoft Azure
- Azure Resource Manager
- Azure Storage Account
- Azure Blob Storage
- Azure Data Factory (ADF)
- Azure Identity and Access Management (IAM)
- CSV File Processing

---

# Project Architecture

```text
Sample - Superstore.csv
          │
          ▼
Azure Blob Storage
(source-data)
          │
          ▼
Linked Service
(LS_BlobStorage)
          │
          ▼
Source Dataset
(DS_Source_CSV)
          │
          ▼
Get Metadata Activity
(File Validation)
          │
          ▼
Copy Data Activity
          │
          ▼
Destination Dataset
(DS_Destination_CSV)
          │
          ▼
output.csv
(destination-data)
```

---

# Azure Resources Used

| Resource Type | Resource Name |
|--------------|--------------|
| Resource Group | rg-adf-assignment |
| Storage Account | storagepranjal001 |
| Source Container | source-data |
| Destination Container | destination-data |
| Azure Data Factory | adf-pranjal18 |
| Linked Service | LS_BlobStorage |
| Source Dataset | DS_Source_CSV |
| Destination Dataset | DS_Destination_CSV |
| Pipeline | PL_CopyData |

---

# Task 1: Explore Azure Portal and Create Resource Group

## Description

A Resource Group was created to organize and manage all Azure resources used in this project.

### Resource Group

```text
rg-adf-assignment
```

### Deliverable

- Screenshot of Resource Group

---

# Task 2: Storage Setup

## Description

A Storage Account was created for storing source and destination data files.

### Storage Account

```text
storagepranjal001
```

### Blob Containers Created

```text
source-data
destination-data
```

### Uploaded File

```text
Sample - Superstore.csv
```

### Deliverables

- Screenshot of Storage Account
- Screenshot of Blob Containers
- Screenshot of Uploaded CSV File

---

# Task 3: Azure Data Factory Basics

## Description

An Azure Data Factory instance was created and configured to process the CSV file.

### Azure Data Factory

```text
adf-pranjal18
```

### ADF Components Explored

- Author
- Monitor
- Manage

### Linked Service

```text
LS_BlobStorage
```

Purpose:

Connect Azure Data Factory with Azure Blob Storage.

### Source Dataset

```text
DS_Source_CSV
```

Configuration:

- Linked Service: LS_BlobStorage
- Container: source-data
- File: Sample - Superstore.csv

### Destination Dataset

```text
DS_Destination_CSV
```

Configuration:

- Linked Service: LS_BlobStorage
- Container: destination-data
- Output File: output.csv

### Deliverables

- Screenshot of Azure Data Factory Home Page
- Screenshot of Linked Service
- Screenshot of Source Dataset
- Screenshot of Destination Dataset

---

# Task 4: Pipeline Development

## Description

A pipeline was developed using Get Metadata and Copy Data activities.

### Pipeline Name

```text
PL_CopyData
```

### Activities Used

#### Get Metadata Activity

Purpose:

Validate the source file before processing.

Metadata Fields Checked:

- Exists
- Size
- Last Modified

#### Copy Data Activity

Purpose:

Copy CSV data from source container to destination container.

### Pipeline Workflow

```text
Get Metadata
      │
      ▼
Copy Data
```

### Deliverable

- Screenshot of Complete Pipeline Design

---

# Task 5: Pipeline Validation and Execution

## Description

The pipeline was validated, published, and executed successfully.

### Validation

Pipeline validation completed successfully.

### Publishing

Pipeline published successfully.

### Execution

Pipeline executed using:

```text
Debug Mode
```

Execution Process:

1. Source file detected successfully.
2. Metadata validated successfully.
3. Data copied successfully.
4. Output file generated successfully.

### Deliverables

- Screenshot of Validation Successful
- Screenshot of Publish Successful
- Screenshot of Pipeline Execution

---

# Task 6: IAM Role Assignment

## Description

Role-based access control was configured for storage access.

### Roles Assigned

#### Reader

Provides read-only access to Azure resources.

#### Contributor

Provides create, update, and delete permissions.

#### Storage Access

ADF was granted access to Blob Storage for performing data movement operations.

### Deliverable

- Screenshot of IAM Role Assignment

---

# Mini Project

## Title

CSV Data Processing Pipeline using Azure Blob Storage and Azure Data Factory

---

## Problem Statement

Build a complete pipeline that reads a CSV file from Azure Blob Storage and processes it using Azure Data Factory.

---

## Objective

Design and implement a complete data pipeline that validates metadata and copies a CSV file from a source location to a destination location.

---

## Requirements

### Source

CSV file stored in Azure Blob Storage.

### Components Used

- Azure Resource Group
- Azure Storage Account
- Azure Blob Containers
- Azure Data Factory
- Linked Service
- Source Dataset
- Destination Dataset
- Get Metadata Activity
- Copy Data Activity

### Process

1. Read CSV file from source container.
2. Validate metadata using Get Metadata activity.
3. Copy file using Copy Data activity.
4. Monitor pipeline execution.

### Destination

New file location inside Azure Blob Storage.

---

# Repository Structure

```text
├── Assignment - 4.pdf
├── README.md
├── Sample - Superstore.csv
└── output.csv
```

---

# Files Included

## 1. Assignment - 4.pdf

Contains the complete Week 4 Assignment documentation including:

- Task 1: Resource Group Creation
- Task 2: Storage Setup
- Task 3: Azure Data Factory Configuration
- Task 4: Pipeline Development
- Task 5: Pipeline Execution
- Task 6: IAM Role Assignment
- Mini Project Documentation
- Screenshots and Results

---

## 2. Sample - Superstore.csv

This is the source dataset used in the project.

Purpose:

- Stored inside Azure Blob Storage
- Used as input for Azure Data Factory
- Metadata validated using Get Metadata Activity
- Processed and copied using Copy Data Activity

---

## 3. output.csv

This is the output file generated by the Azure Data Factory pipeline.

Purpose:

- Generated after successful pipeline execution
- Stored in destination location
- Verifies successful data transfer

---

# Repository Workflow

```text
Sample - Superstore.csv
          │
          ▼
Azure Blob Storage
(source-data)
          │
          ▼
Azure Data Factory
(PL_CopyData)
          │
          ▼
Get Metadata
(File Validation)
          │
          ▼
Copy Data
          │
          ▼
output.csv
```

---

# Verification

The following project components were successfully verified:

| Component | Status |
|------------|---------|
| Resource Group | ✅ |
| Storage Account | ✅ |
| Blob Containers | ✅ |
| CSV Upload | ✅ |
| Linked Service | ✅ |
| Source Dataset | ✅ |
| Destination Dataset | ✅ |
| Metadata Validation | ✅ |
| Copy Data Activity | ✅ |
| Pipeline Validation | ✅ |
| Pipeline Publishing | ✅ |
| Pipeline Execution | ✅ |
| Output File Generated | ✅ |
| IAM Roles | ✅ |

---

# Output Generated

Source File:

```text
Sample - Superstore.csv
```

Generated File:

```text
output.csv
```

Pipeline Status:

```text
Succeeded
```

---

# Future Enhancements

This project can be extended by:

- Processing multiple CSV files using ForEach Activity
- Scheduling pipelines using Triggers
- Integrating Azure SQL Database
- Implementing Data Flow Transformations
- Creating automated monitoring and alerting
- Using Azure Data Lake Storage

---

# Author

**Pranjal Upadhyay**

B.Tech – Computer Science (AI & Data Science)

Week 4 Assignment

Azure Cloud Fundamentals and Data Pipeline Implementation using Azure Data Factory
