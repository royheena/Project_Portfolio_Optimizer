# Portfolio Analysis
![Portfolio_Analysis_Tool](images/PortfolioAnalysisSuite.png)

For Project 3, we decided to improve upon the Portfolio Analysis tool that we developed as part of Project 1.  The Project 1 Portfolio Analysis tool accepted a user portfolio in the form of a list of transactions.  The tool used the Financial Modeling Prep API to grab stock data including daily closing prices, P/E Ratio, Beta, Industry, etc. The tool then calculated daily returns, current balance, performed a diversification analysis, and calculated the efficient frontier.

However, since we only had 2 weeks to work on Project 1, there were several improvements we wanted to make to the tool.
1. Change the code to make it dynamic to be able to analyze any number of transactions within the portfolio.
2. Simplify the data and clean the code by replacing the Financial Modeling Prep API with yfinance.
3. Correct the returns calculations.
4. Correct the S&P index comparison.

In addition to the improvements above, we wanted to add the following features:
1. A robo advisor that guides the investor through questions to create a new hypothetical portfolio for analysis and comparison to the investor's current portfolio.
2. A GUI interface to launch the tool to a wider market
3. An X-year future balance projection based on the current portfolio's balance, mean, and standard deviation, where X is a solicited user input by the robo advisor.

Please refer to [Portfolio Analysis Presentation2.pptx](https://github.com/royheena/Project_Portfolio_Optimizer) for a summary of the Project 3 Portfolio Analysis tool and sample outputs.  

The Project 3 team faced several challenges making the improvements/enhancements to the Project 1 Portfolio Anlaysis tool.
1. Two of the team members were new to the Portfolio Analysis tool so they had a larger learning curve than the members that were on Project 1.  This learning curve ate into the development time allotted for Project 3.
2. Even though we significantly reduced the complexity of the code to receive the API data and convert the data into a user-friendly dataframe for analysis, the yfiance API did not offer the same robust data as the Financial Modeling Prep API so we had to port code that we weren't anticipating porting.
3. The GUI interface required learning a new coding language.  We tried to use tkinter as the GUI interface.  We made remarkable progress within the first week of Project 3.  The major coding blocks were developed and the new language was understood well enough to hack the code.  However, the stitching became an overwhelming task to complete within the last week so unfortunately we had to abandon this enhancement.  Even though the GUI did not make it into the final Project 3 it was really cool to learn how to make GUIs using tkinter.  This will definitely be on the option list for the next project enhancement.
4. The original Project 1 had a dashboard, and it rendered all of the visualizations of the original code. Unfortunately, the dashboard panel is no longer rendering the visualizations (our team members have a love/hate relationship with pyviz). The graphs and stats panel need a platform for display.

Future Improvements to the Portfolio Analysis tool include:
1. We did not want to deal with api keys this go around so we chose to work with yfinance. However, yfinance has limited stocks/etfs/mutual funds so we will have to change this to Quandl or Alpaca in the next go around.
2. The Portfolio Analysis Tool needs to be in a separate notebook and the code needs to be broken into classes and functions so that the output (graphs and ticker stats) can be called in one go. 
3. The Robo-Advisor code needs to be in a separate notebook. So it can call the portfolio_analysis_tool over and over again, without having to go through the original code. 
4. More analysis can be added to the Portfolio Analysis Tool:
    * Functionality for Realized and UnRealized Gains is already in the code, opportunity to create visualizations for this.
    * With use of a better API pull, additional analysis can be done on Earnings, PE Ratios, Dividend Yield, etc. 
    * Displaying table of stock weights for current vs best sharpe ratios. The data is already avaliable in the code, we would just need to display it to the user.
5. More functionality can be added to the Robo-Advisor:
    * User can have a choice of inputting the purchase price of the stock vs. using the closing price (current code).
    * User can input sell data
    * User can replace one ticker with another and robo with recalculate transaction assuming the user bought/sold the alternate ticker
    * Investor Risk assessment to recommend a new portfolio mix
6. Use of a GUI (interface) for the Robo-Advisor and output for a cleaner visually appealing product.
