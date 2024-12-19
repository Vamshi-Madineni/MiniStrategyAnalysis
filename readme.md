`MiniStrategyAnalysis` is a Python-based stock breakout strategy analyzer built with Streamlit, Yahoo Finance, Plotly, and Pandas. It allows users to analyze stocks using a breakout strategy, view key metrics, and download results. The app provides stock data visualizations and detailed analysis, including summary statistics and trade results.

Files in the Project:

- **app.py**: The main application file that runs the Streamlit app, collects user input, fetches stock data, performs analysis, and generates visualizations and reports.
- **requirements.txt**: Contains the necessary Python libraries that need to be installed for the project.


Requirements:

1. **Python 3.x**: Ensure you have Python installed (Python 3.7 or higher recommended).
2. **Streamlit**: A framework to build interactive web apps.
3. **yfinance**: To fetch historical stock data from Yahoo Finance.
4. **Pandas**: To manipulate and analyze the data.
5. **Plotly**: For creating interactive charts and visualizations.
6. **Other dependencies**: A list of required libraries is included in the `requirements.txt`.

---

## Installation Instructions

Step 1: Clone the Repository

Clone the project repository to your local machine.

```
git clone https://github.com/Vamshi-Madineni/MiniStrategyAnalysis.git

cd MiniStrategyAnalysis
```

Step 2: Set Up a Virtual Environment (Optional)

It’s recommended to create a virtual environment to manage dependencies.

```
python -m venv venv
```

Activate the virtual environment:
- On Windows:
  ```
  .\venv\Scripts\activate
  ```
- On macOS/Linux:
  ```
  source venv/bin/activate
  ```

Step 3: Install Dependencies

Use `pip` to install the required libraries from the `requirements.txt` file.

```
pip install -r requirements.txt
```

Step 4: Run the App

Once the dependencies are installed, you can run the Streamlit app with the following command:

```
streamlit run app.py
```

The app will open in your default web browser.

---

## Using the App

### Inputs:

1. **Stock Ticker(s)**: 
   - Accepted Values: One or more stock ticker symbols, separated by commas (e.g., `AMZN`, `TSLA`).
   - Notes: Tickers must be valid stock symbols listed on Yahoo Finance.
   
2. **Start Date**: 
   - Accepted Values: A date in `YYYY-MM-DD` format.
   - Notes: Start date should not be in the future. It represents the start of the data collection period for analysis. Should be at least 20 days before the end date.
   
3. **End Date**: 
   - Accepted Values: A date in `YYYY-MM-DD` format.
   - Notes: End date should not be in the future. It represents the end of the data collection period. Should be at least 20 days after the start date.
   
4. **Volume Breakout Threshold (%)**: 
   - Accepted Values: A positive number representing the minimum percentage increase in trading volume compared to the 20-day moving average volume.
   - Default Value: 200%
   - Minimum Value: 50%
   - Notes: This value represents the percentage increase in volume to be considered a breakout. E.g., 200% means the volume is twice the 20-day moving average.
   
5. **Daily Change Threshold (%)**: 
   - Accepted Values: A positive number representing the minimum percentage increase in price for the breakout condition.
   - Default Value: 2.0%
   - Minimum Value: 0.1%
   - Notes: This value represents the minimum percentage increase in stock price for the breakout condition. E.g., 2.0 means the price must increase by at least 2% on the breakout day.
   
6. **Holding Period (Days)**: 
   - Accepted Values: A positive integer representing how many days to hold the stock after the breakout.
   - Default Value: 10 days
   - Minimum Value: 1
   - Notes: This is the number of days the strategy assumes to hold the stock after the breakout day for analysis.

---

## How to Use the App

1. **Enter Stock Ticker(s)**: Input one or more valid stock tickers, separated by commas (e.g., `AAPL, TSLA`).
2. **Set Start and End Dates**: Select the start and end dates for the stock data analysis period.
3. **Set Breakout Thresholds**: Define the percentage volume and price change thresholds to identify breakout conditions.
4. **Set Holding Period**: Define how many days to hold the stock after a breakout.
5. **Click "Generate Report"**: Press the button to run the analysis. The app will:
   - Fetch stock data.
   - Analyze breakouts based on the defined conditions.
   - Display summary statistics and detailed results.
   - Provide stock price and volume visualizations.
   - Offer a downloadable CSV file of the breakout analysis results.

---

## Output

1. **Summary Statistics**:
   - Total Trades: The total number of trades identified based on breakout conditions.
   - Win Rate (%): The percentage of successful trades (positive return).
   - Average Return (%): The average return percentage of all trades.
   - Max Return (%): The highest return percentage of any trade.
   - Min Return (%): The lowest return percentage of any trade.
   - Standard Deviation (%): The standard deviation of trade returns.
   
2. **Detailed Trade Results**:
   - Entry Date: The date the breakout occurred and the stock was entered.
   - Exit Date: The date the stock was sold after the holding period.
   - Entry Price: The price of the stock at the entry point.
   - Exit Price: The price of the stock at the exit point.
   - Return Percentage: The percentage return from entry to exit.

3. **Visualizations**:
   - Stock Price Chart: A candlestick chart showing the stock's price over time.
   - Volume Chart: A bar chart showing the stock's trading volume over time.
   - Returns Distribution: A histogram showing the distribution of returns for all trades.
   
4. **Downloadable CSV**:
   - After the report is generated, a CSV file of the detailed trade results will be available for download.

---

## Notes

- Ensure that you are connected to the internet when using this app, as it fetches real-time data from Yahoo Finance.
- The app uses Plotly for interactive charts, which should work smoothly in the browser.

---
## Roadblocks
- During the setup of the MiniStrategyAnalysis project, the main roadblock was troubleshooting the issues with the multiple download buttons and handling different stock tickers efficiently. Adjustments were made to ensure the download functionality worked correctly for each stock’s analysis report. Additionally, the unique key assignment for each button helped prevent conflicts. Overall, the project took approximately 2.5 hours to complete, including the implementation of features and debugging.