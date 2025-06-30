# **Nifty 50 Market Prediction Project**

## **Project Description**

This project develops a Python-based application designed to analyze historical Nifty 50 market data and leverage a Large Language Model (LLM) to generate a qualitative prediction for the current day's market trend. The primary goal is to showcase the integration of data analysis with advanced AI capabilities for market insights.

## **Features**

* **Historical Data Analysis:** Processes Nifty 50 opening, high, low, and closing prices, along with trading volume, for the preceding two trading days.  
* **LLM-Powered Prediction:** Utilizes a robust LLM (specifically, gemini-2.0-flash) to interpret the historical data and provide a textual prediction about today's market direction (e.g., "Bullish," "Bearish," "Sideways") along with a brief rationale.  
* **Modular Design:** Structured with clear functions for data fetching, prompt preparation, and LLM interaction, making it easy to understand and extend.  
* **Educational Focus:** Serves as an example of how LLMs can be applied to time-series data analysis and qualitative forecasting in financial contexts.

## **How It Works**

1. **Data Acquisition:** The application first simulates fetching Nifty 50 data for the last two trading days. In a real-world scenario, this would involve integrating with a reliable financial data API (e.g., Alpha Vantage, Yahoo Finance API).  
2. **Prompt Engineering:** The acquired historical data is formatted into a natural language prompt, which is then fed to the LLM. This prompt asks the LLM to analyze the trends and provide a prediction for the current day.  
3. **LLM Inference:** The LLM processes the prompt, identifies patterns or trends from the provided data, and generates a response containing its market prediction and reasoning.  
4. **Prediction Output:** The LLM's prediction is then displayed to the user.

## **Technologies Used**

* **Python:** The core programming language for the application logic.  
* **Google Gemini API:** For accessing and interacting with the gemini-2.0-flash Large Language Model.  
* **JSON:** For handling data structures and API responses.

**To run this Python code:**

1. **Save:** Save the code as a `.py` file (e.g., `nifty_predictor.py`).  
2. **Install `requests`:** If you don't have it, install the `requests` library:  
   Bash  
   pip install requests  
3. **Run:** Execute the script from your terminal:  
   Bash  
   python nifty\_predictor.py
