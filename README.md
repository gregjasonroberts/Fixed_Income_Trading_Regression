## Fixed_Income_Trading_Regression

<!-- wp:paragraph -->
<p>Regressing client trading activity to the treasury markets and bond market volatility.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The following project is an example of an analysis that I performed for work on behalf of a request from the CFO of my organization.   I was tasked with running a regression analysis on the average trading volumes for US Treasuries and understand the correlations with internal fixed income trading revenues.  We also looked at the MOVE Index (Merrill Lynch Option Volatility Estimate) to analyze that correlation as well.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>A significant portion of the revenues in this business unit gets generated from the processing of client trading activity. in US treasury securities. Suffice to say, the ability to forecast revenues is integral to management's guidance to Wall Street and thus it's performance and limiting earnings volatility.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>I will begin by highlighting some of the data consolidation and preprocessing skills utilized in this project as well as some visualization techniques brought to bear.  </p>
<!-- /wp:paragraph -->

### Overview

* Analyze the datasets from internal trading activity, MOVE treasury volatiilty index, and Primary Dealer activity
* Find feature variables that could help predict future client trading activity
* Find weakness in the premise that the MOVE volatility index could predict internal trading volumes



### Code and Resources Used
Python Version: 3.7  
Environment: Jupyter notebook 
Packages: pandas, numpy, statsmodels, sklearn, matplotlib, seaborn, scipy, yellowbrick
*The datasets for this project have been sourced both internally and anonymized as well as from NY Fed data on Primary Dealer activity published weekly and the treasury volaiilty proxy, MOVE Index (Merrill Lynch Option Volatility Estimate ‒ a well-recognized indicator of U.S. interest rate volatility that is often referred to as the VIX for Bonds.


### Data Cleaning
After reading in the data, it was necessary to transform the data to prepare it for modeling it in the formats of internal dataset
* The Primary Dealer activity is published weekly and therefore all datasets were transformed from daily to weekly to conform with the less frequent dataset rather than interpolating data into a misrepresented set.
* Some of the datasets contained NaN values and those values were interpolated by taking the average between nearest values of the NaN

### EDA
I looked at a correlation matrix to determine which predictor variables were ultimately sufficient for modeling (high correlation to the target) as well as careful to introduce multicollinearity which was a potential issue in this set. Below are a few highlights:

![alt text](images/corr_matrix.png)
![alt text](images/prob_plot.png)
![alt text](images/fi_histplot.png)

### Model Building



### Model Performance


