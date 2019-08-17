# Cover Crop Image Classifier 
This Repository houses the data, code and results for a Machine Learning model that classifies species of cover crops using Tensor Flow.

The repository was updated with the progress made to the neural network model. 

[CCT cover crop Classification](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover_Crop_Classification_CCT_only.ipynb) is a notebook that trains an image classifier to identify a Clover, Canola, or Triticale species of cover crop 

[ORF-out cover crop classificaion](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/CC_classification_ORF_out.ipynb) builds on the last model to train identification of a wider range of cover crop species including mixtures. Oat, Radish and Fallow species are those left out from identification, hence the notebook is labeled ORF-out.

[Covercrop testing](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover_Crop_Classifier_Model_Test.ipynb) is a colab notebook used to evaluate the performance of trained models on new and unused test data.

Logs of data results when conducting model improvement: [model performance](https://github.com/Tim-R413/Cover-Crop-Classification/blob/master/Cover%20Crop%20Classifier%20Model%20Datalog.xlsx)

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
- Made improvement to the dataset creation process. Full images are split into 9s to increase datatset size. 
- Made revisions and produced iterations of model builds to conduct further training runs. All recorded in the Datalog excell sheet. 
- After saving the three highest performing models a separate program notebook was created which takes a desired image and runs it through each model simultaneously then displays their results for performance comparison.

## 7/5/19
- training conducted on 16 x 16 pixel resolution images
- achieved a model training and validation accuracy of over 90%
- When the best performing model was tested with mixed species photos the outcome from the model proved to trouble deciphering between the crop features. 
- Performed different modification strategies in hopes of improving model accuracy. i.e. dramaticallly increased training dataset by spliting full imgaes into 16s instaed of 9s 

## 7/12/19
- After another batch of training runs three model builds showed to have very high performance results, all acheiveing over 95% training and validation accuracy.
- focus is moved to now add support of classification of mixed species.
- new data from the Kepler folder was added and needs preprocessing for incorporation in the project 

## 7/19/19
- Successfully preprocessed new image data for use as new training data and instances of each species were separated to be used as test data.
- Started to build a new model training program that incorporates new species categories (i.e. Pea, 2Spp- mixture, 6Spp-mixture, etc.)
-	After reviewing the new images I decided to leave out Oat, Radish and Fallow species out of the categories that the model will identify. This is because the images for these species had very barren and their features were extremely familiar to each other. 
- The decision to implement a Convolutional neural netwotk design was made after initial training wasnt desirable.
- The CNN model design was also applied to the original model that classified Clover, Canola and Triticale species only. Its performance on the new Kepler data was drastically improved and therefore produced the models ability to generalize data. 

## 7/26/19
- Work was done to and refine the classification model containing the multiple new species but after several runs the training and validation results didn’t seem to show much improvement, showing to not get over around 73% accuracy.
- The focus and objectives of the research project at this pooint were now diverted from image label classification to more advanced, multiclass Image segmentation. 
- New research has begun on implementing pixel wise instance segmentation with the cover crop dataset to identify where the different species of crops are located in an image at the pixel level. 
- A new repository was created to house the progress of that project: https://github.com/Tim-R413/Cover-Crop-Image-Segmentation 
