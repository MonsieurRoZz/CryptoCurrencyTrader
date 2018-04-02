# CryptoCurrencyTrader
A machine learning program in python to generate cryptocurrency portfolio allocations using machine learning.
The script is inspired by both the pytrader project https://github.com/owocki/pytrader, the following paper https://arxiv.org/abs/1706.10059.

# Disclaimer
The information in this repository is provided for information purposes only. The Information is not intended to be and does not constitute financial advice or any other advice, is general in nature and not specific to you.

## Project Status
I have implemented a working profitable portfolio manager using deep reinforcement learning with a convolutional neural network in Keras. The model learns slowly to ensure generalization and requires a total of > 5E6 training steps for initial training.

I can achieve consistent profitability after fees with the current implementation of the current system, at a number of time offsets, indicating the system is not overfitting.
![Alt text](fitting_example1.png?raw=true "Optional Title")
![Alt text](fitting_example2.png?raw=true "Optional Title")
![Alt text](fitting_example3.png?raw=true "Optional Title")


## Input Data
Minor changes were made to the Poloniex API python wrapper which is inluded in the repository https://github.com/s4w3d0ff/python-poloniex. Data is retrieved via the Poloniex API in OHLC (open, high, low, close) candlestick format along with volume data.
Data can also be provided as .csv files in the unixtime, open, high, low, close format.

### Training Inputs
Open, high, low close prices at a series of prior times are provided to the solver.

## Validation
In order to estimate the amount of overfitting, a series of offset training runs are performed. If the trading strategy is not overfit, fitting should be approximately consistent across at all offsets in terms of profit fraction and fitting error.

#Setup
To run as a standalone script add a file named API_settings.py containing your poloniex API:
poloniex_API_key = ""
poloniex_API_secret = ""

#Requirements 
python >3
pip3 install tensorflow
pip3 install sklearn
pip3 install numpy
pip3 install scipy
pip3 install pandas
pip3 install requests
pip3 install keras

#TO DO
Requirements and setup instructions.


