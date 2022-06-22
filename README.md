work in progress

# EchoGraphs

Overview
-------

Accurate and consistent predictions of echocardiography parameters are important for cardiovascular diagnosis and treatment. In particular, segmentations of the left ventricle can be used to derive ventricular volume,  ejection fraction (EF) and other relevant measurements. This project proposes a new automated method called EchoGraph for predicting ejection fraction and segmenting the left ventricle by detecting anatomical keypoints. Models for direct coordinate regression based on Graph Convolutional Networks (GCNs) are used to detect the keypoints. GCNs can learn to represent the cardiac shape based on local appearance of each keypoint, as well as global spatial and temporal structures of all keypoints combined. We evaluated our model on the EchoNet benchmark dataset. Compared to semantic segmentation, GCNs show accurate segmentation and improvements in robustness and inference run-time. EF is computed simultaneously to segmentations and our method also obtains state-of-the-art ejection fraction estimation.

EchoGraphs provides a framework for graph-based contour detection for medical ultrasound. 
The repository includes model configurations for
1) predicting the contour of the left ventricle in single ultrasound images
2) predicting two contours of the ED and ES frame and the corresponding EF value for ultrasound sequences with known ED/ES frame
3) predicting the EF values of arbitrary ultrasound sequences alongside with the occurence of ED and ES and the corresponding frames

For more details, please refer to:


(add overview figure)

(add gif of single frame)

Dataset
-------
For training and evaluation we used the EchoNet dataset. 
For more information on the dataset please refer to 


Installation
-------

add required libraries

pip install --user .

Usage
-------

## Preprocessing

To preprocess the original echonet data into a format that is readable by the training code provided in this repository, the 40 keypoints are extracted from the csv file and converted into npy file for each annotation together with other meta data like EF, ED/ES frame and the volumes. Some preprocessing functions are taken from the EchoNet repository.


## Training
The training script can be started with various parameters to adjust the model or the hyperparameter.


## Interference
All trained models can be evaluated using the eval.py 

## Overiew Configurations and default parameter
1) Single Frame approach

2) Multi-frame approach with known ED/ES

3) Multi-frame approach with unknown ED/ES

## Cite paper

For more details, see the following paper:
