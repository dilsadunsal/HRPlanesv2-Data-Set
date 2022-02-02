# YOLO Weights of HRPlanesv2 Data Set

This repo contains weights of YOLOv5 and YOLOv4 models trained with HRPlanesv2 high resolution satellite imagery.

We also would like to share the dataset detailed in this repo with researchers who wishes to collaborate with us.

YOLOv4 trainings have been conducted using Darknet  open source neural network framework (https://github.com/pjreddie/darknet) on a computer with NVIDIA GeForce 2080 Ti graphic card.

YOLOv5 trainings have been conducted on the Google Colab platform on the notebook cloned from the link https://github.com/ultralytics/yolov5.

We also provide 

## <div align="left">HRPlanesv2 Data Set</div>
The HRPlanesv2 dataset consists of 2120 satellite images with different sizes all taken from Google Earth.
Dataset is divided in three parts as 70% train, %20 validation and %10 test. The aircrafts in the train and validation data sets have a proportion of 80% and above.  
The number of objects in the images containing aircraft samples from various airports in the world is shown in the figure below.

![hrplanes1](https://user-images.githubusercontent.com/77750296/151970512-3cb16a18-1d9b-42e6-8eb7-ed54b3cd8db3.jpg)

## <div align="left">Image Samples</div>

![hrplanes](https://user-images.githubusercontent.com/77750296/151931228-ab9baf42-9f09-4981-b0c2-125bde5fc36d.jpg)


</div>

## <div align="left">Weights</div>

For training download  weights-file (162 MB): [yolov4_best.conv.137](https://drive.google.com/file/d/1ed8JjQltaRCQ3ZF2wPNc3tToR1CDP4rX/view?usp=sharing) 


## <div align="left">Details</div>
For YOLOv5, the developers recommend experiments between 300 and 1000 epochs. However the HRPlanesv2 is a large dataset that consists of high-resolution Google Earth images. Therefore, the YOLOv5 experiments have been realized as six different experiments, each consisting of 50 epochs.


## <div align="left">License</div>

Use of the Google Earth images must respect the ["Google Earth" terms of use](https://about.google/brand-resource-center/products-and-services/geo-guidelines/).
All images and their associated annotations can be used for academic purposes only,
<font color="red"><b> but any commercial use is prohibited.</b></font>

