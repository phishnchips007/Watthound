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

## 📊 Interactive Dashboard

View the dashboard here: https://lookerstudio.google.com/s/n_D65kvAhY8

## 📊 Dashboard Preview

Here are the screenshots of the Looker Studio dashboard:

![Screenshot 1](https://github.com/phishnchips007/Watthound/raw/main/watt1.png)
![Screenshot 2](https://github.com/phishnchips007/Watthound/raw/main/watt2.png)
![Screenshot 3](https://github.com/phishnchips007/Watthound/raw/main/watt3.png)
