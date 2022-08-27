# Vehicle-Detection-in-Aerial-Images

## Dataset
* All experiments are performed using the VEDAI dataset, which contains aerial, ortho-normalized imagery from the publicly available Utah AGRC database.
* The original large field-of-view satellite images have been partitioned into images of size 1024 × 1024 and contain a wide diversity of vehicles, backgrounds,
and confuser objects. The imagery is available in three visible color channels and one near infrared channel. While the VEDAI dataset contains 9 classes of
objects, we focus our attention on small vehicles, namely the car and pickupclasses.

## Experiment
* Original VEDAI dataset contains vehicles of 9 classes but here in the experiments we selected vehicles of two classes only- car and pickup. 
* There are 2754 objects of the class 'car'and 1910 objects of the class 'pickup'. VEDAI dataset, which we used in our experiments, contains images of resolution 512x512. We bounded the Vehicle objects in the boxes of resolution of 20x20.
* Original VGG16 model was trained on ImageNet dataset which contains objects of 1000 classes. Model takes images of size 224x224 as input. So we had to resize the images of size 20x20 into size of 224x224.


## Modification in original VGG16 model
* As original VGG16 model takes input size as 224x224 thus we had to resize the 20x20 images into 224x224. Images get blurred by resizing from small pixel size
of 20x20 to a high pixel size of 224x224. So we decided to modify the input to adapt the different size. 
* And this technique worked.
