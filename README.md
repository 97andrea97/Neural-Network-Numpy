# Neural-Network-Numpy
This repo contains 3 independent codes: NN1, NN2, NN3. Where NN1 is the most basic version. NN2 has an implementation of the L2 regularization technique (controlled by the parameter "lmbda"). NN3 has an implementation of the momentum technique (controlled by the parameter "mu").

More info:
NN3 also contains a parameter thought by me, not sufficiently tested yet. The parameter is called "my". It is a multiplicative factor which multiplies the delta error during the backpropagation at each level. The idea is to solve the problem of the vanishing gradient (in this case use my>1) or the exploding gradient(in this case use my<1). If you want ignore this parameter you must SET IT TO ONE!!! NOT TO ZERO!! Suggested value in case of vanishing gradient: between 2-4.

About the datasets:
The code is thought to immediatly try different applications: in this repo there are two datasets, and in the code are generated 2 other datasets. It's possible to change the application by simply changing the parameter "data":

data=0 -> the dataset is a tuple containing pairs: [(1,1),(4,0),(5,1),(6,0)..] where the first element is a number, the second one is the label which is 1 if the number is odd, 0 if the number is even. In this way you can test the network to see how it can classify numbers as even or odds. This is done to show that the result is really bad since we need to encode the number iven as input.

data=1 -> same application of the data=0, but in this case the number is encoded. (the encoding used in the code is really stupid, but that's not the point, is just to show that simply doing an encoding the results are way better).

data=2 -> the dataset is about medical details regarding some patients, used to classify them as probably having some hart disease or not.
More info: https://www.kaggle.com/ronitf/heart-disease-uci

data=3 -> this is the well known MNIST dataset containing the handwritten digits. In order to make faster the code, the dataset has been preprocessed (the typical normalization and the one-hot-encoding of the label, and transformed in a list of pairs), and saved in a numpy array. I only uploaded a really small version of the dataset (1000 samples). To do more exahustive experiments you need to download the dataset and process it.
