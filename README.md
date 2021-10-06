# Quality Inspection for casting product

## Notebook link
https://www.kaggle.com/sonyd4d/qc-using-cnn/notebook
## Overview
* Defects are an unwanted thing in casting industry. For removing this defective product all industry have their quality inspection department. 
* But,the main problem is this inspection process is carried out manually and it is a very time-consuming process and due to human involvement.
* the results obtained through this method are not 100% accurate. 
* This can because of the rejection of the entire order thus creating a loss for company.

## Objective
To automate this process using machine learning models 

## Dataset
![data](https://user-images.githubusercontent.com/20265851/136126372-f8bc20a9-e358-40f8-9d07-4e22e723039f.png)
* This dataset is of casting manufacturing product.
* Casting is a manufacturing process in which a liquid material is usually poured into a mould, which contains a hollow cavity of the desired shape, and then allowed to solidify.
* Reason for collect this data is casting defects!!
* Casting defect is an undesired irregularity in a metal casting process.
* There are many types of defect in casting like blow holes, pinholes, burr, shrinkage defects, mould material defects, pouring metal defects, metallurgical defects, etc.

## EDA
![pie](https://user-images.githubusercontent.com/20265851/136126404-df70c5e6-36fb-4755-91e4-4752afbade4e.png)

## CNN
    Model: "sequential"
    _________________________________________________________________
    Layer (type)                 Output Shape              Param #   
    =================================================================
    conv2d (Conv2D)              (None, 150, 150, 32)      320       
    _________________________________________________________________
    max_pooling2d (MaxPooling2D) (None, 75, 75, 32)        0         
    _________________________________________________________________
    conv2d_1 (Conv2D)            (None, 38, 38, 64)        18496     
    _________________________________________________________________
    max_pooling2d_1 (MaxPooling2 (None, 19, 19, 64)        0         
    _________________________________________________________________
    flatten (Flatten)            (None, 23104)             0         
    _________________________________________________________________
    dense (Dense)                (None, 128)               2957440   
    _________________________________________________________________
    dense_1 (Dense)              (None, 1)                 129       
    =================================================================
    Total params: 2,976,385
    Trainable params: 2,976,385
    Non-trainable params: 0
    _________________________________________________________________

## Metrices 

### Confusion matrix
![cm](https://user-images.githubusercontent.com/20265851/136126554-b22cb27b-890b-4a90-afae-3dc7d34d7be1.png)

### Loss
![loss](https://user-images.githubusercontent.com/20265851/136126546-839ddd81-46e5-4324-9f2f-f60e28a7f703.png)

### Accuracy
![acc](https://user-images.githubusercontent.com/20265851/136126529-6c40476f-967f-4f38-8fab-7f79d46c4bef.png)


