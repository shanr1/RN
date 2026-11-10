# 📊 MBTA Green Line B Branch: Weather & Event Disruptions Analysis

> **BA780 Data Analytics Project (Team A08)**  
> **Contributors:** Susan Huang, Ingrid Felix, Ruining Shan, Tia Theseira, Kaiser Lu

---

## 📖 Project Overview
This project investigates how adverse weather conditions, public events, and seasonal passenger volume impact the travel times and schedule reliability of the **MBTA Green Line B Branch** in Boston. 

By analyzing a merged dataset of over **539,000 transit records** from September and December 2025, alongside NOAA weather logs and City of Boston special event permits, we identify key bottlenecks and quantify delay patterns across above-ground and underground segments.

---

## ⚙️ Main Notebook
The full analysis, data cleaning pipeline, and visualizations can be found in the Jupyter Notebook:
🔗 **[`A08-Green-Line-B-Weather-and-Event-Disruptions.ipynb`](./A08-Green-Line-B-Weather-and-Event-Disruptions.ipynb)**

---

## 🔑 Key Findings

1. **Above-Ground vs. Underground Predictability:**
   - **Above-ground segments** (Boston College to Kenmore) are the primary source of schedule unpredictability, showing nearly **triple the variance** of underground segments (Standard Deviation: **192.9s** above-ground vs. **66.7s** underground) even on normal days.
2. **Peak vs. Off-Peak Dynamics:**
   - Rush hours add ~1.5 minutes to the median end-to-end trip time, but surprisingly result in a **tighter standard deviation (5.6 min)** compared to off-peak hours (**6.6 min**), making peak travel more consistent.
3. **Seasonal Baselines:**
   - Baseline travel is significantly slower during the **September** back-to-school rush (median **47.8 min** end-to-end) compared to **December** (median **43.1 min**).
4. **Combined Disruptions (Weather + Events):**
   - While precipitation alone has minimal impact on travel time, the **combination of rain and public events** creates a compound effect, increasing total delay more than either factor individually.

---

## 💡 Recommendations

* **For MBTA:**
  * **Transit Signal Priority (TSP):** Implement signal priority on Commonwealth Avenue to reduce above-ground traffic light delays.
  * **September Fleet Management:** Increase train frequency and capacity during the fall university move-in period.
  * **Dynamic Scheduling:** Utilize weather forecasts and event databases to proactively deploy extra trains on high-risk days.
* **For Commuters & BU Students:**
  * **Off-Peak Padding:** Allow extra travel time during off-peak hours due to higher trip variance.
  * **Fall Expectation:** Budget an extra 5–10 minutes for commutes during September compared to winter months.

---

## 🛠️ Datasets Used
* **MBTA Light Rail Travel Times (Sep & Dec 2025):** Filtered for `Green-B` route travel durations.
* **NOAA Local Climatological Data (LCD):** Hourly temperature, precipitation, and wind speeds.
* **City of Boston Special Event Permits:** Permitted special events, dates, and locations.
