# Object-Detection-in-Autonomous-Driving-Using-BDD100K-Dataset
Object Detection in Autonomous Driving Using BDD100K Dataset

Final Project Group 9: Object-Detection-in-Autonomous-Driving-Using-BDD100K-Dataset - USD
Dataset.

This project is a part of the AAI-521 course in the Applied Artificial Intelligence Program at the University of San Diego (USD). Project Status: [Completed]

Installation
To use this project, first clone the repo on your device using the below command: git clone (https://github.com/maleal2/Object-Detection-in-Autonomous-Driving-Using-BDD100K-Dataset.git)](https://github.com/maleal2/Object-Detection-in-Autonomous-Driving-Using-BDD100K-Dataset.git)

Project Introduction

This paper presents the implementation and optimization of YOLOv8 for object detection using a custom dataset derived from BDD100K, one of the largest open driving datasets by Berkeley DeepDrive. The dataset includes training and validation subsets with annotations initially in JSON format. Early steps involved analyzing BDD100K’s structure, quantifying annotations, and addressing class imbalances by duplicating data for underrepresented categories like bicycles, motorcycles, trains, and trailers. Augmentation techniques, including horizontal flips, color jitter, random rotations, scaling, and cropping, were applied using the Albumentations library.
A rigorous cross-validation process ensured consistency between annotations and images, resulting in 25,303 training and 6,326 validation images. Annotations were converted into YOLO format while maintaining separate folders for the original and processed data. Challenges, such as invalid bounding boxes from augmentation, were resolved through validation and normalization to preserve data integrity.
Training began with YOLOv8 nano, using 50 epochs, 640-pixel images, and a batch size of 16. Metrics such as F1 scores, precision, recall curves, confusion matrices, and losses were analyzed. Fine-tuning with the YOLOv8 small model included additional data cleaning based on earlier errors, improving dataset reliability through validation and logging. A third training round adjusted hyperparameters, such as learning rate and image size, for further optimization.
Conducted on Google Colab with data stored on Google Drive, the project iteratively addressed challenges like bounding box errors and annotation mismatches. This study highlights best practices for YOLOv8 optimization in autonomous driving, emphasizing data management and model performance. Future work may explore advanced augmentation, regularization techniques, and incorporating weather conditions for a more robust dataset.

Contributors
Maria Leal.

Methods Used
Python, YOLOv8, albumentations, Pytorch

Project Description
Data source: [https://www.kaggle.com/datasets/arashnic/fitbit](https://dl.cv.ethz.ch/bdd100k/data/)

Name of the variables:
pedestrian, car, rider, motorcycle, traffic_light, traffic_sign, bus, bicycle, truck, other_vehicle, train, other_person, trailer

Number of variables: 13

Size of the dataset: 

Validation set: https://dl.cv.ethz.ch/bdd100k/data/100k_images_val.zip , 10,000 files.

Testing set: https://dl.cv.ethz.ch/bdd100k/data/100k_images_test.zip, 20,000 files.

Training set: https://dl.cv.ethz.ch/bdd100k/data/100k_images_train.zip, 70,000 files.

Labels set: https://dl.cv.ethz.ch/bdd100k/data/bdd100k_det_20_labels_trainval.zip
