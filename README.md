## Contextualized LSTM-DNN Model for County-Level Corn Yield Prediction from Weather and Soil Data

Crop yield prediction is critical for agricultural insurance, better risk management, and efficient production strategies. In this study, we propose a novel machine-learning framework to predict county-level corn yield using daily weather data, weather-derived features based on zigzag topology persistence, and static soil information.

## Approach

Our approach integrates a **Long Short-Term Memory (LSTM)** network to capture sequential weather patterns and a shallow feed-forward network for yearly weather topology persistence. The two network outputs are concatenated with soil data and fed into a deep feed-forward network optimized to predict the corn yield at a county level for each year.

## Model and Data

The model was trained on datasets of **1391 county-year pairs** and tested on **50 pairs**. Performance was compared to the following models:
- Convolutional Graph Neural Network (CGNN)
- Transformer
- Support Vector Regression (SVR) with Radial Basis Function (SVR-RBF)
- Extreme Gradient Boosting (XGBoost)
- Combined Vector Autoregression-SVR (VAR-SVR)

## Results

Among the models, the proposed **LSTM-DNN** and **CGNN** models excelled. The goodness of fit **$(R^2)$**, root mean square error (RMSE, **Mg/ha**), mean absolute error (MAE, **Mg/ha**), and mean absolute percentage error (MAPE, **%**) were as follows:

- **LSTM-DNN Model**:
  - **$R^2$**: 0.79
  - **RMSE**: 21.2 Mg/ha
  - **MAE**: 15.5 Mg/ha
  - **MAPE**: 5.49%

- **CGNN Model** (Nearest Competitor):
  - **$R^2$**: 0.65
  - **RMSE**: 22.2 Mg/ha
  - **MAE**: 17.4 Mg/ha
  - **MAPE**: 7.09%

The **LSTM-DNN model**'s accuracy and computational simplicity were slightly better than the **CGNN model**. The **LSTM-DNN model** explained around **79%** of the county average yield variability from weather and soil data. The **MAPE of 5.49%** from observed yields reflects a reliable tool for estimating the yield.

## Future Work

Future studies could fine-tune the model with more accurate and high-resolution data instead of county-level records.
