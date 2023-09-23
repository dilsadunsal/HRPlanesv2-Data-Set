# HRPlanesv2 Data Set - High Resolution Satellite Imagery for Aircraft Detection

This repository contains the details of the HRPlanesv2 high-resolution satellite imagery dataset for aircraft detection, created for use in [Dilsad Unsal's](https://www.linkedin.com/in/dilsad-unsal-b4a1101bb/) master's thesis, as well as the benchmark results of experiments using YOLOv4, YOLOv5, and YOLOv8, along with the associated weight files.
 
Researchers who are interested can directly download the weight files from the experiments and access the dataset using the provided [Zenodo Link](https://zenodo.org/record/7331974#.Y3dUlXZByUk).

This dataset is also published on the IEEE Earth Observation Dataset Platform, accessible via the following [Link](https://eod-grss-ieee.com/dataset-detail/ak1BclhJbkpuUkh5Uitmd3B5L2hNQT09).



## <div align="left">Details About the Experiments</div>

YOLOv4 training experiments were conducted using the Darknet open-source neural network framework (https://github.com/pjreddie/darknet) on a computer equipped with an NVIDIA GeForce 2080 Ti graphics card.

YOLOv5 training experiments were conducted on the Google Colab platform using a notebook cloned from the following link: https://github.com/ultralytics/yolov5.

For YOLOv5, the developers recommend experiments between 300 and 1000 epochs. However the HRPlanesv2 is a large dataset that consists of high-resolution Google Earth images. Therefore, the YOLOv5 experiments have been realized as six different experiments, each consisting of 50 epochs.

YOLOv8 training experiments were conducted using the Google Colab notebook cloned from the Roboflow platform, accessed via the link https://colab.research.google.com/github/roboflow-ai/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb.

## <div align="left">Details About the Dataset</div>

The HRPlanesv2 dataset has been created in two steps. First,  [HRPlanes](https://github.com/TolgaBkm/HRPlanes) dataset refined by eliminating half of the images. Remaining half consists images with clear wheather conditions and high object percentage. Secondly, to further improve experiment results, images of airports from many different regions with various uses (civil/military/joint) selected and labeled.
 
The HRPlanesv2 dataset contains 2120 very high-resolution Google Earth images, with a total of 14335 aircraft labeled.

Each image is stored as a "**.jpg**" file with dimensions of 4800 x 2703 pixels, and each label is saved in YOLO "**.txt**" format.


The dataset has been divided into three parts: 70% for training, 20% for validation, and 10% for testing. The aircraft in the images within the training and validation datasets are 80% or larger in size.




![graph3](https://github.com/dilsadunsal/HRPlanesv2-Data-Set/assets/77750296/819a5d97-680d-46e6-bbc9-6575451d81c7)







## <div align="left">Image Samples</div>


![Picture2](https://user-images.githubusercontent.com/77750296/153885017-78632f3c-0a35-4720-ae7d-92bddfc9c489.jpg)


</div>

## <div align="left">Benchmark Analysis and Weight Files</div>

The mAP results from experiments with different input sizes are given in the table below. Researchers could download the weight files directly from the links on the table.


| Model              | Patch   Size | P | R | mAP @.50| mAP @.50:.05:.95 | Optimizer | Weights |
|:--------------------------:|:------------------:|-------------------------:|-------------------------:|-------------------------:|-------------------------:|-------------------------:|-------------------------:|
|YOLOv8-nano                         | 640x640                | 0.972                      | 0.962                      | 0.987                      | 0.758                      |SGD                         |[yolov8_nano_SGD_best.pt](https://drive.google.com/file/d/1DTQ7I1NJgzmWnhIOXY0g6ISgA5iihQJh/view?usp=drive_link)                  |
|YOLOv4                         | 576x576                | 0.97                      | 0.99                      | 0.988                      | 0.760                      |N/A                         | [yolov4_best.conv.137](https://drive.google.com/file/d/1ed8JjQltaRCQ3ZF2wPNc3tToR1CDP4rX/view?usp=sharing)                  |
|YOLOv8-nano                         | 640x640                 | 0.978                      | 0.967                      | 0.988                      | 0.781                     |Adam                         | [yolov8_nano_adam_best.pt](https://drive.google.com/file/d/1ag5bblMu0JyjrjGbHuSIRWezTD-XpST0/view?usp=drive_link)                     |
|YOLOv5X                         | 576x576                 | 0.994                      | 0.996                      | 0.992                      | 0.802                      |SGD                         | [yolov5_576_best.pt](https://drive.google.com/file/d/1QsLOXON89D2h_ck67YOKrqUsWRl4U_Mj/view?usp=sharing)                 |
|YOLOv8X                         | 640x640                 | 0.979                      | 0.976                      | 0.991                      | 0.807                     |Adam                         | [yolov8X_adam_best.pt](https://drive.google.com/file/d/1IZIlKb1TLvShaLSXekZ0zXNCHv_A-Na1/view?usp=drive_link)                     |
|YOLOv5X                         | 640x640                 | 0.996                      | 0.99                      | 0.995                      | 0.815                     |SGD                         | [yolov5_640_best.pt](https://drive.google.com/file/d/1W3M-mnhyA8i75UCxfddSWQEs8jM-nMom/view?usp=sharing)                     |
|YOLOv8-large                         | 640x640                 | 0.981                      | 0.977                      | 0.991                      | 0.816                    |Adam                         | [yolov8_large_adam_best.pt](https://drive.google.com/file/d/10WA-ZbCC6DpB2mo0L0EtCSpH2bDswPL2/view?usp=drive_link)                     |
|YOLOv8-large                         | 640x640                 | 0.990                      | 0.985                      | 0.993                      | **0.835**                     |SGD                         | [yolov8_large_SGD_best.pt](https://drive.google.com/file/d/1abKPIVrEIXXjI8jpRVn0oK0bYeQIAIpA/view?usp=drive_link)                     |SGD                         |
|YOLOv8X                         | 640x640                 | 0.992                      | 0.979                      | 0.993                      | **0.838**                     |SGD                         | [yolov8X_SGD_best.pt](https://drive.google.com/file/d/14sOvN1kDjsw5jlEqycbVCz03Nm9-KH6z/view?usp=drive_link)                     |


## <div align="left">License</div>

Use of the Google Earth images must respect the ["Google Earth" terms of use](https://about.google/brand-resource-center/products-and-services/geo-guidelines/).
All images and their associated annotations can be used for academic purposes only,
<font color="red"><b> but any commercial use is prohibited.</b></font>

Released under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/)




## <div align="left">Citation</div>


People who want to use the dataset should give DOI citation on the Zenodo page.

"Unsal, Dilsad. (2022). HRPlanesv2 - High Resolution Satellite Imagery for Aircraft Detection [Data set]. Zenodo. https://doi.org/10.5281/zenodo.7331974"

Citation Link for HRPlanes [publication link](https://dergipark.org.tr/en/pub/ijeg/issue/77206/1107890)
