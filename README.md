# Tensorboard
[Tensorboard Introduction | Deep Learning Tutorial 16 (Tensorflow2.0, Keras & Python)](https://www.youtube.com/watch?v=9SdLOcGnebU&list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&index=17)


Notes from [Convolution padding and stride | Deep Learning Tutorial 25 (Tensorflow2.0, Keras & Python)](https://www.youtube.com/watch?v=oDAPkZ53zKk&list=PLeo1K3hjS3uu7CxAacxVndI4bE_o3BDtO&index=26)
## Reducing the input size using Valid Convolution
Loopy pattern filter: (m-f+1)*(n-f+1)
Vertical line filter 
diagonal line filter 

## Disadvantages
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