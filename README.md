Hello World! 

Each trading day on the Nasdaq Stock Exchange concludes with the Nasdaq Closing Cross auction. This process 
establishes the official closing prices for securities listed on the exchange. These closing prices serve as 
key indicators for investors, analysts and other market participants in evaluating the performance of individual 
securities and the market as a whole. The objective of this project is to develop a model capable of predicting 
the closing price movements for hundreds of Nasdaq listed stocks using data from the order book and the closing
auction of the stock. Information from the auction can be used to adjust prices, assess supply and demand dynamics,
and identify trading opportunities.

The dataset that will be used in this project is provided by Optiver, a well-known quantitative trading firm.
It contains historical data for the daily ten minute closing auction on the NASDAQ stock exchange. 

This repository contains two Python notebooks. The "Preprocessing:EDA.ipynb" notebook conducts exploratory data analysis on the Kaggle dataset, preprocesses the data, and engineers potentially useful features. The "lgbm_integrate.ipynb" notebook trains and evaluates a LightGBM model. Following feature generation based on the analysis from "Preprocessing:EDA.ipynb," a LightGBM regressor is trained with 5-fold cross-validation and hyperparameters are fine-tuned. Predictions are then submitted to the Optiver API to assess accuracy with the hidden test set.

On the last iteration of fold 5, the model was able to achieve a MAE score for 4.803. The average MAE across all folds is around 5.831. 
