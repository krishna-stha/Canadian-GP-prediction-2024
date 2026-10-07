# 🏎️ Canadian Grand Prix Prediction — OpenF1 API

Predict race results for the Canadian Grand Prix using real F1 telemetry and historical race data from the [OpenF1 API](https://openf1.org).

## 📦 Setup

```bash
pip install -r requirements.txt
jupyter notebook canadian_gp_prediction.ipynb
```

No API key needed — OpenF1 is completely free for historical data.

## 📊 What the Notebook Does

| Section | Description |
|---|---|
| API Fetcher | Pulls sessions, laps, stints, pit stops, weather, positions |
| Data Cleaning | Removes outlier laps (safety car, pit laps), normalizes times |
| Feature Engineering | Median/best pace, consistency, tire degradation, pit strategy |
| ML Model | Gradient Boosting Regressor predicts finishing order |
| Visualizations | 7 charts: lap times, race pace, tire strategy, weather, predictions |

## 🌐 OpenF1 Endpoints Used

| Endpoint | Data |
|---|---|
| `/meetings` | Race weekend metadata |
| `/sessions` | Qualifying + race session keys |
| `/laps` | Lap-by-lap timing for every driver |
| `/stints` | Tire compound + stint lengths |
| `/pit` | Pit stop timing |
| `/weather` | Air/track temp, humidity, wind |
| `/position` | Track position per lap |
| `/drivers` | Driver names, team, team colors |

## 🔮 Live Race Week

During the Canadian GP weekend, uncomment Section 16 to fetch **live qualifying laps** and refine the grid-based prediction in real time.

## ⚠️ Disclaimer

Predictions are based on historical pace data. Race incidents, weather changes, and strategy calls can significantly alter results.
