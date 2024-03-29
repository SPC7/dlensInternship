# Decision Lens Internship 2021

* [Stock Project](Stock_Project.ipynb): Monte Carlo Simulation, Volume, Market Cap and EMA

The main idea of this paper, as well as the project, is to explore the use of interactive python tools in order to draw interesting correlations as well as insights into data sets. The project begins with plotting and charting the basics of stock data: close/open prices, daily/monthly/etc. Average price, Volume, Market Cap, etc. Candlestick charts are also available and editable. After creating a birds-eye-view of the data at hand, it was time the project evolved beyond descriptive summaries of data. 

  In order to get a more accurate depiction of the trend a stock follows, a bit more manipulation was needed on the data set. Auto correlation is a way to represent the similarities between a given time series and, in this case, a lagged version a day behind. So, what this means is that you can compare and measure the relationship between a variables current value and its past values. In the scope of this project the original code written include a time series analysis on the adjusted closing price of the stocks, however, the program allows for the user to pass any column or variable through the function. 

  Time series autocorrelation gives one of two answers, a positive number 0 to 1, or a negative number -1 to 0. A positive correlation when using autocorrelation would suggest that the trend of the variable in question will continue to behave in the same way as it has been. Values closest to positive 1 are a good predictor of what the future of a stock may look like. Negative correlation would infer that the variable in question will most likely not behave in the same way as it had in the past. Any values near -1 imply a stronger correlation. To accompany this idea, the project also includes a scatter matrix which can be created on the basis of any variable. The reason this was included was to show a visual representation of different stocks and their behaviors side-to-side.

  Apart from all of the technical analysis and data manipulation, there is one idea which every investor is very familiar with, this is hindsight bias. It is easy to say to yourself after turning a profit, “ I should have put more in” or “I should have bought more shares”. What is not easy to do is to put in the right amount that you confidently think balances and grows your portfolio. While there are tools that are available to do this, they are not always user friendly or easily accessible on popular brokerage applications. The idea here is to take the data from the stocks, as done before, and manipulate it in such a way that it is possible to predict to a certain degree of confidence what range of prices a stock or a portfolio may fall in after a given period of time.

This idea led eventually to the discovery of the Monte Carlo Simulation which would be perfect to test this idea.

  The Monte Carlo Simulation is a model which can be used to estimate the probability of infinitely different outcomes when there are multiple random variables affecting the outcomes. This process is then repeated for a specified number of trials over a certain time period for example.

The next idea was to apply this model to a stock portfolio:

  The idea is to use Cholesky decomposition in order to evaluate the value portfolio of each day over the specified time period by taking a cumulative product of the daily returns.

What is the Cholesky Decomposition: https://www.sciencedirect.com/topics/engineering/cholesky-decomposition

  The program then takes any stock or list of stocks which you would like to analyze and runs the simulation on them. The findings are interesting, especially when you look into Value at Risk. The values returned from the simulation will show you the taking of a bunch of uncorrelated data from the normal distribution and correlating the data with the covariance matrix through the use of the lower triangle of the Cholesky decomposition.

  The last thing calculated right after the Monte Carlo simulation was value at risk (VaR) as well as (CVaR). VaR is the measure of risk of loss on an investment, in the case here, the VaR will estimate how much my portfolio might lose, given a certain probability and time frame.  CVaR addresses what VaR does not. VaR may not be able to get the full picture of the risk associated with the investment, therefore, CVaR estimates how much an investment may lose under the circumstance that the VaR threshold is broken.
  
This project provided a gateway into a new idea which is currently under development in a private repository that will be linked here upon completion:

This new idea employs a similar process in simulating potential project spending and budgeting scenarios in order to give the user insight on possible solutions to overspending issues.
  
  
Links Used:
  
* https://www.investopedia.com/terms/c/conditional_value_at_risk.asp
* https://www.investopedia.com/terms/a/autocorrelation.asp
* https://rosettacode.org/wiki/Cholesky_decomposition
* https://gist.github.com/Mistobaan/555b020c58282451ec658be19da4c4e2
* https://workflowy.com/


