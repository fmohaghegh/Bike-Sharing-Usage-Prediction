# Prediction of Bike Sharing System Usage
This project uses the following software packages and Python libraries:
Python 3.6.1, Numpy 1.4.2, Pandas 0.22, Sklearn 0.16.1, matplotlib 3.1.2, seaborn 0.8.1, Jupyter Notebook 5.4.0.

This data analysis to form a prediction model for the hourly utilization “cnt” of bike sharing data set: https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset. 

To make sure that all attributes contribute to the number of bikes used, I start with plotting the variation of usage vs each attribute. The results show that all attributes affect the usage. However, some of them like year and season are more important than weekdays or working days. I will include all attributes in the analysis. For the prediction, I used the data of the last week as the test set. The rest is the training set.
I believe the best approach to solve this problem is machine learning artificial neural networks because the number of contributing parameters is low, and the training set i.e. the number of hours in big. I constructed an artificial neural network (ANN) with the number of input nodes equal to the affecting attributes. Due to having a small number of 13 input nodes, the number of hidden layers is chosen to be small i.e. three hidden layers with 20, 20, and 2 nodes. Sigmoid activation function for the first layer and leaky relu for the rest of the layers apply the non-linearity. For the training, I used Adams optimization along with mean square error as the loss function.

I obtained impressive results: The mean error between the actual data and the predicted values is 1.05% and the mean absolute deviation is 0.79.
