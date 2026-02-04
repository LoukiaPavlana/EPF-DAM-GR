### **EnexGroup_Data_Visualization_V1.ipynb**

    In this notebook we create an initial visualisation of the data provided by Enex Group https://www.enexgroup.gr/el/markets-publications-el-day-ahead-market

### **Admie_Data_Visualization.ipynb**

    In this notebook we create an initial visualisation of the data provided by https://www.admie.gr/en/market/market-statistics/key-data

### **MCP_Graphs.ipynb**

    In this notebook we create the combined dataframe of MCP using data from Janurary 2024-Octomber 2024
    that we later on use on our models.
    We create the additional  features: Day of the Week,Hour,Is Holiday
    (we create more features in the model notebooks later on)
    
    We create plots for the daily mean MCP of each month and compare the values of each month.
    We create:
    * heat maps comparing the MCP with the day of the week
    * the distribution of MCP by month
    * A correlation matrix for the MCP with:
      * Day of the week
      * Hour, Is Holiday
      * Month
      * Date 
    * The distribution of mcp on holidays and non holidays
    
    We continue by examining the correlation of MCP with the other forecasted hourly values provided by Enex Group
    (the PreMarketSummary Section)
    We create heatmaps comparing MCP with:
    * Production Forecast ( by energy sources)
    * Demand Forecast
    * Exports Forecast (by each interconnection)
    * Imports Forecast (by each interconnection)
    * Buy/Sell Nominations Forecast.
    
    We also create some pie charts
    displaying the final energy mix (after market close)




## Data_extraction_Of_2024_2023_2022.ipynb

    In this notebook we combine and clean the excel files collected from henex to create the data set.


