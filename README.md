# Stock Movement Analysis Based on Social Media Sentiment

This repository comprehensively analyzes stock price movements based on sentiment extracted from Reddit discussions. Using advanced natural language processing techniques, the project combines sentiment analysis with stock market data to predict stock price trends and movement directions.

## Project Structure

### `reddit_stock_raw.csv`
Contains raw scraped data from Reddit, including discussion text and timestamps. Ensure the file is placed in the repository's root directory or update the path in the `reddit_csv_path` variable.

#### Required Columns:
- **Datetime**: The timestamp of the Reddit post.
- **Discussion**: The content of the discussion or post.

### `scraping_reddit_data.ipynb`
A Jupyter Notebook that provides the code to scrape Reddit data for stock-related discussions. Use this notebook to collect fresh data from Reddit.

### `STOCK_MARKET_CLASS_AND_REGG.ipynb`
The main Jupyter Notebook containing the core implementation for:
- Preprocessing Reddit data.
- Conducting sentiment analysis.
- Merging sentiment data with stock price data.
- Training machine learning models to predict stock price trends and directions.

## Features

### Sentiment Analysis
Utilizes two sentiment analysis approaches:
- **VADER Sentiment Analysis**: Extracts polarity scores from the Reddit discussions.
- **Transformer-based Sentiment Analysis**: Uses Hugging Face's pre-trained models to classify sentiment as Positive or Negative.

### Stock Data Integration
Fetches historical stock price data using the `yfinance` library, incorporating technical indicators like:
- **SMA** (Simple Moving Average)
- **EMA** (Exponential Moving Average)
- **RSI** (Relative Strength Index)
- **Volatility**

### Machine Learning Models
- **Regression**: Predicts future stock prices.
- **Classification**: Predicts stock price movement direction (up or down).

### Visualization
- Sentiment distribution.
- Discussion trends over time.
- Actual vs. predicted stock prices and directions.

## Installation and Setup

### Prerequisites
Ensure the following tools and libraries are installed:
- Python 3.8+
- Jupyter Notebook
- Python libraries: `pandas`, `numpy`, `nltk`, `yfinance`, `scikit-learn`, `xgboost`, `matplotlib`, `transformers`

To install missing libraries, run:
```bash
pip install pandas numpy nltk yfinance scikit-learn xgboost matplotlib transformers
