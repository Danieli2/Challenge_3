# Challenge_3
#Background

In this Challenge, you'll take on the role of an analyst at a high-tech investment firm. The vice president (VP) of your department is considering arbitrage opportunities in Bitcoin and other cryptocurrencies. As Bitcoin trades on markets across the globe, can you capitalize on simultaneous price dislocations in those markets by using the powers of Pandas?

For this assignment, you’ll sort through historical trade data for Bitcoin on two exchanges: Bitstamp and Coinbase. Your task is to apply the three phases of financial analysis to determine if any arbitrage opportunities exist for Bitcoin.

#What You're Creating

You’ll create a Jupyter notebook that contains the code for your data collection, preparation, and analysis, including any visualizations. Within the same notebook file, you should use comments and text to document your analysis, including the answers to the questions in the Challenge instructions. Make this report clear and concise. Add appropriate comments to the code, and include any necessary labels for the visualizations. Remember that you’ll present this report to your VP!

To accomplish these tasks, you’ll perform the following phases of financial analysis:

Collect CSV data in a Jupyter notebook file.
Prepare the datasets for analysis by cleaning missing and erroneous data.
Analyze the data at a high level through summary statistics and visualizations, and use this information to select areas for deeper analysis. Specifically, you’ll select time periods in which to identify arbitrage opportunities.
Files
Download the following files to help you get started:

#Module 3 Challenge Files

#Instructions

This Challenge consists of the following steps:

Create your GitHub repository.
Collect the data.
Prepare the data.
Analyze the data.
Create your analysis report.
Create Your GitHub Repository
In this section, you’ll create the GitHub repository for this Challenge. To initialize the repository, use the Resources folder and the crypto_arbitrage.ipynb notebook provided in the Starter_Code folder. Then complete the following steps:

Create a README.md file for the Challenge.

Create a .gitignore file to exclude the files that you don’t want to include in your repository.

Upload your Jupyter notebook to the repository.

#IMPORTANT

Make sure to commit and push your changes as you progress through the Challenge.

#Collect the Data
To collect the data that you’ll need, complete the following steps:

Using the Pandas read_csv function and the Path module, import the data from bitstamp.csv file, and create a DataFrame called bitstamp. Set the DatetimeIndex as the Timestamp column, and be sure to parse and format the dates.

Use the head (and/or the tail) function to confirm that Pandas properly imported the data.

Repeat Steps 1 and 2 for coinbase.csv file.

#Prepare the Data

To prepare and clean your data for analysis, complete the following steps:

For the bitstamp DataFrame, replace or drop all NaN, or missing, values in the DataFrame.

Use the str.replace function to remove the dollar signs ($) from the values in the Close column.

Convert the data type of the Close column to a float.

Review the data for duplicated values, and drop them if necessary.

Repeat Steps 1–4 for the coinbase DataFrame.

#Analyze the Data

Your analysis consists of the following tasks:

Choose the columns of data on which to focus your analysis.

Get the summary statistics and plot the data.

Focus your analysis on specific dates.

Calculate the arbitrage profits.

#Choose the Columns of Data

Select the data you want to analyze. Use loc or iloc to select the following columns of data for both the bitstamp and coinbase DataFrames:

Timestamp (index)

Close

#Get the Summary Statistics and Plot the Data

Sort through the time series data associated with the bitstamp and coinbase DataFrames to identify potential arbitrage opportunities. To do so, complete the following steps:

Generate the summary statistics for each DataFrame by using the describe function.

For each DataFrame, create a line plot for the full period of time in the dataset. Be sure to tailor the figure size, title, and color to each visualization.

In one plot, overlay the visualizations that you created in Step 2 for bitstamp and coinbase. Be sure to adjust the legend and title for this new visualization.

Using the loc and plot functions, plot the price action of the assets on each exchange for different dates and times. Your goal is to evaluate how the spread between the two exchanges changed across the time period that the datasets define. Did the degree of spread change as time progressed?

Focus Your Analysis on Specific Dates
Focus your analysis on specific dates by completing the following steps:

Select three dates to evaluate for arbitrage profitability. Choose one date that’s early in the dataset, one from the middle of the dataset, and one from the last year of the time period.

For each of the three dates, generate the summary statistics and then create a box plot. This big-picture view is meant to help you gain a better understanding of the data before you perform your arbitrage calculations. As you compare the data, what conclusions can you draw?

Calculate the Arbitrage Profits
Calculate the potential profits for each date that you selected in the previous section. Your goal is to determine whether arbitrage opportunities still exist in the Bitcoin market. Complete the following steps:

For each of the three dates, measure the arbitrage spread between the two exchanges by subtracting the lower-priced exchange from the higher-priced one. Then use a conditional statement to generate the summary statistics for each arbitrage_spread DataFrame, where the spread is greater than zero.

For each of the three dates, calculate the spread returns. To do so, divide the instances that have a positive arbitrage spread (that is, a spread greater than zero) by the price of Bitcoin from the exchange you’re buying on (that is, the lower-priced exchange). Review the resulting DataFrame.

For each of the three dates, narrow down your trading opportunities even further. To do so, determine the number of times your trades with positive returns exceed the 1% minimum threshold that you need to cover your costs.

Generate the summary statistics of your spread returns that are greater than 1%. How do the average returns compare among the three dates?

For each of the three dates, calculate the potential profit, in dollars, per trade. To do so, multiply the spread returns that were greater than 1% by the cost of what was purchased. Make sure to drop any missing values from the resulting DataFrame.

Generate the summary statistics, and plot the results for each of the three DataFrames.

Calculate the potential arbitrage profits that you can make on each day. To do so, sum the elements in the profit_per_trade DataFrame.

Using the cumsum function, plot the cumulative sum of each of the three DataFrames. Can you identify any patterns or trends in the profits across the three time periods?

#Create Your Analysis Report

Write your final report by using text or comments within your Jupyter notebook file. This report should summarize your analysis and include the following:

Assumptions or discoveries that you made during the analysis

Summary tables and calculations

Visualizations

#Requirements

Create Your GitHub Repository (10 points)
To receive all points, you must:
Create a README.md file for the Challenge. (3 points)
Create a .gitignore file to exclude the files that you don’t want to include in your repository. (3 points)
Upload your Jupyter notebook to the repository. (4 points)
Collect the Data (10 points)
To receive all points, your code must:
Using the Pandas read_csv function, import the data from bitstamp.csv and create a DataFrame called bitstamp. Set the index as the Timestamp column, and be sure to parse and format the dates. (3 points)
Use the head (and/or the tail) function to confirm that Pandas properly imported the data. (3 points)
Repeat Steps 1 and 2 for coinbase.csv. (4 points)
Prepare the Data (10 points)
To receive all points, your code must:
For the bitstamp DataFrame, replace or drop all NaN, or missing, values in the DataFrame. (2 points)
Use the replace function to remove the dollar signs ($) from the values in the Close column. (2 points)
Convert the data type of the Close column to a float. (2 points)
Review the data for duplicated values, and drop them if necessary. (2 points)
Repeat the four preceding steps for the coinbase DataFrame. (2 points)
Analyze the Data (20 points)
To receive all points, your code must:
Get the summary statistics and plot the data. (5 points)
Focus your analysis on specific dates. (5 points)
Calculate the arbitrage profits. (10 points)
Create Your Analysis Report (20 points)
To receive all points, your report must include:
Assumptions or discoveries that you made during the analysis (10 points)
Summary tables and calculations (5 points)
Visualizations (5 points)
Coding Conventions and Formatting (10 points)
To receive all points, your code must:
Place imports at the beginning of the file, just after any module comments and docstrings and before module globals and constants. (3 points)
Name functions and variables with lowercase characters and with words separated by underscores. (2 points)
Follow Don't Repeat Yourself (DRY) principles by creating maintainable and reusable code. (3 points)
Use concise logic and creative engineering where possible. (2 points)
Deployment and Submission (10 points)
To receive all points, you must:
Submit a link to a GitHub repository that’s cloned to your local machine and contains your files. (4 points)
Use the command line to add your files the repository. (3 points)
Include appropriate commit messages in your files. (3 points)
Code Comments (10 points)
To receive all points, your code must:
Be well commented with concise, relevant notes that other developers can understand. (10 points)
Submission
To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

