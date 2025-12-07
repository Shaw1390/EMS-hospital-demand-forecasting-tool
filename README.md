# Toronto Climate, Air Quality & EMS Dashboard

## Overview
This project explores how environmental conditions, air pollution, and digital health signals affect daily EMS call volumes in Toronto. Multiple datasets were combined, including climate and weather data, air quality measurements, Google Trends health-related searches, and EMS call records.

We performed exploratory data analysis, created lag and rolling average features, and trained a Random Forest model to predict EMS calls. All results are presented in an interactive Streamlit dashboard. 

## Data Sources
- **Climate Data:** Daily weather stats from Environment Canada  
- **Air Quality Data:** Open-source AQI data for Toronto  
- **Google Trends:** Health-related search terms for Toronto  
- **EMS Calls:** Publicly available emergency services dataset  

## Methodology
1. Load and clean all datasets.  
2. Merge climate, pollution, EMS, and Google Trends data by date.  
3. Engineer lag and moving average features to capture temporal effects.  
4. Perform exploratory data analysis (EDA) to visualize trends and correlations.  
5. Train a Random Forest regression model to predict EMS calls.  
6. Evaluate the model using RMSE, R², and feature importance.  
7. Build a Streamlit dashboard for interactive visualization.  

## Dashboard Features
- Interactive time series of EMS calls, air pollution, and temperature trends  
- Correlation heatmap between numeric variables  
- Feature importance chart from the Random Forest model  
- Actual vs predicted EMS calls  
- Filters by date range and search trends  
![Dashboard GIF](/Assets/streamlit-streamlit_app-2025-12-07-00-43-21-ezgif.com-video-to-gif.gif)
## Key Insights
- PM2.5 and NO₂ are strong predictors of EMS call volumes.  
- Google Trends searches for “breathing problems” and “ambulance” provide digital indicators.  
- Multi-day averages of temperature and pollution are more predictive than single-day values.  

## Requirements
- Python 3.9+  
- Libraries: pandas, numpy, matplotlib, seaborn, plotly, pytrends, scikit-learn, streamlit  

Install dependencies with:

```bash
pip install pandas numpy matplotlib seaborn plotly pytrends scikit-learn streamlit
```

## How to Run 
Run the dashboard using:

```bash
streamlit run app.py
```

Then open http://localhost:8501 in a web browser to interact with the dashboard. 

## License

This project uses publicly available datasets and is released under the MIT License.
