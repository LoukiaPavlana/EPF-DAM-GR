## 1_Regression_Model_using_only_historic_MCP_values__V2_One_week_forecast.ipynb
    In this notebook we create simple initial regression model for DAM MCP forecasting
    
    We utilize the dataframe previously created in a different notebook "Market clearing price Graph.ipynb "and saved in a csv file with these modifications:
    * Created a Date and Hour collumns,sorted the data according to their values
    * Created a collumn corresponding to the day of the week with 1:Sunday , 2:Monday etc.
    * Used the holiday library to create a collumn for whether its a holiday or a working day with 1 corresponding to a holiday and 0 to a working date
    
    (therefore we just read the already created files)
    
    
    * We beging by testing a simple gradient boosting Regressor on various time periods and predicting 7 days each time and we tested multiple feature sets.
    * We continue by creating and testing more regression models specifically **Random Forest** , **Linear Regression**,**Gradient boosting**, **XGBRegressor**, **LGBMRegressor**
    * We continue by testind to data scalers min-max and standard scaler and we conclude by performing a grid search for the best hyperparameters of each architecture.


## 2_Regression_Model_using_only_historic_MCP_Values_V3_One_day_forecast_single_step.ipynb
    In this notebooks we test multiple scaling approaches includind min-mas and standardn scaler adn we conduct a grid search to determine the best hyperparameter selectio for each model and we test more ferature sets

## 4_Regression_Model_MultiStep_WindowTesting_One_day_forecast.ipynb
    On the previous notebooks we tested our models with a single output (1 hour at a time )
    In a real world senario the model should forecast 24 values (one for each hour of the day) at a time.
    
    To implement that  we created a direct multistep output model by wrapping the base regressors (like Gradient Boosting or Random Forest) with scikit‑learn’s MultiOutputRegressor. The model is trained to output a vector of 24 predictions in one shot.


## 5_Regression_Model_ExogenousFeatures_and_WindowTesting.ipynb
    In this notebook we add exogenous same day features in the inputn sequences bu concatenating the two inout vectors.
    We continue by testing various different training sizes and we create grapghs and pies for the distribution of the best training size