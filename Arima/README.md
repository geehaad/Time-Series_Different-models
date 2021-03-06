<h1>ARIMA(Auto Regressive Integrated Moving Average)</h1> 
<b>ARIMA </b>is a combination of 2 models AR(Auto Regressive) & MA(Moving Average). <br>
<h3>It has 3 hyperparameters -</h3> 
<ul>
  <li>P (auto regressive lags),</li> <li>d (order of differentiation),</li> <li>Q (moving avg.) which respectively comes from the AR, I & MA components.</li> 
</ul> The AR part is correlation between prev & current time periods. <br>To smooth out the noise, the MA part is used. <br>The I part binds together the AR & MA parts. <h1>The general steps to implement an ARIMA model are:</h1>
<ol> 
  <li> Load the data: The first step for model building is of course to load the dataset. </li> <li> Preprocessing: Depending on the dataset, the steps of preprocessing will be defined. This will include creating timestamps, converting the dtype of date/time column, making the series univariate, etc. </li> <li> Make series stationary: In order to satisfy the assumption, it is necessary to make the series stationary. This would include checking the stationarity of the series and performing required transformations. </li> 
  <li> Determine d value: For making the series stationary, the number of times the difference operation was performed will be taken as the d value. </li> 
  <li> Create ACF and PACF plots: This is the most important step in ARIMA implementation. ACF PACF plots are used to determine the input parameters for our ARIMA model. </li> 
  <li> Determine the p and q values: Read the values of p and q from the plots in the previous step. </li> <li> Fit ARIMA model: Using the processed data and parameter values we calculated from the previous steps, fit the ARIMA model. </li> 
  <li> Predict values on validation set: Predict the future values </li>
  <li> Calculate RMSE: To check the performance of the model, check the RMSE value using the predictions and actual values on the validation set. </li>
</ol>
<h1> Tuning Parameters_ Auto ARIMA Although ARIMA </h1>
is a very powerful model for forecasting time series data, the data preparation and parameter tuning processes end up being really time consuming. <br>
Before implementing ARIMA, you need to make the series stationary, and determine the values of p and q using the plots we discussed above. <br>
Auto ARIMA makes this task really simple for us as it eliminates steps 3 to 6 we saw in the previous section.<br>

<ol> 
  
  <h3>Below are the steps you should follow for implementing auto ARIMA: </h3>
  <li> Load the data: This step will be the same. Load the data into your notebook. </li> 
  <li> Preprocessing data: The input should be univariate, hence drop the other columns. </li>
  <li> Fit Auto ARIMA: Fit the model on the univariate series. </li> 
  <li> Predict values on validation set: Make predictions on the validation set. </li> 
  <li> Calculate RMSE: Check the performance of the model using the predicted values against the actual values. </li> 
</ol>
