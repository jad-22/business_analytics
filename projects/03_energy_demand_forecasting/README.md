# 03. UK Daily Energy Demand Forecasting

### Data Source

Data was provided by Imperial College, but was based on real-life dataset.

### Objectives

In the energy market, being able to accurately predict the next day's energy demand is highly important to plan for a cost-efficient grid operation. 
This project was an assigment and also a competition to build a forecasting model that can accurately predict the next 2-day load demand.

### Methodology

![forecasting_process](https://github.com/jad-22/business_analytics/blob/main/projects/03_energy_demand_forecasting/03_forecasting_methodology.png)

The finalised model was based on several steps:
1. Data collection and preprocessing
   * Being aware that the effect of covid and increasing gas prices on electricity demand, we include covid stringency index and monthly gas prices as independent variables
   * Add computed features such as squared of temperature and fourier series terms
   * Add binary variables to account for seasonalities
2. Model fitting and selection
   * Build several models such as multi-variate linear regression (MLR), ARIMA, Holt-Winters (ETS), etc.
   * Selected models based on lowest root-mean-squared-errors (RMSE): MLR, MLR (Fourier), ARIMA-X, TBATS, STL-ETS
3. Model forecasting and weighting
   * Generate model forecast from the selected models
   * Calculate for the weighted-average of the forecasts, weighted on the inverse of the RMSE
4. Forecast adjustment
   * Multiply by an adjustment factor of approximately 0.91 to 0.95 to account reduce overprediction
