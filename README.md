# Cover Crop image Classifier 
This Repository houses the data and code for a Machine Learning model that classifies species of cover crops using Tensor Flow.


The repository will be updated in consistency with the progress made to the neural network model. 


# Tools used for Development 
This Machine Learning model will be designed using a standard Python local environmnet as well as on Google Colab. Google Colab is a free Jupyter notebook environment that requires no setup, and runs entirely on the Cloud. Colab has tensorflows API's entirely integrated and is useful in applying Tensorflows GPU abilites.

Both versions of the model will be provided and updated in this repository.


# Project updates, notes and next steps:

## 6/18/19:
- image data preprocessing progress conducted 
- use of the Python Image Library (PIL) was very useful in adjusting the data to be converted into numpy arrays.
- the code developed was able to crop the images, change their resolution and convert to and from greyscale
- the updated progress can be seen in the 'Data Pre-Processing code' folder of the repository
- specific adjustments to the cropping and resolution of the images will need to made

## 6/21/19:
- The Data Pre-processing code was completed and successfully extracts and creates pools of training and testing datasets
- A new function was created to split the full images into multiple seperate images by cropping different sections. function name: image_division
-Used tf.Keras to build a simple sequential model to train using the training dataset of 60 images ( a larger dataset will be made in the furture)
-intial training with images of 20 x 20 pixel resolution was used at first 

## 6/24/19:
- Creation of an excell spreadsheet to record data on network runs (i.e. pixel resolution, size of training dataset, number of network layers, activation functions, number of nodes, etc)
- Data will be sored in the "Run Results" folder of the repository. 
