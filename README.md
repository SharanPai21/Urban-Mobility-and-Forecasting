# 🚕 Urban Mobility Analytics & Demand Forecasting

This project analyzes urban taxi ride patterns in New York City by combining geospatial, temporal, weather, and holiday data to forecast hourly demand at the zone level. The ultimate goal is to help improve operational efficiency through data-driven insights on dynamic pricing, fleet rebalancing, and service planning.

---

## 📁 Directory Structure

```

├── raw\_data/           # Raw datasets
│   ├── taxi_df.csv
│   ├── weather_df.csv
│   ├── holiday_df.csv
│   └── taxi_zone.geojson
│
├── cleaned_data/       # Processed dataset for modeling and visualization
│   └── final_trip_data.csv
│
├── notebook/           # Jupyter Notebooks with EDA, feature engineering, and modeling
│   └── urban_mobility_analysis.ipynb
│
├── heatmap/            # Interactive and static demand heatmaps
│   └── demand_heatmap.html
│
└── README.md           # Project documentation

```

---

## 📊 Project Goals

- Analyze spatial and temporal demand patterns
- Forecast hourly taxi demand at the zone level
- Understand the influence of weather and holidays
- Recommend fleet optimization and pricing strategies

---

## 🧠 Key Features

- 📍 **Zone-Level Demand Forecasting** using XGBoost
- 🌦️ **Weather-Aware Modeling** incorporating temperature, visibility, wind, etc.
- 🗓️ **Holiday & Weekday Impact Analysis**
- 🗺️ **Heatmap Visualization** of demand surges
- 📈 **Temporal Aggregation** to hourly level for operational insights

---

## 🔍 Cool Insights I Found

- 🌧️ **Rain = Rides:** Rainy days see **11% more rides** — people skip walking and grab a cab instead!
- 🏙️ **Manhattan Rules:** Manhattan alone accounts for **2.6M trips**, far more than any other borough.
- 🎉 **Holiday Dip:** Surprisingly, holidays see **fewer rides** (**0.39%** of trips vs **0.61%** on normal days).
- 🌦️ **Weather Matters:** Weather significantly impacts demand — people **really hate getting wet** and tend to avoid walking when conditions are poor.

---

## 📚 Final Dataset Columns

| Column Name     | Description |
|-----------------|-------------|
| `pickup_hour`   | Hour of the trip (YYYY-MM-DD HH:00) |
| `pickup_date`   | Date of the trip (YYYY-MM-DD) |
| `PULocationID`  | Numeric identifier for pickup zone |
| `zone`          | Name of the pickup zone |
| `borough`       | NYC borough where the pickup occurred |
| `num_trips`     | Number of trips in the zone during the hour |
| `temp`          | Temperature (°C) at the pickup hour |
| `humidity`      | Humidity (%) |
| `precip`        | Precipitation (mm or binary event) |
| `windgust`      | Maximum wind gust (km/h) |
| `windspeed`     | Average wind speed (km/h) |
| `visibility`    | Visibility (km) |
| `conditions`    | Weather conditions (e.g., Clear, Rain, Snow) |
| `is_holiday`    | Binary flag: 1 if date is a holiday |
| `weekday`       | Day of the week (e.g., Monday, Tuesday) |
| `is_weekend`    | Binary flag: 1 for Saturday/Sunday |

---

## 🛠️ Technologies Used

- **Python:** Pandas, GeoPandas, Scikit-learn, XGBoost
- **Visualization:** Folium, Plotly, Power BI
- **Geospatial:** PostGIS (optional), GeoJSON
- **Data Sources:** NYC Taxi Data, NOAA Weather, Public Holidays

---

## 🗺️ Heatmaps

Interactive demand heatmaps help visualize:
- Top demand hotspots by hour
- Weather-affected regions
- Holiday traffic surges

Available under `/heatmap/`.

---

## 🚀 Business Use Cases

- 🔄 **Fleet Redistribution:** Reallocate taxis in real-time based on predicted demand
- 📉 **Wait Time Reduction:** Deploy more vehicles in high-demand zones
- 💸 **Incentive Optimization:** Recommend bonuses for drivers in under-served areas
- 🎯 **Smart Pricing:** Adjust fares based on weather, holidays, and demand
