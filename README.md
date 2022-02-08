# AR_Accounts_Prediction_xgboost

My team created an xgboost model using over 300 variables. The goal was to predict the pay rate of invoices, giving the company insight into which accounts would potentially be late on payment. The dataset was given to us by the client and consisted of over 2.7 million rows and 97 columns. We calculated a new variable, age, as the target variable for our model. The code includes visualization plots of the data, as well as residuals plot and ecdf plot for the results. Our model was able to predict rate of invoice payment within 2 weeks for 90% of accounts. 

Multiple functions make up this code. They are explained below.

prepareData():
- Function to prepare data for analysis
- Create subsample of data - easier for processing
- Calculate age of invoice and add column to dataset (set >= 0)
- Filter data to 'Invoice' type

encodeData():
- Function to encode data for xgboost model
- Turns categorical data into 0/1
- Removes unneccessary columns

plotData():
- Function to plot data
- 4 plots:
- Raw Invoice Delays by Size of Invoice
- Trend Line in Invoice Age Since 2005
- Forecast and trends by year, day of week, and day of year
- Trends for Each Profit Center

trainModel():
- Function to train xgboost model
-  Create training data (70% of total) and testing data (30% of total)
- Predict on test data

plotResiduals():
- Function to plot residuals

plotImportance():
- Function to plot variable importance
