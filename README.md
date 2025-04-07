# 🔄 End-to-End ETL Pipeline on Google Cloud Platform

This project shows how to build a complete ETL pipeline using Google Cloud Platform (GCP). It uses Airflow (Cloud Composer) to schedule and manage data tasks, loads data into BigQuery, and visualizes the results in a Looker dashboard.

---

## 📌 Key Features

- Extracts data from a MySQL database and a public currency exchange API
- Transforms the data using Python and Pandas
- Uploads the result as CSV to Google Cloud Storage (GCS)
- Loads the final data into Google BigQuery
- Managed and scheduled using Apache Airflow (Cloud Composer)
- Displays business insights on a Looker dashboard


---

## 🛠️ Tools & Services

| Purpose           | Tool / Service              |
|-------------------|-----------------------------|
| Workflow Orchestration | Apache Airflow (Cloud Composer) |
| Database          | MySQL                       |
| Data Transformation | Python, Pandas             |
| Cloud Storage     | Google Cloud Storage (GCS)  |
| Data Warehouse    | Google BigQuery             |
| Dashboard         | Looker                      |
| API Integration   | Currency Exchange API       |

---

## 🔁 ETL Pipeline Flow

```mermaid
graph TD
    A[MySQL: Raw Tables] --> B[Airflow: Extract Task]
    B --> C[Airflow: API Task (USD to THB)]
    C --> D[Airflow: Transform with Pandas]
    D --> E[Upload CSV to GCS]
    E --> F[Load to BigQuery]
    F --> G[Visualize in Looker Dashboard]
