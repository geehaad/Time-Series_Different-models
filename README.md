# Time-Series_Different-models
understand Time series forecasting with different models in python, and fine tune the hyper-parameters to get the least possible error.

<h2>The objective of this notebook is: </h2>
<ol>
<li>In the first part: understand Time series forecasting with ARIMA model in python, and fine tune the hyper-parameters to get the least possible error.</li>
<li> In the second part: Apply CNN from scratch to the same dataset.</li>
<li> Apply Facebook prophet to the same dataset.</li>
</ol>

<h2>The dataset</h2>

Build a model to forecast the demand (passenger traffic) in Airplanes.<br> 
The data is classified in date/time and the passengers travelling per month
<h2>What is Time series analysis?</h2>

A. Time Series is a series of observations taken at specified time intervals usually equal intervals. <br>
 

<h2>We don't need to apply Time series in atleast the following 2 cases:</h2>
<ul>
<li> 
a) The dependant variable(y) (that is supposed to vary with time) is constant.<br>
    Eq: y=f(x)=4, a line parallel to x-axis(time) will always remain the same.</li> 
<li> b) The dependant variable(y) represent values that can be denoted as a mathematical function.<br> Eq: sin(x), log(x), Polynomials etc. Thus, we can directly get value at some time using the function itself. No need of forecasting.</li> 
    </ul>

<h2>There are 4 componentsof Time Series:</h2>
<ul>
<li>
a) Trend - Upward & downward movement of the data with time over a large period of time. Eq: Appreciation of Dollar vs rupee.</li>
<li>b) Seasonality - seasonal variances. Eq: Ice cream sales increases in Summer only</li>
<li>c) Noise or Irregularity - Spikes & troughs at random intervals</li>
<li>d) Cyclicity - behavior that repeats itself after large interval of time, like months, years etc.</li>
</ul>

<h2>Why does Time Series(TS) need to be stationary?</h2>
<h3>It is because of the following reasons:</h3>
<ul>
<li>a) If a TS has a particular behavior over a time interval, then there's a high probability that over a different interval, it will have same behavior, provided TS is stationary. This helps in forecasting accurately.</li>
<li>b) Theories & Mathematical formulas ae more mature & easier to apply for as TS which is stationary.</li>
</ul>

<h2>Tests to check if a series is stationary or not</h2>
<h3> There are 2 ways to check for Stationarity of a TS:</h3>
<ul>
 <li>a) Rolling Statistics - Plot the moving avg or moving standard deviation to see if it varies with time. Its a visual technique.</li>
<li>b) ADCF Test - Augmented Dickey–Fuller test is used to gives us various values that can help in identifying stationarity. The Null hypothesis says that a TS is non-stationary. It comprises of a Test Statistics & some critical values for some confidence levels. If the Test statistics is less than the critical values, we can reject the null hypothesis & say that the series is stationary. THE ADCF test also gives us a p-value. Acc to the null hypothesis, lower values of p is better.</li>
     </ul>
