# HRPlanesv2 Data Set - High Resolution Satellite Imagery for Aircraft Detection

This repo contains the details of HRPlanesv2 high resolution satellite imagery for aircraft detection dataset created to be used in [Dilsad Unsal's](https://www.linkedin.com/in/dilsad-unsal-b4a1101bb/) master's thesis and YOLOv4 and YOLOv5 weights trained with that dataset.
 


Researchers who are interested could directly download the weights that give 0.815 mAP as a result of YOLOv5 experiments and 0.760 mAP as a result of YOLOv4 experiments and access the dataset with the [Zenodo Link](https://zenodo.org/record/7331974#.Y3dUlXZByUk).

This dataset also published on the IEEE Earth Observation Dataset Platform with the [Link](https://eod-grss-ieee.com/dataset-detail/ak1BclhJbkpuUkh5Uitmd3B5L2hNQT09).



## <div align="left">Details About Experiments</div>

YOLOv4 trainings have been conducted using Darknet  open source neural network framework (https://github.com/pjreddie/darknet) on a computer with NVIDIA GeForce 2080 Ti graphic card.

YOLOv5 trainings have been conducted on the Google Colab platform on the notebook cloned from the link https://github.com/ultralytics/yolov5.

For YOLOv5, the developers recommend experiments between 300 and 1000 epochs. However the HRPlanesv2 is a large dataset that consists of high-resolution Google Earth images. Therefore, the YOLOv5 experiments have been realized as six different experiments, each consisting of 50 epochs.



## <div align="left">Details About Dataset</div>

The HRPlanesv2 dataset has been created in two steps. First,  [HRPlanes](https://github.com/TolgaBkm/HRPlanes) dataset refined by eliminating half of the images. Remaining half consists images with clear wheather conditions and high object percentage. Secondly, to further improve experiment results, images of airports from many different regions with various uses (civil/military/joint) selected and labeled.

The HRPlanesv2 dataset contains 2120 very high resolution Google Earth images. A total of 14,335 aircrafts have been labelled. 

Each image is stored as a "**.jpg**" file of size 4800 x 2703 pixels and each label is stored as YOLO "**.txt**" format.

Dataset has been split in three parts as 70% train, %20 validation and %10 test. The aircrafts in the images in the train and validation datasets have a percentage of 80 or more in size.  


![hrplanes1](https://user-images.githubusercontent.com/77750296/151970512-3cb16a18-1d9b-42e6-8eb7-ed54b3cd8db3.jpg)

## <div align="left">Image Samples</div>


![Picture2](https://user-images.githubusercontent.com/77750296/153885017-78632f3c-0a35-4720-ae7d-92bddfc9c489.jpg)


</div>

## <div align="left">Benchmark Analysis and Weights</div>

The mAP results from experiments with different input sizes are given in the table below. Researchers could download the weight files directly from the links on the table.


| Model              | Patch   Size | P | R | mAP @.50| mAP @.50:.05:.95 | Weights | Optimizer |
|:--------------------------:|:------------------:|-------------------------:|-------------------------:|-------------------------:|-------------------------:|-------------------------:|-------------------------:|
|YOLOv4                         | 576x576                | 0.97                      | 0.99                      | 0.988                      | 0.760                      | [yolov4_best.conv.137](https://drive.google.com/file/d/1ed8JjQltaRCQ3ZF2wPNc3tToR1CDP4rX/view?usp=sharing)                  |N/A                         |
|YOLOv5                         | 576x576                 | 0.994                      | 0.996                      | 0.992                      | 0.802                      | [yolov5_576_best.pt](https://drive.google.com/file/d/1QsLOXON89D2h_ck67YOKrqUsWRl4U_Mj/view?usp=sharing)                 |SGD                         |
|YOLOv5                         | 640x640                 | 0.996                      | 0.99                      | 0.995                      | **0.815**                     | [yolov5_640_best.pt](https://drive.google.com/file/d/1W3M-mnhyA8i75UCxfddSWQEs8jM-nMom/view?usp=sharing)                     |SGD                         |






## <div align="left">License</div>

Use of the Google Earth images must respect the ["Google Earth" terms of use](https://about.google/brand-resource-center/products-and-services/geo-guidelines/).
All images and their associated annotations can be used for academic purposes only,
<font color="red"><b> but any commercial use is prohibited.</b></font>

Released under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/)

Contact for collaboration:

Thesis Author: [M.Sc. Dilsad Unsal](https://www.linkedin.com/in/dilsad-unsal-b4a1101bb/)

Thesis Advisor: [Prof. Dr. Elif Sertel](https://web.itu.edu.tr/~sertele/) 





## <div align="left">Citation</div>


People who want to use the dataset should give DOI citation on the Zenodo page.

"Unsal, Dilsad. (2022). HRPlanesv2 - High Resolution Satellite Imagery for Aircraft Detection [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7331974"
    
