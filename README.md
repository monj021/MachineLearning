# MachineLearning
Image Classification with Convolutional Neural Networks (CNN)
Problem 1: Dogs vs. Cats dataset will be used as image dataset which you can download from www.kaggle.com/c/dogs-vs-cats/data (you need to make a registration). It contains 25,000 images of dogs and cats (12,500 from each class). For your CNN you will be using only 4,000 pictures of cats and dogs (2,000 cats, 2,000 dogs). Split the set in the following way: 2,000 pictures for training; 1,000 for validation, and 1,000 for testing.
a) Download the original dataset and create a new one containing three subsets: a training set with 1,000 samples of each class, a validation set with 500 samples of each class, and a test set with 500 samples of each class.
b) Use Sequential model and build the topology of your CNN implementing augmentation by including four convolutional layers Conv2D (with Relu activation), four MaxPooling2D layers and a Dense layer of size 1 and a sigmoid activation as the number of classes is two. Use RMSprop optimizer.
c) Display some randomly augmented images (four images of two different cats and four images of two different dogs).
d) To avoid overfitting add Dropout layer and do the training of your CNN using data- augmentation generators. Plot training and validation accuracy as well as training and validation loss.
e) Visualize every channel in every intermediate activations and explain why this is useful.
f) Visualize convolutional filters: get the gradient of the loss with regard to the input, apply stochastic gradient descent, include a code for filter visualizations and generate a grid of all filter response patterns in a layer.
