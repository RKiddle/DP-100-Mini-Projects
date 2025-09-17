# 🧪 Week 1: Azure ML Workspace Setup — “Build Your Lab”

This guide walks you through setting up a reproducible Azure Machine Learning workspace linked to GitHub, with compute targets, datastores, and Conda environments configured for DP-100 mini projects.

---

## 🧠 Objectives

- Create and configure an Azure ML workspace
- Link GitHub repo for version control
- Set up compute targets (CPU, GPU, Spark)
- Register a datastore with sample datasets
- Configure Conda environment for reproducible workflows

---

## 🛠️ Step-by-Step Setup

### 1. Create Azure ML Workspace

1. Go to [Azure ML Studio](https://ml.azure.com/)
2. Click **Create Workspace**
3. Fill in:
   - **Name**: `dp100-lab-rjk`
   - **Subscription**: Your active Azure subscription
   - **Resource Group**: `rjk233-rg` (or create new)
   - **Region**: `East US 2` or preferred region
4. Click **Review + Create**

---

### 2. Link GitHub Repo

1. In Azure ML Studio, go to **Linked Services**
2. Click **+ New GitHub Repository**
3. Link to: `https://github.com/RKiddle/DP-100-Mini-Projects`
4. Select branch: `main`
5. Enable version control for notebooks and pipeline components

---

### 3. Set Up Compute Targets

Go to **Compute > + New Compute** and create:

| Type      | Name             | Size         | Notes                          |
|-----------|------------------|--------------|--------------------------------|
| CPU       | `cpu-cluster`    | Standard_DS3 | Default training & notebooks   |
| GPU       | `gpu-cluster`    | Standard_NC6 | For deep learning & AutoML     |
| Spark     | `spark-pool`     | 3 nodes
