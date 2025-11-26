# Azure Arc Software Assurance Workbook

## Purpose

The purpose of this repository is to provide an Azure Workbook for monitoring Software Assurance compliance across your Azure Arc-enabled infrastructure. This workbook simplifies license management, enhances visibility into hybrid environments, and enables proactive compliance monitoring for both Windows Servers and SQL Server instances.

## Features

* **Centralized Software Assurance monitoring** for Azure Arc-enabled servers and SQL instances
* **Real-time compliance tracking** with visual dashboards and metrics
* **Filtering capabilities** by subscription, resource group, and server type
* **Detailed server inventory** with licensing information and infrastructure details
* **Built-in guidance** with links to official Microsoft documentation for enabling Software Assurance
* **Multi-platform support** including Azure Local (HCI), SCVMM, VMware vSphere, AWS, GCP, and physical servers

## Screenshots

![Azure Arc Software Assurance Dashboard](screenshots/example1.png)
![Azure Arc Software Assurance Dashboard](screenshots/example2.png)

## Architecture Overview

The workbook queries Azure Resource Graph to collect licensing information from Arc-enabled resources across your hybrid infrastructure. The main components include:

* **Azure Resource Graph** - Data source for Arc resource information
* **Azure Workbook** - Visualization and dashboard interface
* **Arc-enabled Windows Servers** - Servers with license profile configuration
* **Arc-enabled SQL Server instances** - SQL instances with license type configuration
* **Azure Portal** - Centralized access point for monitoring

This architecture provides a unified view across hybrid environments, enabling consistent license compliance monitoring and reporting.

## Prerequisites

* An active Azure subscription with Arc-enabled servers and/or SQL instances
* **Azure Arc-enabled Windows Servers** with license profiles configured
* **Azure Arc-enabled SQL Server instances** with license types configured
* **Reader permissions** on the subscriptions and resource groups containing Arc resources
* Access to **Azure Workbooks** in the Azure Portal

## Usage

### Step 1: Deploy the Workbook

* Download the workbook JSON file from this repository
* In the Azure Portal, navigate to **Azure Workbooks**
* Click **New** → **Advanced Editor**
* Paste the JSON content from `arc-sa-overview.json`
* Click **Done Editing** and **Save** the workbook

### Step 2: Monitor Software Assurance Compliance

The workbook provides several views:

**Summary Tiles:**
* Arc Servers - Software Assurance Enabled/Disabled counts
* Arc SQL Servers - Software Assurance Enabled/Disabled counts  
* Coverage percentage for both Windows Server and SQL Server

**Server Inventory Table:**
* Detailed list of all Arc-enabled servers and SQL instances
* License compliance status with visual indicators
* Server type, version, infrastructure kind, and location information
* Built-in filtering capabilities for focused analysis

### Step 3: Enable Software Assurance for Non-Compliant Resources

For servers showing as "Software Assurance Disabled":

**For SQL Server instances:**
* Configure the license type to "Paid" in the Azure Portal

**For Windows Servers:**
* Enable Software Assurance in the license profile settings

## Potential Use Cases

* **License Compliance Monitoring:** Track Software Assurance configuration across hybrid infrastructure
* **Cost Optimization:** Identify servers eligible for Azure Hybrid Benefit through Software Assurance
* **Audit & Reporting:** Generate compliance reports for license audits and governance
* **Hybrid Cloud Visibility:** Gain insights across on-premises, multi-cloud, and Azure environments
