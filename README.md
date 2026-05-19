# Household-Power-Consumption-Forecasting

Summary and Project Findings
1. Methodology

This project implements a machine learning pipeline to forecast household power consumption using the following workflow:

Data Preparation: The dataset was cleaned by imputing missing values with the column mean. Temporal features were extracted from the timestamp to capture cyclical patterns, including Hour, Day, and Month.

Feature Selection: The model utilizes temporal inputs (Hour, Day, Month) to predict Global_active_power.

Modeling: A RandomForestRegressor was chosen for its effectiveness in capturing non-linear relationships in complex data.

Evaluation: The model was evaluated using Mean Absolute Error (MAE) and the R-squared (R²) score to determine predictive accuracy.

2. Results

The model currently achieves an R² score of approximately 0.37.

Interpretation: An R² of 0.37 suggests that the current temporal features explain about 37% of the variance in power consumption. While this serves as a solid baseline, it indicates that power usage is highly influenced by factors beyond just time (such as historical lag, temperature, or appliance-specific usage patterns).

3. Future Improvements

To enhance the predictive power of this model, future work could include:

Lag Features: Incorporating previous power consumption readings (Global_active_power at time t-1) as inputs.

Cyclical Encoding: Transforming time features into sine and cosine components to better represent the circular nature of time.

Chronological Splitting: Transitioning from random train-test splitting to a chronological split to prevent data leakage and better simulate real-world forecasting.
