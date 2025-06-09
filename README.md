# 🚕 Urban Mobility Analytics & Demand Forecasting

This project analyzes urban taxi ride data in New York City to understand geospatial and temporal patterns, forecast demand, and provide data-driven recommendations for optimizing taxi fleet allocation. By combining ride data with weather and holiday information, we build an intelligent mobility analytics system that enables dynamic pricing, fleet rebalancing, and improved service efficiency.

---

## 📁 Directory Structure

```

├── raw\_data/           # Raw input datasets (trips, weather, holidays, geo zones)
│   ├── taxi\_df.csv
│   ├── weather\_df.csv
│   ├── holiday\_df.csv
│   └── taxi\_zone.geojson
│
├── cleaned\_data/       # Cleaned and preprocessed data used for modeling
│   └── final\_trip\_data.csv
│
├── notebook/           # Jupyter notebooks with full EDA, geospatial analysis, and modeling
│   └── urban\_mobility\_analysis.ipynb
│
├── heatmap/            # Static and interactive demand heatmaps
│   └── demand\_heatmap.html
│
└── README.md           # Project overview and documentation

```

---

## 📊 Project Goals

- Visualize spatial and temporal demand across NYC zones
- Forecast hourly trip demand per zone
- Analyze the impact of weather and holidays on mobility
- Provide operational insights: dynamic pricing, fleet rebalancing, driver incentives

---

## 🧠 Key Features

- 🔍 **Geospatial Analysis** using GeoPandas and Folium  
- 📈 **Time-Series Demand Forecasting** using XGBoost  
- 🌦️ **External Feature Enrichment** using weather and holiday data  
- 🗺️ **Interactive Heatmaps** to visualize high-demand zones  
- 📊 **Data-Driven Recommendations** for fleet operators

---

## 📚 Datasets Used

| Dataset Name       | Description                                      |
|--------------------|--------------------------------------------------|
| `taxi_df.csv`      | Raw trip-level taxi data with timestamps and zones |
| `weather_df.csv`   | Hourly/daily weather conditions                  |
| `holiday_df.csv`   | National and local holidays and major events     |
| `taxi_zone.geojson`| Zone metadata and geometries for mapping         |

---

## 🛠️ Tech Stack

- **Language:** Python (Pandas, GeoPandas, NumPy)
- **ML:** XGBoost, Scikit-learn
- **Visualization:** Folium, Plotly, Power BI
- **Geospatial:** GeoPandas, PostGIS (optional for scalability)
- **Dashboard (future):** Streamlit or Power BI

---

## 📌 Sample Output Columns

The final forecasting dataset contains:

- `pickup_hour`: Timestamp rounded to the hour
- `PULocationID`: Numeric zone identifier
- `zone`: Name of the pickup zone
- `borough`: NYC borough
- `num_trips`: Total number of trips in that zone-hour

---

## 🚀 Business Impact

This system allows:
- 📉 Reduced passenger wait times
- 📍 Optimized fleet distribution by hour and zone
- 💸 Informed dynamic pricing and driver incentive programs

---



