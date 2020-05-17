# style_transfer

In this notebook, we’ll recreate a style transfer method that is outlined in the paper, 
Image Style Transfer Using Convolutional Neural Networks, by Gatys in PyTorch.

In this paper, style transfer uses the features found in the 19-layer VGG Network, which
is comprised of a series of convolutional and pooling layers, and a few fully-connected layers.
In the image below, the convolutional layers are named by stack and their order in the stack.
Conv_1_1 is the first convolutional layer that an image is passed through, in the first stack. 
Conv_2_1 is the first convolutional layer in the second stack. The deepest convolutional layer in the network is conv_5_4.

In this notebook, we'll use a pre-trained VGG19 Net to extract content or style features from a passed in image.
We'll then formalize the idea of content and style losses and 
use those to iteratively update our target image until we get a result that we want.
