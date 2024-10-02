

1. Tool Selection
Use either Streamlit or Dash as your primary framework for the web app. Both are good for creating interactive web applications with Python.
2. Web Scraping Setup
Utilize BeautifulSoup and Requests libraries to scrape data from screener.in.
Ensure that the user can input the company NSE/BSE symbol, and you fetch the required data dynamically:
PE Ratios
RoCE
Growth Metrics (TTM/3/5/10-year periods)
Handle scenarios where consolidated data is not available by defaulting to standalone data.
3. Data Calculation
PE Ratio Calculation: Get the current PE directly from screener.in. The FY23 PE can be calculated as:
FY23 PE
=
Current Market Cap
FY23 Net Profit
FY23 PE= 
FY23 Net Profit
Current Market Cap
​
 
Growth Metrics: Collect and display the compounded sales/profit growth for the given periods.
4. DCF Valuation & Intrinsic PE Calculation
Use the DCF model to calculate the intrinsic PE based on user inputs (e.g., cost of capital, growth rates, RoCE, etc.).
Implement the fade period logic to smoothly transition growth rates over time, as described in the instructions.
5. Degree of Overvaluation
Calculate the degree of overvaluation using the formula provided, comparing the lower of current PE and FY23 PE against the calculated intrinsic PE.
6. UI Layout
Follow the UI layout shown in the provided example. Ensure the user input panel (with constraints on input ranges) is implemented clearly on the right side, with results displayed dynamically on the left.
7. Testing and Final Touches
Test for edge cases (missing consolidated data, incorrect symbol input).
Ensure that all computed values (e.g., PE ratios, growth metrics) are accurate and match the example given.
8. Submission
Package the web application in a way that can be run locally or deployed on platforms like Heroku for easy access by the reviewers.
Tools/Libraries to Consider:
Dash or Streamlit for the UI.
BeautifulSoup and Requests for web scraping.
Pandas for data manipulation.
NumPy/Scipy for any complex financial calculations.
Plotly for any graphical representation if need**
