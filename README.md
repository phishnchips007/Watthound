## Watthound ⚡

Watthound is a lightweight anomaly detection tool designed for analyzing smart meter data. The project simulates a utility monitoring environment with a cybersecurity lens—allowing users to identify irregular consumption patterns or potential tampering.

## 🛠️ Tech Stack

- **Google Sheets** – for manual IoT data insertion and transformation  
- **Google Query** – used SQL-like syntax for filtering, logic, and calculations  
- **Looker Studio** – to visualize metrics and build a responsive dashboard  

## 💡 Problem It Solves

Energy utilities and cybersecurity teams often need quick visibility into smart device behavior. Watthound solves this by enabling non-engineers to monitor IoT consumption, detect anomalies, and understand usage trends—without backend infrastructure or expensive software.

## 📊 Sample Metric

```sql
SELECT 
  Meter_ID, 
  AVG(Daily_Usage) 
WHERE 
  Region = 'Zone A' 
GROUP BY 
  Meter_ID 
HAVING 
  AVG(Daily_Usage) > 2 * (SELECT AVG(Daily_Usage) FROM Sheet1)

## 📸 Dashboard Preview

Below is a snapshot of the Looker Studio dashboard used in this project, visualizing anomalies in smart meter energy data by region and device type.
<img width="1280" height="719" alt="Screenshot 2025-08-14 at 2 48 06 AM" src="https://github.com/user-attachments/assets/0a3ad3f4-60cd-49e2-9fe0-b304e074d33a" />
<img width="1280" height="832" alt="Screenshot 2025-08-14 at 2 47 53 AM" src="https://github.com/user-attachments/assets/459ad47b-f536-467e-811b-aa892c8f8da4" />
