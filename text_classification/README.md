# Text Classification

## Introduction
This is a Machine learning model built using TensorFlow and Keras. When users input
a text file or a string for a review(games/movies). The model predict if the user
intended for the review to be a good or bad review.

Try it out at https://neville-loh.github.io/tf_start.html !

### Online model
To Try out the model, enter any text in the text boxes up to 250 words. The longer the description the better the result.
The model will predict if your text are good or bad. 

A score is given from 0 to 100, 100 means your text is postive, as if the content 

To see the actual value the model predicted. Right-click and inspect the element.
The value is logged in the browser console. A 1 means a very positive review, and a 0 means a very negative review.


### Running the model locally
```
# Requires the latest pip
pip install --upgrade pip

# Current stable release for CPU and GPU
pip install tensorflow

pip install numpy
```

## Result:



## Neural network design
![](./img/layer.png)

The first input layer allows up to 250 words to be input. The data is padded to
match the input requirement if the text have less than 250 words. The input words
will be parse into a integer value that represent the words.  

The second layer is the embedded layer which build association in terms of word
vector. Each word is mapped to one vector and the vector values are learned in a way that
resembles a neural network. The batch is 10000, and the dimension in this layer is set to 16.


The third layer is use to concatenate the embedded layer into lower dimension so it
can be fed into the model



The output layer is chosen to be sigmodal like, this allows are prediction lies
close to either a good review or a bad review, avoiding ambiguity. The output is
between 0 and 1.


## Training the model:


## Future improvement
Natural language processing like these can be deployed inside email or chat system to identify harresment messages. For example, similar model can help tackle the problem of school bully or workplace harresment.
