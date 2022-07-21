# Module-7-Challenge

![alt text](7-4-challenge-image.png)

## Background
In recent years, finance has had an explosion in passive investing. **Passive investing** means that you invest in a group of assets called an exchange-traded fund (ETF). This way, you don’t spend time researching individual stocks or companies, or take the risk of investing in a single stock. ETFs offer more diversification.

In this Challenge assignment, you’ll build a financial database and web application by using SQL, Python, and the Voilà library to analyze the performance of a hypothetical fintech ETF.

## What You're Creating
For this Challenge assignment, you need to create and submit the following deliverables:

* A Jupyter notebook that contains the following:

    * Your analysis of the ETF data that a SQL database stores

    * Professionally styled and formatted interactive visualizations

* A screenshot or video of the web application that you created by deploying your Jupyter notebook via the Voilà library

Upload the Jupyter notebook for this assignment to your GitHub repository. Make sure to update the `READ.md` file to include an explanation of your project, the screenshot or video of your deployed application, and any other information that’s needed to interact with your notebook and web application.

## Files
Download the following files to help you get started:
* [Module 7 Challenge File](Starter_Code/Starter_Files/visual_data_analysis.ipynb)

## Instructions
Use the `etf_analyzer.ipynb notebook` to complete your analysis of a fintech ETF that consists of four stocks: GOST, GS, PYPL, and SQ. Each stock has its own table in the `etf.db` database, which the `Starter_Code` folder contains.

Analyze the daily returns of the ETF stocks both individually and as a whole. Then deploy the visualizations to a web application by using the Voilà library.

The detailed instructions are divided into the following parts:

* Analyze a single asset in the ETF

* Optimize data access with advanced SQL queries

* Analyze the ETF portfolio

* Deploy the notebook as a web application

# Analyze a Single Asset in the ETF
For this part of the assignment, you’ll use SQL queries with Python, Pandas, and hvPlot to analyze the performance of a single asset from the ETF.

Complete the following steps:

1. Write a SQL `SELECT` statement by using an f-string that reads all the PYPL data from the database. Using the SQL `SELECT` statement, execute a query that reads the PYPL data from the database into a Pandas DataFrame.

2. Use the `head` and `tail` functions to review the first five and the last five rows of the DataFrame. Make a note of the beginning and end dates that are available from this dataset. You’ll use this information to complete your analysis.

3. Using hvPlot, create an interactive visualization for the PYPL daily returns. Reflect the “time” column of the DataFrame on the x-axis. Make sure that you professionally style and format your visualization to enhance its readability.

4. Using hvPlot, create an interactive visualization for the PYPL cumulative returns. Reflect the “time” column of the DataFrame on the x-axis. Make sure that you professionally style and format your visualization to enhance its readability.

# Optimize Data Access with Advanced SQL Queries
For this part of the assignment, you’ll continue to analyze a single asset (PYPL) from the ETF. You’ll use advanced SQL queries to optimize the efficiency of accessing data from the database.

Complete the following steps:

1. Access the closing prices for PYPL that are greater than 200 by completing the following steps:

    * Write a SQL `SELECT` statement to select the dates where the PYPL closing price was higher than 200.0.

    * Using the SQL statement, read the data from the database into a Pandas DataFrame, and then review the resulting DataFrame.

    * Select the “time” and “close” columns for those dates where the closing price was higher than 200.0.

2. Find the top 10 daily returns for PYPL by completing the following steps:

    * Write a SQL statement to find the top 10 PYPL daily returns. Make sure to do the following:

        * Use `SELECT` to select only the “time” and “daily_returns” columns.

        * Use `ORDER` to sort the results in descending order by the “daily_returns” column.

        * Use `LIMIT` to limit the results to the top 10 daily return values.

    * Using the SQL statement, read the data from the database into a Pandas DataFrame, and then review the resulting DataFrame.

# Analyze the ETF Portfolio
For this part of the assignment, you’ll build the entire ETF portfolio and then evaluate its performance. To do so, you’ll build the ETF portfolio by using SQL joins to combine all the data for each asset.

Complete the following steps:

1. Write a SQL query to join each table in the portfolio into a single DataFrame. To do so, complete the following steps:

    * Use a SQL inner join to join each table on the “time” column. Access the “time” column in the `GDOT` table via the `GDOT.time` syntax. Access the “time” columns from the other tables via similar syntax.

    * Using the SQL query, read the data from the database into a Pandas DataFrame. Review the resulting DataFrame.

2. Create a DataFrame that averages the “daily_returns” columns for all four assets. Review the resulting DataFrame.

HINT
3. Use the average daily returns in the etf_portfolio_returns DataFrame to calculate the annualized returns for the portfolio. Display the annualized return value of the ETF portfolio.

HINT
4. Use the average daily returns in the `etf_portfolio_returns` DataFrame to calculate the cumulative returns of the ETF portfolio.

5. Using hvPlot, create an interactive line plot that visualizes the cumulative return values of the ETF portfolio. Reflect the “time” column of the DataFrame on the x-axis. Make sure that you professionally style and format your visualization to enhance its readability.

# Deploy the Notebook as a Web Application
For this part of the assignment, complete the following steps:

    1. Use the Voilà library to deploy your notebook as a web application. You can deploy the web application locally on your computer.

    2. Take a screen recording or screenshots to show how the web application appears when using Voilà. Include the recording or screenshots in the `README.md` file for your GitHub repository.

# Requirements
# Analyze a Single Asset in the ETF (20 points)
To receive all points, you must:

* Write a `SQL SELECT` statement by using an f-string that reads all the PYPL data from the database. Using the SQL `SELECT` statement, execute a query that reads the PYPL data from the database into a Pandas DataFrame. (5 points)

* Use the `head` and `tail` functions to review the first five and the last five rows of the DataFrame. Make a note of the beginning and end dates that are available from this dataset. Use this information to complete your analysis. (5 points)

* Using hvPlot, create an interactive visualization for the PYPL daily returns. Reflect the “time” column of the DataFrame on the x-axis. Make sure that you professionally style and format your visualization to enhance its readability. (5 points)

* Using hvPlot, create an interactive visualization for the PYPL cumulative returns. Reflect the “time” column of the DataFrame on the x-axis. Make sure that you professionally style and format your visualization to enhance its readability. (5 points)

# Optimize Data Access with Advanced SQL Queries (20 points)
To receive all points, you must:

* Access the closing prices for PYPL that are greater than 200:

    * Write a SQL `SELECT` statement to select the dates where the PYPL closing price was higher than 200.0. (4 points)

    * Using the SQL statement, read the data from the database into a Pandas DataFrame, and then review the resulting DataFrame. (3 points)

    * Select the “time” and “close” columns for those dates where the closing price was higher than 200.0. (3 points)

* Find the top 10 daily returns for PYPL:

    * Write a SQL statement to find the top 10 PYPL daily returns. (2 points)

        * Use `SELECT` to select only the “time” and “daily_returns” columns. (2 points)

        * Use `ORDER` to sort the results in descending order by the “daily_returns” column. (2 points)

        * Use `LIMIT` to limit the results to the top 10 daily return values. (2 points)

    * Using the SQL statement, read the data from the database into a Pandas DataFrame, and then review the resulting DataFrame. (2 points)

# Analyze the ETF Portfolio (20 points)
To receive all points, you must:

* Write a SQL query to join each table in the portfolio into a single DataFrame.

    * Use a SQL inner join to join each table on the “time” column. Access the “time” column in the `GDOT` table via the `GDOT.time` syntax. Access the “time” columns from the other tables via similar syntax. (3 points)

    * Using the SQL query, read the data from the database into a Pandas DataFrame. Review the resulting DataFrame. (3 points)

* Create a DataFrame that combines the “daily_returns” columns for all four assets. Review the resulting DataFrame. (3 points)

* Use the portfolio returns in the `etf_portfolio_returns` DataFrame to calculate the annualized returns for the portfolio. Display the annualized return value of the ETF portfolio.

    * To calculate the annualized returns, take the mean of the `etf_portfolio_returns` and multiply by 252. (2 points)

    * To convert the decimal to a percentage, multiply the results by 100. (2 points)

* Use the portfolio returns in the `etf_portfolio_returns` DataFrame to calculate the cumulative returns of the ETF portfolio. (3 points)

* Using hvPlot, create an interactive line plot that visualizes the cumulative return values of the ETF portfolio. Reflect the “time” column of the DataFrame on the x-axis. Make sure that you professionally style and format your visualization to enhance its readability. (4 points)

# Deploy the Notebook as a Web Application (10 points)
To receive all points, you must:

* Use the Voilà library to deploy your notebook as a web application. Deploy the web application locally on your computer. (5 points)

* Take a screen recording or screenshots to show how the web application appears when using Voilà. Include the recording or screenshots in the `README.md` file for your GitHub repository. (5 points)

# Coding Conventions and Formatting (10 points)
To receive all points, you must:

* Place imports at the top of the file, just after any module comments and docstrings and before module globals and constants. (3 points)

* Name functions and variables with lowercase letters and with words separated by underscores. (2 points)

* Follow Don't Repeat Yourself (DRY) principles, creating maintainable and reusable code. (3 points)

* Use concise logic and creative engineering where possible. (2 points)

# Deployment and Submission (10 points)
To receive all points, you must:

* Submit a link to a GitHub repository that’s cloned to your local computer and that contains your files. (4 points)

* Use the command line to add your files to the repository. (3 points)

* Include appropriate commit messages for your files. (3 points)

# Comments (10 points)
To receive all points, your code must:

* Be well commented with concise, relevant notes that other developers can understand. (10 points)

# Submission
To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

NOTE
You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next module.

Comments are disabled for graded submissions in Bootcamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Manager. If you would like to resubmit your work for an additional review, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.