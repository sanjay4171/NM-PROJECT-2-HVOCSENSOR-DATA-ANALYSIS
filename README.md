

# HVAC Sensor Data Analysis

**Sanjay Raj J**
**2nd Year | Mechanical Engineering**
**ARM College of Engineering & Technology**
**Course: Data Analysis in Mechanical Engineering**

---

## Introduction

This project focuses on analyzing real-world sensor data from HVAC (Heating, Ventilation, and Air Conditioning) systems. The main goal is to explore how different factors like temperature, humidity, air flow, and CO₂ levels relate to energy usage and indoor environment quality. As someone interested in both mechanical systems and data analysis, I found this project helpful in understanding how data can be used to improve energy efficiency in buildings.

---

## Why This Project?

Through this project, I wanted to:

* Discover trends and patterns in how HVAC systems operate.
* Identify situations where energy consumption might be higher than normal.
* Gain insights that could help improve system performance or maintenance planning.
* Explore the connection between environmental conditions and occupancy levels.

---

## Overview of the Dataset

The dataset contains time-based measurements from an HVAC setup. Each row records sensor values collected at a specific time. Below is a summary of the features included:

| Feature                   | Meaning                                               |
| ------------------------- | ----------------------------------------------------- |
| Date\_Logged              | Date and time when the reading was recorded           |
| Temperature (C)           | Room temperature in Celsius                           |
| Humidity (%)              | Relative humidity indoors                             |
| Air\_Flow (CFM)           | Air flow rate (cubic feet per minute)                 |
| CO2\_Level (ppm)          | CO₂ level inside the room (parts per million)         |
| Occupancy                 | Number of people present at the time                  |
| Energy\_Consumption (kWh) | Power consumed by the HVAC system (in kilowatt-hours) |

---

## Steps Taken in Data Preprocessing

To prepare the data for analysis, I followed these basic steps:

1. **Loading the Data**
   Used `pandas` to read the dataset and get an initial understanding of column types and data structure.

2. **Datetime Formatting**
   Converted the `Date_Logged` column to datetime format so I could do time-based grouping and analysis.

3. **Handling Missing Values**
   Filled in missing values in columns like `Air_Flow` and `CO2_Level` using the column mean, to avoid dropping useful data.

4. **Feature Extraction**
   Created two new columns from the timestamp:

   * `Hour` – to analyze hourly patterns.
   * `DayOfWeek` – to study differences between weekdays and weekends.

---

## Exploratory Data Analysis (EDA)

### Key Observations from the Data:

* **Energy Use Follows a Daily Cycle**
  Power consumption tends to be higher during regular working hours.

* **CO₂ Levels Rise with Occupancy**
  As expected, more people in the room means more CO₂ in the air.

* **Air Flow Adjusts with Room Usage**
  Air flow increases when occupancy goes up, which may suggest the system responds dynamically.

* **Correlation Between Features**

  * Energy use is moderately influenced by temperature and air flow.
  * CO₂ level is strongly linked to the number of people present.

### Visualizations Created:

* Time series plots to show hourly and daily trends.
* Histograms and boxplots to check distributions and spot outliers.
* Heatmaps to visualize feature correlations.

---

## Key Takeaways

* HVAC systems react to occupancy levels by adjusting airflow, which helps maintain indoor air quality.
* Energy use is predictable based on time and room activity, making it possible to plan for efficiency.
* CO₂ data can act as an indirect measure of occupancy in spaces where people movement is hard to track directly.

---

## What Can Be Done Next?

This project opens the door to some interesting future work:

* Apply outlier detection (e.g., IQR method) to remove suspicious data points.
* Build a basic predictive model to estimate energy use based on room conditions and occupancy.
* Detect unusual behavior in the HVAC system using anomaly detection techniques.

---

## Tools and Technologies Used

* **Python (Pandas, NumPy)** – for cleaning and preparing the data
* **Plotly & Matplotlib** – for making visualizations
* **Jupyter Notebook** – for writing and presenting the analysis step-by-step
