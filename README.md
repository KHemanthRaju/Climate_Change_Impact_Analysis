### Climate Change Impact Analysis

#### Project Overview

I developed a **Climate Change Impact Analysis** project to investigate how global temperature changes correlate with the frequency and intensity of extreme weather events (e.g., heatwaves, floods). Using historical climate data, I wrangled temperature and weather event records, visualized trends, and built a predictive model to forecast future extreme event frequency based on temperature anomalies. This project highlights the real-world implications of climate change and provides actionable insights for preparedness.

#### Dataset

- **Source**: [Global Land Temperatures](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data) and [Natural Disaster Events](https://www.kaggle.com/datasets/noaa/noaa-global-historical-climatology-network) from Kaggle, supplemented with simplified data from Berkeley Earth and NOAA.
- **Download**: For simplicity, I’ve used a pre-processed subset from Berkeley Earth’s Global Temperatures dataset available on Kaggle:
    - **File**: GlobalTemperatures.csv
    - **Link**: [Download from Kaggle](https://www.kaggle.com/datasets/berkeleyearth/climate-change-earth-surface-temperature-data?select=GlobalLandTemperaturesByCountry.csv)
    - **Size**: ~128 MB, containing columns: dt (date), AverageTemperature, AverageTemperatureUncertainty, Country.
- **Additional Data**: I’ll simulate extreme weather event data (e.g., heatwaves) based on temperature thresholds for this example, as the full NOAA disaster dataset requires more preprocessing. You can expand this with real event data if desired.

#### Steps

1. **Data Wrangling**: Clean and aggregate temperature data, simulate extreme weather events.
2. **Visualization**: Plot temperature trends and extreme event frequency.
3. **Machine Learning**: Predict future extreme event frequency using a regression model.

### Explanation

1. **Data Wrangling**:
    - Loads the GlobalTemperatures.csv dataset from Kaggle.
    - Aggregates by date to get global average temperatures, calculates anomalies relative to a 1900-1950 baseline, and simulates heatwaves (anomaly > 1.5°C).
    - Groups data by year for analysis.
2. **Visualization**:
    - Line plot shows the temperature anomaly trend over time.
    - Bar plot displays annual heatwave frequency.
    - Scatter plot correlates anomaly with heatwave count, colored by year.
3. **Machine Learning**:
    - Trains a Linear Regression model to predict heatwave count from temperature anomaly.
    - Forecasts heatwave frequency for 2025-2035 assuming a 1°C rise.
    - Provides an R² score and coefficient for interpretation.

---

### Running the Code

1. **Requirements**:
    - Install libraries: pip install pandas numpy matplotlib seaborn scikit-learn.
    - No manual download needed—the code fetches the dataset from Kaggle’s hosted URL (assuming internet access).
2. **Execution**:
    - Run in a Python environment (e.g., Jupyter Notebook).
    - Outputs: Three visualizations, a forecast plot, R² score, and an impact insight.
