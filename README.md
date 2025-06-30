# hack2skillmarketdemo - Nifty 50 Market Prediction Project
This project develops a Python-based application designed to analyze historical Nifty 50 market data and leverage a Large Language Model (LLM) to generate a qualitative prediction for the current day's market trend. The primary goal is to showcase the integration of data analysis with advanced AI capabilities for market insights.
Features
Historical Data Analysis: Processes Nifty 50 opening, high, low, and closing prices, along with trading volume, for the preceding two trading days.
LLM-Powered Prediction: Utilizes a robust LLM (specifically, gemini-2.0-flash) to interpret the historical data and provide a textual prediction about today's market direction (e.g., "Bullish," "Bearish," "Sideways") along with a brief rationale.
Modular Design: Structured with clear functions for data fetching, prompt preparation, and LLM interaction, making it easy to understand and extend.
Educational Focus: Serves as an example of how LLMs can be applied to time-series data analysis and qualitative forecasting in financial contexts.
How It Works
Data Acquisition: The application first simulates fetching Nifty 50 data for the last two trading days. In a real-world scenario, this would involve integrating with a reliable financial data API (e.g., Alpha Vantage, Yahoo Finance API).
Prompt Engineering: The acquired historical data is formatted into a natural language prompt, which is then fed to the LLM. This prompt asks the LLM to analyze the trends and provide a prediction for the current day.
LLM Inference: The LLM processes the prompt, identifies patterns or trends from the provided data, and generates a response containing its market prediction and reasoning.
Prediction Output: The LLM's prediction is then displayed to the user.
Technologies Used
Python: The core programming language for the application logic.
Google Gemini API: For accessing and interacting with the gemini-2.0-flash Large Language Model.
JSON: For handling data structures and API responses.
To run this Python code:
Save: Save the code as a .py file (e.g., nifty_predictor.py).
Install requests: If you don't have it, install the requests library:
Bash
pip install requests
Run: Execute the script from your terminal:
Bash
python nifty_predictor.py
Important Notes:
API Key: The GEMINI_API_KEY is left as an empty string (""). In the Canvas environment, this will be automatically handled. If you run this code outside Canvas, you would need to replace "" with your actual Google Cloud API key that has access to the Gemini API.
Mock Data: The get_mock_nifty_data() function provides dummy data. For a real trading application, you would replace fetch_nifty_data() with actual API calls to retrieve live or historical stock data. Libraries like yfinance or dedicated financial data APIs are common choices.
LLM Limitations: Remember the disclaimer! LLMs are powerful but are not infallible financial advisors. Their predictions are based on patterns they've learned from vast amounts of text data, not necessarily deep financial market understanding.
Asynchronous Execution: The get_llm_prediction and main functions are async. This is because API calls are I/O bound operations, and asyncio helps manage them efficiently. The asyncio.run(main()) line at the end handles running the asynchronous code.

