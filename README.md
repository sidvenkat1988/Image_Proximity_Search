# Image_Proximity_Search

This is a repository in which I tried to perform an image proximity search on the CIFAR-10 dataset, which was done as a part of my Data Management assignment at my university. This action was performed on the basis of:

	1) Feature extraction using Autoencoders and
	2) Performing a similarity metrics using either Cosine Similarity or Euclidean Distance.


Three different autoencoding methods were implemented, namely:

	1) Deep Autoencoders
	2) Denoising Autoencoders and
	3) Convolutional Autoencoders

The following activation, optimizers and loss functions were used:
	
	1) Activation - ReLU for the hidden layers, Sigmoid or Tanh for the output layers
	2) Optimizers - Adam or Adadelta
	3) Loss Functions - Binary Crossentropy or Mean Squared Error

There were a total of 8 different combinations of the aforementioned functions used on each Autoencoder, as a result of which there were a total of 24 different models that were implemented.

Each of the Jupyter Notebooks containing the model implementations have the following naming convention:

	"Autoencoder_Type Functions_Combination.ipynb"

The combinations are abbreviated as follows, the names with which the Jupyter notebooks also end:

	1) RSAM -> ReLU-Sigmoid-Adam-MeanSquaredError
	2) RSAB -> ReLU-Sigmoid-Adam-BinaryCrossEntropy
	3) RTAM -> ReLU-Tanh-Adam-MeanSquaredError
	4) RTAB -> ReLU-Tanh-Adam-BinaryCrossEntropy
	5) RSADM -> ReLU-Sigmoid-Adadelta-MeanSquaredError
	6) RSADB -> ReLU-Sigmoid-Adadelta-BinaryCrossEntropy
	7) RTADM -> ReLU-Tanh-Adadelta-MeanSquaredError	
	8) RTADB -> ReLU-Tanh-Adadelta-BinaryCrossEntropy

The link to the files is as follows:
https://drive.google.com/drive/folders/14nRSWhyqHHGUntUpyiNNcToLRD504P2i?usp=sharing

In the above link:
	1) The Raw_Data folder contains the RGB and the Gray pixeled feature vectors of each image of the CIFAR-10 dataset and
	2) The remaining folders contain the encoded feature vectors extracted from each model.

The raw data was downloaded using Keras datasets function and was exported as flat-files using Pandas. This was done in order to create an instance of an Hybrid OLAP Data Warehousing technique in my system. This process is shown in the 'Fetching the data.ipynb' notebook.

The 'Demo.ipynb' notebook can be run on the encoded feature vectors in the remaining data folders. 

Considering the fact that I'm new to the world of Deep Learning, the results aren't all that great. With better knowledge on different optimisation functions, hyper parameters etc. I should hopefully be able to train better models. 