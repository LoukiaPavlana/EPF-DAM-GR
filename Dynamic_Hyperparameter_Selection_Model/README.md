**META-MODEL-v2.ipynb**

    In this notebook we conduct and expolartory data analysis for the correlation of daily realised volatility with the best hyperparameter selection (training_size X look-back window) we create box plots, bar charts as well as pearson correlation heatmaps.
    We proceed to create multiple statistic features for each day.
    After we determine the relation of these instances we create and train to different classes of models with the aim of forecasting the best hyperprameter combination for each day.
    The models are trained on the dataset created in LSTM/8_LSTM.ipynb were we run 12 models for each day of 2024 to determine the best configuration for each one.
    We proceed with training a linear regression model that forecasts the expected MAE of each of the hyperprameter combinations and selects the one with the lowest MAE and a classifier that determines which combination (class) fits each day best.


**Distributions_from_hyperparameter_tests.ipynb**
    In this notebook we create pie charts from the results of the various (training_size X Look back window) tests we run for each of the model to determine thei distribution.