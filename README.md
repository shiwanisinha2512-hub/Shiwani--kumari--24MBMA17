# Salon & Spa Business Intelligence on Databricks 📈

![Spark](https://img.shields.io/badge/Apache%20Spark-3.5.0-E25A1C?logo=apache-spark&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-Workspace-FF3621?logo=databricks)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

A comprehensive data analysis project for a Salon & Spa chain, built to run on the Databricks platform. This repository contains the PySpark script, sample data, and setup instructions to extract key business insights from appointment records.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Analyses](#key-analyses-performed)
- [Technology Stack](#technology-stack)
- [Directory Structure](#directory-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Setup Instructions](#setup-instructions)
- [Running the Analysis](#-running-the-analysis)
- [Expected Output](#-output-and-visualizations)
- [Contributing](#-contributing)
- [License](#-license)

---

## Project Overview

The goal of this project is to analyze salon appointment data to uncover actionable insights. By processing data on customers, services, and appointments, we can answer critical business questions to optimize staffing, personalize marketing campaigns, manage inventory, and improve overall salon performance. The entire data processing pipeline is designed to be executed within a Databricks notebook.

---

## Key Analyses Performed

The notebook performs five key business intelligence analyses:

1.  *⭐ Popular Services*: Identifies the most frequently booked services.
2.  *⏰ Peak Business Times*: Determines the busiest hours of the day to optimize staff scheduling.
3.  *💰 Revenue by Service*: Ranks services by total revenue generated, highlighting the most profitable offerings.
4.  *💖 Customer Loyalty*: Segments repeat customers to inform loyalty programs and marketing efforts.
5.  *🏢 Salon Performance*: Compares revenue and appointment volume across different salon branches.

---

## Technology Stack

* *Platform: **Databricks* (Unity Catalog enabled)
* *Core Engine: **Apache Spark* for distributed data processing.
* *API/Language: **PySpark* (Python API for Spark).
* *Data Storage*: CSV files hosted in a Databricks Volume.

---

## Directory Structure


salon-spa-databricks-project/
│
├── data/
│   ├── appointments.csv
│   ├── customers.csv
│   ├── salons.csv
│   └── services.csv
│
├── salon_spa_analysis.py       # The main PySpark script to be used in the notebook
└── README.md                   # This README file


---

## 🚀 Getting Started

Follow these instructions to clone the repository and set up the project on Databricks.

### Prerequisites

* *Git* installed on your local machine.
* An active *Databricks* account with access to a cluster and Unity Catalog.

### Setup Instructions

*Step 1: Clone the Repository*

First, clone this repository to your local machine:

bash
git clone [https://github.com/](https://github.com/)<your-username>/salon-spa-databricks-project.git
cd salon-spa-databricks-project


*Step 2: Upload Data to a Databricks Volume*

1.  In your Databricks workspace, navigate to the *Data Explorer*.
2.  Select a catalog and schema, and then choose *Create > Create volume*. Name the volume salon_data.
3.  Once created, select the volume and click *Upload to this volume*. Upload all four CSV files located in the data/ directory of the cloned repository.

*Step 3: Set Up the Databricks Notebook*

1.  Create a new notebook in your Databricks workspace.
2.  Open the salon_spa_analysis.py file from the cloned repository, copy its entire content, and paste it into a cell in your new notebook.
3.  *This is the most important step:* Update the base_path variable in the notebook to match your specific Databricks Volume path.

    python
    # Find this section in the notebook and update the path
    # ----------------- CONFIGURATION (CODE FIX) -----------------
    base_path = "/Volumes/<your_catalog>/<your_schema>/salon_data/"
    

---

## ▶️ Running the Analysis

Once the setup is complete, simply attach a running cluster to your notebook and execute the cell containing the PySpark code. The script will print status updates and display the resulting DataFrames as interactive tables.

---

## 📄 Output and Visualizations

The script generates two forms of output:

1.  *CSV Files*: The five analysis results are saved as CSV files in a new outputs/ folder within your Databricks Volume (.../salon_data/outputs/).
2.  *Interactive Dashboards*: Each of the five analysis DataFrames is displayed in the notebook using the display() function. You can use the built-in Databricks visualization tools to instantly create charts from these tables to form a dashboard.



---

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improvements or want to add new analyses, please follow these steps:

1.  Fork the repository.
2.  Create a new branch (git checkout -b feature/NewAnalysis).
3.  Make your changes and commit them (git commit -m 'Add new analysis for X').
4.  Push to the branch (git push origin feature/NewAnalysis).
5.  Open a Pull Request.

---

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for details.
