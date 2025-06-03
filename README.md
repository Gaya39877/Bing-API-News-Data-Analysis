
# 📰 Bing News Data Ingestion & Analysis

This project ingests the latest news articles using the **Bing News Search API**, processes the data using Microsoft Fabric, and visualizes insights via a Power BI dashboard. It enables automated data collection, cleansing, transformation, sentiment analysis, and real-time alerts for actionable insights.

## 📊 Architecture Overview

![Bing News Data Pipeline](./BingAPI.webp)

### Pipeline Layers:

1. **Bronze Layer – Raw Ingestion**  
   - News data is ingested from Bing News Search API using **Data Factory**.
   - Data is copied to Microsoft Fabric in **JSON format**.
   - Stored in **Lakehouse (Bronze Layer)** as raw data.

2. **Silver Layer – Transformation & Cleansing**  
   - Raw JSON is cleaned, structured, and transformed.
   - Processed data is stored in **Silver Lakehouse Table** for analytics use.

3. **Gold Layer – Sentiment Analysis**  
   - Enriched data is passed through a sentiment analysis model.
   - Results are saved in the **Gold Lakehouse Table**.

4. **Visualization & Alerts**  
   - A **Power BI dashboard** displays the latest insights.
   - **Data Activator** monitors sentiment patterns and triggers alerts (e.g., via Microsoft Teams).

5. **Orchestration**  
   - The entire workflow is managed through an **orchestration pipeline** in Microsoft Fabric for automation and scheduling.

---

## 🚀 Key Technologies

- **Bing News Search API** – News source
- **Microsoft Fabric** – Data platform
- **Data Factory** – Orchestration and ingestion
- **Lakehouse (Bronze, Silver, Gold)** – Storage and processing
- **Power BI** – Data visualization
- **Data Activator** – Real-time alerting
- **Microsoft Teams** – Notifications

---

## 📁 Folder Structure (Suggested)

```
bing-news-ingestion/
│
├── ingestion/                  # Data ingestion pipeline scripts
├── transformation/            # Data cleaning and transformation
├── sentiment_analysis/        # NLP scripts for sentiment scoring
├── dashboards/                # Power BI dashboard files
├── orchestration/             # Fabric orchestration definitions
├── config/                    # API keys and config files (excluded from version control)
├── assets/                    # Images like architecture diagram
│   └── BingAPI.webp
└── README.md
```

---

## ✅ Prerequisites

- Bing News Search API key
- Access to Microsoft Fabric and Lakehouse workspace
- Power BI Service
- Permissions to use Data Factory and Data Activator

---

## ⚙️ How to Use

1. **Connect to Bing API** in Data Factory using the API key.
2. **Copy data to Fabric workspace** in JSON format.
3. **Store raw JSON** in the Bronze Lakehouse.
4. **Transform & clean data** into the Silver layer.
5. **Run sentiment analysis** and store results in the Gold layer.
6. **Visualize insights** using Power BI.
7. **Enable alerts** in Data Activator to receive notifications in Teams.

---

## 📌 Outcome

An end-to-end automated pipeline that keeps your organization informed of the latest news trends with real-time sentiment insights and proactive alerts.

---

## 📬 Contact

For queries or contributions, feel free to reach out to the project maintainer.
