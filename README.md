# Convulation basics
Each neuron receives some inputs, performs a dot product and optionally follows it with a non-linearity. The whole network still expresses a single differentiable score function: from the raw image pixels on one end to class scores at the other.

## Input image
![capture](https://user-images.githubusercontent.com/23000971/33498854-ee1ad20c-d6f8-11e7-8745-615526769217.JPG)

## Kernal Matrix used:-
[[-1 -1 -1]
 [-1  8 -1]
 [-1 -1 -1]]
 
 ## Output image
 After applying matrix dot product with the image the resulted output image is 
![capture2](https://user-images.githubusercontent.com/23000971/33498872-f9d51418-d6f8-11e7-8191-4ee8944c4a8e.JPG)
 

# Convolutional autoencoders

## Encoder

The encoder consists of three convolutional layers. The number of features changes from 1, the input data, to 16 for the first convolutional layer, then from 16 to 32 for the second layer, and finally, from 32 to 64 for the final convolutional layer.

While transacting from one convolutional layer to another, the shape undergoes an image compression:
![en](https://user-images.githubusercontent.com/23000971/33498625-16bba1f6-d6f8-11e7-9ae6-4e0f87ccbee8.png)

## Decoder

The decoder consists of three deconvolution layers arranged in sequence. For each deconvolution operation, we reduce the number of features to obtain an image that must be the same size as the original image. In addition to reducing the number of features, deconvolution involves a shape transformation of the images:
![de](https://user-images.githubusercontent.com/23000971/33498634-21cd81cc-d6f8-11e7-817a-ea50417ca001.png)


## Complete figure:-
![conv_autoencoder](https://user-images.githubusercontent.com/23000971/33498647-2c8a1274-d6f8-11e7-9768-ee5c80853d88.png)

