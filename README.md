
# Road Accidents Dashboard

## Problem Statement

This Power BI Dashboard provides a comprehensive analysis of **road accidents** to help authorities and policymakers identify the major factors contributing to accidents, assess casualty severity, and evaluate patterns across **vehicle types, road types, areas, and light/weather conditions**.

By identifying these insights, the dashboard assists in formulating **data-driven strategies** to reduce accidents and improve **road safety measures**.


## Steps Followed

* **Step 1:** Imported the **Road Accident Dataset (CSV format)** into Power BI Desktop.
* **Step 2:** Opened **Power Query Editor**, and under the *View* tab, enabled **Column Distribution**, **Column Quality**, and **Column Profile** options.
* **Step 3:** Changed column profiling to **entire dataset** to view complete data statistics.
* **Step 4:** Checked for missing or erroneous data values — minimal nulls were found and appropriately handled.
* **Step 5:** Cleaned and transformed necessary columns (e.g., Year, Area, Weather Conditions, Vehicle Type) for proper data modeling.
* **Step 6:** Applied a **Dark Theme** for professional visualization consistency.
* **Step 7:** Created various **visualizations** to represent key metrics and relationships.
* **Step 8:** Added **slicers** for interactive filtering by:

  * *Weather Conditions*
  * *Road Surface Conditions*
* **Step 9:** Added **Card visuals** to represent:

  * Total CY Accidents
  * Total CY Casualties
  * Fatal, Serious, and Slight Casualties
  * Year-over-Year (YoY) % Change for each category
* **Step 10:** Added charts to visualize accident distribution:

  * **Bar Chart** – Casualties by Vehicle Type
  * **Pie Charts** – Casualties by Area (Urban vs Rural), Casualties by Light Condition
  * **Bar Chart** – Casualties by Road Type
  * **Line Chart** – CY vs PY Casualties by Month and Year
  * **Map Visual** – Casualties by Location
* **Step 11:** Created calculated **DAX measures** to support KPI visualizations.


## DAX Measures Used

**1. Total Accidents:**

```DAX
Total CY Accidents = SUM(Road_Accident_Data[Accidents_Current_Year])
```

**2. Total Casualties:**

```DAX
Total CY Casualties = SUM(Road_Accident_Data[Casualties_Current_Year])
```

**3. Fatal Casualties:**

```DAX
Fatal Casualties = SUM(Road_Accident_Data[Fatal_Casualties])
```

**4. YoY % Change (example):**

```DAX
YoY % Change = DIVIDE([CY Value] - [PY Value], [PY Value]) * 100
```

*(Additional measures were created for Serious and Slight Casualties, each showing year-over-year percentage change.)*



## Visualizations Overview

| Visualization Type | Description                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------ |
| **Cards**          | Total CY Accidents, Total CY Casualties, Fatal/Serious/Slight Casualties with YoY % Change |
| **Bar Chart**      | Casualties by Vehicle Type                                                                 |
| **Line Chart**     | CY vs PY Casualties by Month and Year                                                      |
| **Pie Charts**     | Casualties by Area (Urban vs Rural) and by Light Condition (Daylight vs Darkness)          |
| **Bar Chart**      | Casualties by Road Type                                                                    |
| **Map Visual**     | Casualties by Location                                                                     |
| **Slicers**        | Weather Conditions and Road Surface Conditions                                             |



## Snapshots

### Dashboard Overview 
<img width="788" height="440" alt="Screenshot 2025-11-01 at 4 38 00 PM" src="https://github.com/user-attachments/assets/3a08b5e4-2daf-4d81-afa3-d99a04c79e09" />


### Weather & Road Surface Filters

<img width="302" height="287" alt="Screenshot 2025-11-01 at 5 07 05 PM" src="https://github.com/user-attachments/assets/5e569fab-de17-44d6-b713-2414a6c48e2e" />
<img width="302" height="287" alt="Screenshot 2025-11-01 at 5 08 17 PM" src="https://github.com/user-attachments/assets/f8d8db17-6c42-4a68-ba04-c839525974df" />

## Insights

A single-page interactive dashboard was created in Power BI Desktop and published to Power BI Service.

### [1] Total Figures

* **Total CY Accidents:** 144.4K
* **Total CY Casualties:** 195.7K
* **Fatal Casualties:** 2.9K
* **Serious Casualties:** 29.9K
* **Slight Casualties:** 195.7K

All categories show a **YoY decrease**, with fatal casualties reducing by **33.3%** and serious casualties by **18.2%**.



### [2] Casualties by Vehicle Type

* **Cars:** 449,182 (highest)
* **Motorcycles:** 45,726
* **Trucks:** 45,144
* **Buses:** 17,267
* **Agricultural Vehicles:** 1,352
* **Others:** 4,631

→ **Cars and Motorcycles** account for the majority of road casualties.



### [3] Casualties by Area

* **Urban Areas:** 61.23%
* **Rural Areas:** 38.77%
  → Urban zones experience more accidents, likely due to higher vehicle density.



### [4] Casualties by Light Condition

* **Daylight:** 72.98%
* **Darkness:** 27.02%
  → Most accidents occur during daylight hours, indicating heavy daytime traffic as a factor.



### [5] Casualties by Road Type

* **Single Carriageway:** Highest casualties
* **Dual Carriageway and Roundabouts:** Fewer casualties comparatively.



### [6] Monthly Trends (CY vs PY)

* Casualties fluctuate across months, with noticeable spikes in **June–October**, indicating peak road activity.
* Overall downward trend in 2022 compared to 2021.



### [7] Filters and Interactivity

Users can dynamically filter data by:

* **Weather Conditions** (Fine, Rainy, Snow/Fog, Others)
* **Road Surface Conditions** (Dry, Wet/Damp, Frost/Ice, Flood, Snow)

This allows deeper exploration into how environmental factors affect road safety.







