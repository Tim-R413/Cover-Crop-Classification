# Cover Crop image Classifier 
This Repository houses the data, code and results for a Machine Learning model that classifies species of cover crops using Tensor Flow.

The repository was updated with the progress made to the neural network model. 

[CCT cover crop Classification](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover_Crop_Classification_CCT_only.ipynb) is a notebook that trains an image classifier to identify a Clover, Canola, or Triticale species of cover crop 

[ORF-out cover crop classificaion](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/CC_classification_ORF_out.ipynb) builds on the last model to train identification of a wider range of cover crop species including mixtures. Oat, Radish and Fallow species are those left out from identification, hence the notebook is labeled ORF-out.

[Covercrop testing](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover_Crop_Classifier_Model_Test.ipynb) is a colab notebook used to evaluate the performance of trained models on new and unused test data.

Logs of data results during modek improvement: [logs](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover%20Crop%20Classifier%20Model%20Datalog.xlsx)

The CCT classifier model acheived an accuracy of over 93% and its file can be found [here](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/CCT_covercrop_model), the more advanced classifier model (ORF-out) was not done in performance improvemnt due to a shift of the projects objectives to instance segmentation.

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
- Used tf.Keras to build a simple sequential model to train using the training dataset of 60 images ( a larger dataset will be made in the furture)
- intial training with images of 20 x 20 pixel resolution was used at first 

## 6/24/19:
- Creation of an excell spreadsheet to record data on network runs (i.e. pixel resolution, size of training dataset, number of network layers, activation functions, number of nodes, etc)
- Data will be stored in the [Cover Crop Classsifier Model Datalog](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover%20Crop%20Classifier%20Model%20Datalog.xlsx) 

## 6/28/19

## 7/5/19

## 7/12/19

## 7/19/19

## 7/26/19
