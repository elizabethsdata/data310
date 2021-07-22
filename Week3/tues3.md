# Writeup

## Dataset 

For the custom training model, we used the familiar iris dataset. This dataset is a set of measurements of three different flowers (setosa, virginica, and versicolor). It measures sepal width and length, and petal width and length. We've used this dataset several times before. There are 120 total examples, and each example has four features and one of three possible label names. 

## Creating tf.dataset

I used TensorFlow's make_csv_dataset command to create the tensorflow dataset. This command is used because it is parsing a CSV formatted file. It loads the csv into a format usable for tensorflow, and requires a few parameters to be set. I set batch_size to 32, meaning the set of data used in one iteration of model training will be 32 data points long. I also specified the input data, as read by get_file, and the column/label names. I let tensorflow use the default setting of shuffling the data as well. 

## Model Architecture

Before the model itself, I used tf.stack to pack the features into a single array with the shape (batch size, num_features). The type of model we used is a neural network, or a network of different hidden layers of neurons that take input connections from the previous layers. This model allows for highly complex relationships. The category of neural network used is a dense fully connected neural network. The output of this will be the probability of each type of iris flower. 

To create this model I used the TensorFlow keras API. I created two keras dense layers with 10 nodes each, and an output layer of. 3 nodes (one for each flower). I also specified the input shape of (4,). Each layer used ReLU to create its' output shape of each node. The rules of ReLU are if the input is negative or zero, output is 0, and if input is poisitive, output equals input. The ideal number of layers and neurons depends on the problem and often requires experimentation, but generally more neurons makes a more powerful model, but needs more data to feed it. The functions used in the model are softmax and argmax, with softmax returning the probabilities of reach result, and argmax outputting which it thinks is most likely as the final prediction. 

## Training





