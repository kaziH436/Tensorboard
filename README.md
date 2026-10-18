# Tensorboard
[Tensorboard Introduction | Deep Learning Tutorial 16 (Tensorflow2.0, Keras & Python)](https://www.youtube.com/watch?v=9SdLOcGnebU&list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&index=17)


Notes from [Convolution padding and stride | Deep Learning Tutorial 25 (Tensorflow2.0, Keras & Python)](https://www.youtube.com/watch?v=oDAPkZ53zKk&list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&index=26)
## Reducing the input size using Valid Convolution
Loopy pattern filter: (m-f+1)*(n-f+1)
Vertical line filter 
diagonal line filter 

### Disadvantages
The corner pixels don't play an important role in feature detection

- Convolution padding: pad such that output is same as input

- Stride: moving a window around the image


Image classification: putting images in certain classes 

Image Classification with localization: putting objects in the image in certain classes while identifying where the object is located in the image

Object Detection: If there is multiple objects in the image, making the bounding boxes arund the objects and identifying it is object detection

Sliding window object detection: keeping moving the window to understand if there is a dog or not. The window size is the size of the object

- Disadvantages: too much computation 
- R CNN: trying CNN 
- Fast R CNN 
- faster R CNN 
- YOLO

Image segmentation (instance): classifying the pixels of each object in a image

## RNN (recurrent neural network)

### Usecases
The sequence matters 
- Autocomplete
- Translation
- NER 
- Sentiment Analysis

[What is Recurrent Neural Network (RNN)? Deep Learning Tutorial 33 (Tensorflow, Keras & Python)](https://www.youtube.com/watch?v=Y2wfIKQyd1I&list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&index=33)

### ANN disadvantages 
- fixed neural size is a problem, input and output size might change
- Too much computation
- Parameters are not shared?
- The sequence matters to the meaning of the words

## Types of RNN
Many inputs and many outputs in translation 
Many to one: parameter as input and output is 1 (review) in sentinent analysis 
one to many: music notes 

## Vanishing and Exploding Gradients
Vanishing Gradients: If the gradient is the multiplication of small gradients, the resulting gradient is smaller and that would make the training process slow

Exploding Gradients: If the gradient is the multiplication of large gradients, the resulting gradient is larger and that would make the training process fast

### Vanishing problem in RNN
In translations, the input is passed in and the impact of the earlier words reduces, causing short memory and maybe it will forgot the "first words"

### Solutions 
#### LSTM (training phase)
In the memory cell, there is a cell state (long term memory) and a hidden state (short term memory)

Keywords are stored in the long term memory for prediction. 
The memory is thrown out if a new keyword is introduced.  (gates help to do this)

#### GRU
This only has 2 gates: update gate and reset gate
Update gate: how much of past memory to retain 
Reset Gate: how much of past memory to forget
- Combines short term and long term in one 
- more efficient than LSTM

## Bi-directional RNN
for a forward RNN: the prediction is only influenced by previous words (inputs, hidden layers, predictions, loss, backpropagation to adjust the weights for words and that input sentence)
for bi-directional: there is another layer to go another way