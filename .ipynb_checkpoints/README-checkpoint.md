# Deep-learning-for-stock-prediction

Background and motivation *
What is the modelling problem and why is it important?

	We want to explore and report about the latest state of the art deep learning techniques for predicting the stock market. One of the main objectives of finance has been predicting how the stock market evolves and we are curious to observe how different deep learning models can tackle this challenge.

Project objectives *
What are the ultimate goals and how will you evaluate whether these goals are achieved? Note that there could be just one goal

	Benchmark different deep learning models for time series predictions, and optimise the architecture to get the best results.

Raw data *
What data will you use? What are the data sources?
	
	We selected the dow jones index, from January 2010 to January 2020 which gives us data from 20 companies. In total we have 2516 samples for each company, and these features [close, high, low, open, volume, adjClose, adjHigh, adjLow, adjOpen, adjVolume, divCash, splitFactor]. The data has been scraped from this website: https://www.tiingo.com

Data wrangling *
How will you filter and transform the data? Will you create additional features?

	We will compute these technical indicators from the data: moving average, exponential moving average, momentum, Bollinger bands, MACD.

	We will also compute the Fourier transform on the data, which will give us a more accurate idea of the trend of the time series. 

Modelling approaches *
What is your candidate model (ML approach such as feedforward neural network)? What is your benchmark model (simple approach such as linear regression)? Note that you may have more than one candidate model.

	We are planning on using ARIMA as our benchmark model, and then compare it to more complex models such as RNN (but it suffers from vanishing gradient problem, to mitigate it we will clip the gradient), Recurrent Unit (GRU) and Long-Short Term Memory (LSTM). For each model we will perform hyper parameter optimisation, to not overfit we will do regularisation/drop out, and early stopping to optimise the performance. During training we will use an optimiser like ADAM. 


Model evaluation and selection *
How will you evaluate (loss) and select (hyper-parameters) the model?

	For the hyper parameter optimisation we will perform grid search on a set of parameters, together with cross-validation, for the architecture of the Neural Networks. As for the loss function, we are planning on using MSE.

