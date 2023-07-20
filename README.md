# Stock-Alert
This Python script appears to be a project that retrieves stock data for the company "Tesla Inc" (stock symbol: TSLA) from the Alpha Vantage API, analyzes the price change, and sends relevant news articles along with the percentage change to a specified phone number using the Twilio API. Here's a brief explanation of the code:

Import necessary modules: The script imports the required modules for making API requests (requests), working with dates (datetime), and sending SMS (twilio.rest.Client).

Constants: The script defines several constants:

STOCK: The stock symbol for which data is retrieved (TSLA for Tesla Inc).
COMPANY_NAME: The name of the company (Tesla Inc).
STOCK_KEY: The API key for accessing the Alpha Vantage API to get stock data.
STOCK_API: The URL for the Alpha Vantage API.
NEWS_KEY: The API key for accessing the News API.
NEWS_API: The URL for the News API.
Retrieving stock data: The script makes a request to the Alpha Vantage API to get daily adjusted stock data for the specified stock symbol. It then extracts the daily closing prices for the last two days and calculates the percentage difference between them.

Checking for significant stock change: If the percentage difference in stock prices (per_diff) is greater than 4%, the script proceeds to retrieve news articles related to the specified company using the News API.

Sending SMS with relevant information: If significant stock change is detected, the script formats the relevant stock information (percentage change and whether it went up or down) along with the titles and content of the top three news articles related to the company. The Twilio API is used to send these formatted messages to a specified phone number.
