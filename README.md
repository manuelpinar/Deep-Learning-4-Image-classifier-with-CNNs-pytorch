# Image Classifier with PyTorch
Image classifier with pytorch
Google Colab code


This is the code (image classifier_final.ipynb) to classify flower images between 102 classes. The code is for Colab, to can use CUDA through the GPU of Google. The code is structured like follow:

1) Install Pytorch (is necessary install every time with you start your code)
2) Import necessaries libreries
3) Mount our Drive unity (is necessary upload our image folders like validation, test or train folders at google drive) Google Colab works over Google Drive
4) Load and Transform the data (images), to train, validate and pass the images through our Neural Network or Model you must transform before the images.
5) Load in a mapping from category label to category name. With cat_to_name.json
6) Load a pre-trained network from ImageNet framework, in my case I used Densenet121
7) Define a untrained feed-forward network as a classifier, using ReLU activations and dropout, the we need specify the Loss and the Optimizer
8) Attach the untrained FF network to Densenet = Model
9) Train, validate and Test our model (only the part untrained (FF)). I only calculate the accuracy over the validation.
10) Save our model totally trained (checkpoint.pth) Is over 25 Mb isn't uploaded in this repository
11) Load the model trained
Now you'll write a function to use a trained network for inference. That is, you'll pass an image into the network and predict the class of the flower in the image. Write a function called predict that takes an image and a model, then returns the top  K  most likely classes along with the probabilities
12)Take an image of the test or validation folder
13) Process and show the image processed
14) Search the TopK most probable classes
15) Plot the most probable class
