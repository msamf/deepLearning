# Classifying Microscopic Histopathology Images with Pytorch
This project classifies images as cancerous or normal, using computer vision and CNN via pytorch. 
NOTE: This project is based on Codecademy's [Image Classification with Pytorch](https://www.codecademy.com/paths/build-deep-learning-models-pytorch/tracks/pytorch-sp-image-classification-with-pytorch/modules/pytorch-sp-mod-image-classification-with-pytorch/projects/classifying-microscopic-histopathology-images-with-py-torch-v-2).

## Dataset
The dataset is called [PatchCamelyon (PCAM)](https://github.com/basveeling/pcam), and comprises 96x96 image sections taken from images of lymph node sections. Each image is labeled as tumor (1) or normal (0). A small subset of the data is used, and loaded images using a provided custom PCamDataset class.

## Methods
The following steps are taken:
* Importing data with transformation and augmentation pipelines (loaded in batches)
    * Training set: resize; random flips, rotations, color jitters; converstion to tensor; normalization
    * Validation and testing set: resize; conversion to tensor; normalization
* Creating CNN (3 convolution layers, 3 maxpooling layers, two fully connected layers)
* Training CNN 
* Evaluating CNN

## Results and Discussion
The CNN achieved an overall accuracy of 81% and f-score of 81%. This is a relatively strong result, although this is room for improvement. 

Some potential next steps include:
* Exploring effect of CNN architecture on accuracy (e.g. adding additional layers, hyperparameter tuning of layers including kernel size/padding/stride, etc)
* Exploring effect of learning rate
* Comparing with other algorithms 
* As this is a medical project as well, it may be more critical to catch all tumours i.e. aiming for high recall