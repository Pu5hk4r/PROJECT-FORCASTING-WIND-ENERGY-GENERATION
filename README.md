# ⚡ Wind Turbine Renewable Energy Generation Forecasting Web App

A web-based machine learning application to forecast wind energy generation using time-series feature engineering and a pre-trained XGBoost regression model. Built with Flask and visualized through Matplotlib plots.

---

## 📊 Visualization
![visuals](https://github.com/Pu5hk4r/PROJECT-FORCASTING-WIND-ENERGY-GENERATION/blob/main/wind_energy_genration_prediction.png)
---
## 📚 Project Overview

Wind energy is a crucial source of renewable energy in today's sustainable world.  
This project predicts future energy generation from wind turbines based on **timestamp-driven features** like hour, day, and month — enabling better **energy planning and optimization**.  
Users can dynamically input a date range through a web interface and receive a **real-time prediction plot** for the specified period.

---

## 🚀 Features

- **Interactive Web App**: Users input a date range to forecast energy generation.
- **Machine Learning Model**: Pre-trained XGBoost Regressor (`model2.pkl`) for high-accuracy predictions.
- **Automatic Feature Engineering**: Generates time-based features from timestamps (hour, day, month, etc.).
- **Visualization**: Real-time prediction graphs created with Matplotlib and displayed via Flask.
- **Lightweight Backend**: Simple Flask server handles user requests, model inference, and visualization generation.

---

## 🛠️ Tech Stack

- **Backend:** Python, Flask
- **Machine Learning:** XGBoost, Pickle
- **Data Processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Frontend:** HTML (via Flask Jinja2 Templates)

---

## 🧩 Key Components

| Component | Description |
|:---------|:-------------|
| `model.py` | Loads pre-trained model, handles feature engineering, prepares future timestamps |
| `app.py` | Flask app managing routes, user inputs, prediction logic, and plot generation |
| `/templates/index.html` | Frontend web form for date input |
| `/static/output.png` | Saves generated prediction plot |

---

## 🛤️ How It Works

1. **User Input**:  
   - User selects a **From Date** and **To Date** via the web form.

2. **Feature Generation**:  
   - The app creates a date range with **10-minute intervals** between the two dates.
   - Features such as `hour`, `minute`, `day`, `month`, `year`, etc., are automatically generated.

3. **Prediction**:  
   - The feature set is fed into the pre-trained XGBoost model to predict **future energy output**.

4. **Visualization**:  
   - Predictions are plotted as a **time-series graph** and saved dynamically.

5. **Result Display**:  
   - The generated graph is displayed back to the user on the same page.

---

## 📈 Example Flow

```plaintext
User selects:
From Date: 2025-04-20
To Date: 2025-04-22

-> System generates 10-min interval timestamps
-> Features extracted from timestamps
-> Model predicts energy output at each interval
-> Graph created showing energy trends between April 20–22
-> Graph displayed on the web page

```

---
## 🧹 Future Enhancements (Ideas)
- Deploy on cloud platform (AWS/GCP) for wider access.
- Add user authentication to save prediction history.
- Improve model accuracy by integrating external weather features (wind speed, humidity, temperature).
- Make plots interactive with Plotly or Dash.








