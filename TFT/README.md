## 1_TFT_Model_Single_Step.ipynb

    In this notebook we create the inital TFT model with a single step output, and run a thorough feature engineering analysis.


## 2_TFT_multistep_test_all_feature_Sets.ipynb
    In this notebook we test a direct multistep output approach for the nodel.
    * we test approximately 60 feature sets
    * We test various scaling methods:
      1. For categorical feature encoding:
            1. Embedded categorical encoder of the model (input these features on time_varying_known_categoricals)
            2. One hot encoding 
        2. For the scaling of the target (MCP)
            1. Standard Scaler
            2. Embedded tft scaler 
        
        3. For feature scaling:
            1. Standard scaler
            2. MinMax Scaler
            3. No scaler
    * We run mulitple hyperparameter combination tests
    * We test the performance of the model with different training sizes and look back windows on different periods
    And finally we conlude to the best TFT architecture


## 3_TFT.ipynb

In this notebook we run a final training sizes x look-back window analysis for all the months of 2024