# Building Footprint detection
Final project for the Building AI course

## Summary
This project aims to detect the building footprint from satellite/aerial images with Mask R-CNN and image matting (KNN matting, closed-form matting and Grabcut). Due to the lack of GIS data in some peripheral areas, this script will generate the simplified building footprints for spatial analysis.

## Background
In underdeveloped areas, the GIS database is limited and not complete. For urban design projects, we use the OpenStreetMap database to access the spatial information. However, the rural structure is unclear and missing all building footprints. On the other hand, Google Map provide the aerial images. This script will detect the building footprint and export the shapefiles for lateral design. 

## How is it used?

From dataset > Convolutional Neural Network > Get the building bounding box and building mask > Local semantic segmentation > High accurate mask > Doughlas Peucker algorithm with polygon constraints > vectorial building footprints.

The Ramer–Douglas–Peucker algorithm, also known as the Douglas–Peucker algorithm and iterative end-point fit algorithm, is an algorithm that decimates a curve composed of line segments to a similar curve with fewer points. It was one of the earliest successful algorithms developed for cartographic generalization. It produces the most accurate generalization, but it is also more time-consuming.
<img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Douglas-Peucker_animated.gif" width="300">

## Data sources and AI methods
Dataset:
You can download the [cropped aerial image tiles and raster labels](https://study.rsgis.whu.edu.cn/pages/download/3.%20The%20cropped%20aerial%20image%20tiles%20and%20raster%20labels.zip) from [WHU Building Dataset](https://study.rsgis.whu.edu.cn/pages/download/building_dataset.html).

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments
* [A method for extracting buildings from remote sensing images based on 3DJA-UNet3+] ((https://www.nature.com/articles/s41598-024-70019-z)) 
