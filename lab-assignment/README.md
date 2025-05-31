# Azure AI Translator Service - Lab Overview

This repository contains resources and step-by-step instructions to build a hands-on lab for the **Azure AI Translator Service**. The lab demonstrates how to provision, configure, and use Azure’s AI-powered text translation service within a cloud-native environment.

---

## 📌 Overview of Azure AI Translator

**Azure AI Translator** is part of the **Azure Cognitive Services** suite. It provides real-time, AI-powered text translation capabilities that support over 100 languages and dialects. This API-based service is ideal for integrating multi-language translation features into applications, enabling global communication and accessibility.

Key features include:

- **Real-time translation** of text from one language to another.
- **Language detection** to automatically identify the source language.
- **Scalability and flexibility** for integration in web, mobile, or enterprise applications.
- **Secure and compliant** platform hosted on Azure, leveraging global infrastructure.

---

## 🎯 Lab Objectives

In this lab, you will:

✅ Provision an **Azure Cognitive Services Translator** resource using an ARM template.  
✅ Retrieve the **subscription key** and **endpoint URL** for API access.  
✅ Use **Python** to call the **Azure Translator REST API** and translate text between multiple languages.

---

## 🛠️ Prerequisites

- **Azure subscription** with appropriate access to create resources.
- **Azure CLI** installed and authenticated.  
  [Install the CLI here](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest).

- **Python 3.x** installed with the `requests` library:
  ```bash
  pip install requests
## Prerequisites

- An active [Azure account](https://azure.microsoft.com/free/).
- Azure CLI installed. Install it [here](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli).
- Basic familiarity with Azure services.

---

## Lab Setup

### Step 1: Create an Azure Account

1. Visit the [Azure Free Account page](https://azure.microsoft.com/free/).
2. Click **Start free**.
3. Follow the prompts to create your Azure account.

---

### Step 2: Sign in to Azure Portal

1. Go to the [Azure Portal](https://portal.azure.com/).
2. Log in with your Azure account.

---

### Step 3: Create a Resource Group

A resource group is a container that holds related resources for your solution.

#### Azure Portal:

1. In the Azure Portal, click on **Resource groups**.
2. Click on **+ Create**.
3. Enter the following:
   - **Subscription**: Select your subscription.
   - **Resource group**: Provide a unique name (e.g., `translator-lab-rg`).
   - **Region**: Choose the region closest to you.
4. Click **Review + create**, then **Create**.

#### Azure CLI:

```bash
az login
az group create --name translator-lab-rg --location eastus