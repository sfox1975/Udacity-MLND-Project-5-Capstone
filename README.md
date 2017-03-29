# Udacity-MLND-Project-5-Capstone
Using machine learning to predict the directionality of the S&amp;P500 Stock Market Index

## Purpose
The purpose of this project is to determine whether machine learning techniques can be used to predict the directionality (i.e. up or down) of the S&P500 stock market index on any given day, based on the market opening price and an assortment of historical market data. For this project, directionality will be defined as a ‘1’ for an increase in market value and as a ‘0’ for a decrease in market value, so the problem will be a machine learning ‘classification’ problem. The directionality is defined relative to the opening value. For example, if the market opens at 2,170 at 9:30ET and closes at 2,175 at 16:00ET, that would count as an increase and directionality value of ‘1’.

## Usage
To run the notebook, type the following from a command line: 
`jupyter notebook Fox-Capstone.ipynb`

## Data
All data used for the project was downloaded from Yahoo! Finance:

http://finance.yahoo.com/quote/%5EGSPC/history?p=%5EGSPC

http://finance.yahoo.com/quote/%5EVIX/history?p=^VIX

The data used in this project was historical market data from January 29th, 1993 to September 29th, 2016. The start date was chosen based on this date being the earliest date for which volatility (VIX) data was available via Yahoo! Finance. The VIX is considered the market’s ‘fear index’ and measures the volatility of stocks. During times of market turmoil, the VIX increases.

The raw data is included in the ‘SP500_historical.csv’ file provided as part of the project submission. The raw data file contained 10 fields, and as will be discussed later, these 10 fields were used to derive the features for the machine learner. The 10 raw data fields are as follows:

* Date:			calendar date for any given data row
* SP_Open:		opening value (recorded at 9:30ET) for the S&P500
* SP_High:		highest value on any given day for the S&P500
* SP_Low:		lowest value on any given day for the S&P500
* SP_Close:		closing value (recorded at 16:00ET) for the S&P500
* SP_Volume:		number of shares of S&P500 components traded
* Vix_Open:		opening value for the VIX index
* Vix_High:		highest value on any given day for the VIX index
* Vix_Low:		lowest value on any given day for the VIX index
* Vix_Close:		closing value for the VIX index

For the date range under consideration, the raw data file contains 5,962 trading days. Figure 1 presents a plot of the S&P500 and VIX closing value for each of these days.

## Libaries Used
* scikit-learn
* TensorFlow

## Additional Documents
* Fox-Capstone.ipynb: contains code and exploratory data analysis and commentary. Written in Python (2.7.12) in Jupyter Notebooks
* Fox-MLND-Capstone.pdf: project report, containing summary of the analyses and key conclusions
* SP500_historical.csv: raw data, as discussed in the 'Data' section above
