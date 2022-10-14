# HRPlanesv2 Data Set - High Resolution Satellite Imagery for Aircraft Deteciton

This repo contains the details of HRPlanesv2 high resolution satellite imagery for aircraft detection dataset created to be used in [Dilsad Unsal's](https://www.linkedin.com/in/dilsad-unsal-b4a1101bb/) master's thesis and YOLOv4 and YOLOv5 weights trained with that dataset.
 


Researchers who are interested could directly download the weights that give 0.815 mAP as a result of YOLOv5 experiments and 0.760 mAP as a result of YOLOv4 experiments.

We also would like to share the dataset detailed in this repo with researchers who wishes to collaborate with us.


## <div align="left">Details About Experiments</div>

YOLOv4 trainings have been conducted using Darknet  open source neural network framework (https://github.com/pjreddie/darknet) on a computer with NVIDIA GeForce 2080 Ti graphic card.

YOLOv5 trainings have been conducted on the Google Colab platform on the notebook cloned from the link https://github.com/ultralytics/yolov5.

For YOLOv5, the developers recommend experiments between 300 and 1000 epochs. However the HRPlanesv2 is a large dataset that consists of high-resolution Google Earth images. Therefore, the YOLOv5 experiments have been realized as six different experiments, each consisting of 50 epochs.



## <div align="left">Details About Dataset</div>

The HRPlanesv2 dataset has been created in two steps. First,  [HRPlanes](https://github.com/TolgaBkm/HRPlanes) dataset refined by eliminating half of the images. Remaining half consists images with clear wheather conditions and high object percentage. Secondly, to further improve experiment results, images of airports from many different regions with various uses (civil/military/joint) selected and labeled.

The HRPlanesv2 dataset consists of 2120 satellite images with different sizes all taken from Google Earth. A total of 14,335 aircrafts have been labelled. The size of all images in the dataset is 4800 x 2703 pixels.

All images in the dataset are in "**.jpg**" and labels are in YOLO "**.txt**" format

Dataset has been split in three parts as 70% train, %20 validation and %10 test. The aircrafts in the images in the train and validation datasets have a percentage of 80 or more in size.  

The number of objects in the images containing aircraft samples from various most crowded airports and airbases around the world is shown in the figure below.

![hrplanes1](https://user-images.githubusercontent.com/77750296/151970512-3cb16a18-1d9b-42e6-8eb7-ed54b3cd8db3.jpg)

## <div align="left">Image Samples</div>


![Picture2](https://user-images.githubusercontent.com/77750296/153885017-78632f3c-0a35-4720-ae7d-92bddfc9c489.jpg)


</div>

## <div align="left">Benchmark Analysis and Weights</div>

The mAP results from experiments with different input sizes are given in the table below. Researchers could download the weight files directly from the links on the table.


| Model              | Patch   Size | mAP @.50:.05:.95 | Weights |
|:--------------------------:|:------------------:|-------------------------:|-------------------------:|
|YOLOv4                         | 576x576                | 0.760                      | [yolov4_best.conv.137](https://drive.google.com/file/d/1ed8JjQltaRCQ3ZF2wPNc3tToR1CDP4rX/view?usp=sharing)                  |
|YOLOv5                         | 576x576                 | 0.802                      | [yolov5_576_best.pt](https://drive.google.com/file/d/1QsLOXON89D2h_ck67YOKrqUsWRl4U_Mj/view?usp=sharing)                 |
|YOLOv5                         | 640x640                 | **0.815**                     | [yolov5_640_best.pt](https://drive.google.com/file/d/1W3M-mnhyA8i75UCxfddSWQEs8jM-nMom/view?usp=sharing)                     |






## <div align="left">License</div>

Use of the Google Earth images must respect the ["Google Earth" terms of use](https://about.google/brand-resource-center/products-and-services/geo-guidelines/).
All images and their associated annotations can be used for academic purposes only,
<font color="red"><b> but any commercial use is prohibited.</b></font>

Released under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/)

Contact for collaboration:

Thesis Author: [M.Sc. Dilsad Unsal](https://www.linkedin.com/in/dilsad-unsal-b4a1101bb/)

Thesis Advisor: [Prof. Dr. Elif Sertel](https://web.itu.edu.tr/~sertele/) 





## <div align="left">Citation</div>


    @mastersthesis{deeplearning,
    author   =     {Emine Dilşad Ünsal},
    title    =     {{Aircraft Detection From High Resolution Satellite Images With Convolutional Neural Networks}},
    school   =     {Istanbul Technical University Graduate School},
    address  =     {Istanbul, Turkey},
    year     =     {2021},
    }
    
