This folder contains 5 notebooks with the entire analysis and creation of the LSTM models for the Greek MCP DAM forecast

## **1_LSTM_Model_using_only_historic_Market_Price_Values_AddedFeatures_&_Recursive_Vs_Multistep.ipynb :**


```
In this notebook we started by testing models with single step output (1 hour at a time) we
1. tested a vanilla LSTM progressed to 
2. Stacked LSTM with different layers and differnet hyperparameters (Models M2 through M12)
3. Tested two encodings for the categorical features 
    1. One hot encoding (best)
    2. Cyclic encoding
4. Tested two different approaches for a multistep forecasting (we tested on the same period so the metrics are comparable)
    1. Autoregressive
    2. Direct Multi-Step (best as can be seen from the following dataframes)
5. After determining the best best architecture we tested more featute sets

In the above analysis the models take as input only historic features and data. 
To further improve the model in the next notebook we will test two differnt methods to incorporate same-day exogenous data to the model.
```


## **2_New_LSTM_Exogenous_Features.ipynb :**

```
In this notebook we tested two different approaches for incorporating same day exogenous data (like forecasted demand etc) to the model to further improve the metrics.
And also created a thorough hyperparameter search utilizing the keras_tuner library.
The two approaches were:
1. Two sequences processed independently and then concatenated into one to create the input of the LSTM model
2. Encoder-Decoder architecture
The ladder proved to have slightly better results and therefore we keep that approach for the next steps of our analysis.
In the next notebook we will examine the impact of the input_sequence length as well as the training size and period of the model.
```

## **3_LSTM_Testing_Input_Windows_and_Training_Sizes.ipynb :**
```
In this notebook we created the inital tests for window size lentghs and various training horizon lenghts
```


## **4_LSTM_More_Feature_Engineering.ipynb :**
```
In this notebook we test even more feature sets and then we proceed to test different traing size lentghs and input window lengths on different periods.
we conclude the best configuration of traing size lentghs X input window lengths per month.
```



## **8_LSTM.ipynb :**
```
In this notebook, we iteratively test all feature sets once more, with 5 iterations each to eliminate the stochastic bias.
We proceed with creating and testing 12 different training size X input window length configurations, for each day of the 2024, we run 4.380 models to determine the relationship of daily volatily with these hyperparameters.
```