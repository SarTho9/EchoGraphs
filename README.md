work in progress

# EchoGraphs

Overview
-------
EchoGraphs provides a framework for graph-based contour detection for medical ultrasound. 
The repository includes model configurations for
1) predicting the contour of the left ventricle in single ultrasound images
2) predicting two contours of the ED and ES frame and the corresponding EF value for ultrasound sequences with known ED/ES frame
3) predicting the EF values of arbitrary ultrasound sequences alongside with the occurence of ED and ES and the corresponding frames



Paper:


(add overview figure)

(add gif of single frame)

Dataset
-------
refer to echonet, add link and description


Installation
-------
add required libraries

pip install --user .

Usage
-------


## Preprocessing

To preprocess the original echonet data into a format that is readable by the training code provided in this repository, the 40 keypoints are extracted from the csv file and converted into npy file for each annotation together with other meta data like EF, ED/ES frame and the volumes.


## Training

## Interference

## Overiew Configurations


## Cite paper

For more details, see the following paper:
