# 🌤️ Weather Forecast Analysis — Power BI Dashboard

A dynamic Power BI report that fetches live weather data via the **WeatherAPI** and visualizes current conditions, forecasts, air quality, and more — all in a single interactive page.

---

## 📌 Overview

This dashboard provides real-time and forecasted weather intelligence for any location. It connects directly to the WeatherAPI to pull current conditions and multi-day forecast data, then presents it through a clean, icon-rich Power BI interface.

---

## 🗂️ Project Structure

```
Weather_Forecast_Analysis.pbix   # Main Power BI report file
README.md
```

---

## 📊 Dashboard Features

| Visual | Description |
|---|---|
| **Location Slicer** | Filter by city/location name |
| **Day Slicer** | Select forecast day |
| **Current Temperature (°C)** | Live temperature card |
| **Wind Speed** | Current wind speed |
| **Humidity (%)** | Current humidity level |
| **Precipitation (in)** | Current precipitation amount |
| **Visibility** | Current visibility range |
| **Weather Condition Icon** | Live weather condition image |
| **Avg Temp Trend (Line Chart)** | Average temperature by forecast day |
| **Chance of Rain (Stacked Bar)** | Rain probability across forecast days |
| **Air Quality — CO (Card + Donut)** | Carbon monoxide level with AQI breakdown |

---

## 🌐 Data Source — WeatherAPI

This report uses the **[WeatherAPI](https://www.weatherapi.com/)** REST API.

### Tables / Endpoints Used

| Power BI Table | API Data |
|---|---|
| `Current Data` | `/current.json` — real-time conditions (temp, humidity, wind, rain, air quality) |
| `Forcast_Day Data` | `/forecast.json` — multi-day forecast (avg temp, day name, rain chance) |
| `Locations` | Location metadata |
| `_Measures` | Calculated DAX measures (AQI, Wind Speed, Visibility, Temp) |

### Key Fields

- `current.humidity`, `current.precip_in`, `current.chance_of_rain`
- `current.condition.icon`
- `current.air_quality.co`
- `forecast.forecastday.day.avgtemp_c`

---

## 🔑 API Key Setup

1. Sign up for a free API key at [https://www.weatherapi.com/](https://www.weatherapi.com/)
2. Open the `.pbix` file in **Power BI Desktop**
3. Go to **Home → Transform Data → Data Source Settings**
4. Update the API key parameter in the query editor (look for a parameter or web URL query)
5. Click **Close & Apply**

---

## 🚀 Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (latest version recommended)
- A valid WeatherAPI key (free tier works)
- Internet connection for live data refresh

### Steps

```
1. Clone or download this repository
2. Open Weather_Forecast_Analysis.pbix in Power BI Desktop
3. Update the API key (see above)
4. Click Refresh to load live data
5. Use the Location and Day slicers to explore
```

---

## 🔄 Data Refresh

- **Manual refresh**: Click **Refresh** in Power BI Desktop
- **Scheduled refresh** (Power BI Service): Publish to the Power BI Service and configure a scheduled refresh under dataset settings. Requires a gateway if using a personal API key in the query URL.

---

## 📦 DAX Measures

Custom measures are stored in the `_Measures` table:

| Measure | Description |
|---|---|
| `Current_Temp_C` | Current temperature in Celsius |
| `Wind_Speed` | Formatted wind speed |
| `Visibility_View` | Visibility display value |
| `AQI` | Air Quality Index derived from CO levels |

---

## 🛠️ Built With

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
- [WeatherAPI](https://www.weatherapi.com/)
- Power Query (M language) for API data ingestion
- DAX for custom measures and KPIs

---

## 📄 License

This project is for personal/educational use. Weather data is provided by WeatherAPI under their [terms of service](https://www.weatherapi.com/terms.aspx).

---

## 🙋 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

---

## 📬 Contact

Feel free to open an issue or reach out via GitHub if you have questions or suggestions.
