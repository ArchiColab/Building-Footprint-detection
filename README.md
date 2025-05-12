# Building Footprint detection
Final project for the Building AI course

## Summary
This project aims to detect building footprints from satellite and aerial images using Mask R-CNN and image matting techniques, including KNN matting, closed-form matting, and Grabcut. In regions with limited GIS data, this script generates simplified building footprints to support spatial analysis.

## Background
In underdeveloped areas, GIS databases are often incomplete or lacking critical spatial data. Urban design projects commonly rely on OpenStreetMap for spatial information, but rural areas frequently lack mapped building footprints. Meanwhile, Google Maps provides aerial imagery. This script detects building footprints from these images and exports shapefiles for urban design applications.

## How is it used?
The process follows these steps:
- Dataset preparation
- Convolutional Neural Network processing
- Extracting building bounding boxes and masks
- Local semantic segmentation
- Refining masks for high accuracy
- Applying the Douglas-Peucker algorithm with polygon constraints
- Generating vector-based building footprints
  
The Ramer–Douglas–Peucker algorithm simplifies a curve composed of line segments, reducing the number of points while preserving the overall shape. Initially developed for cartographic generalization, it offers high accuracy but requires more computational resources.
<img src="https://upload.wikimedia.org/wikipedia/commons/3/30/Douglas-Peucker_animated.gif" width="300">


## Data sources and AI methods
Dataset:
You can download the [cropped aerial image tiles and raster labels](https://study.rsgis.whu.edu.cn/pages/download/3.%20The%20cropped%20aerial%20image%20tiles%20and%20raster%20labels.zip) from [WHU Building Dataset](https://study.rsgis.whu.edu.cn/pages/download/building_dataset.html).

## Challenges
This script represents an initial phase for extracting building footprints. Future work will focus on integrating Graph Neural Networks (GNNs) in urban planning, enabling more advanced spatial analysis. While this script streamlines certain aspects of design projects, further refinement is needed for real-world applications

## What next?
Exploring Urban AI and GNN applications for AI-driven urbanism.

## Acknowledgments
* [A method for extracting buildings from remote sensing images based on 3DJA-UNet3+](https://www.nature.com/articles/s41598-024-70019-z)
* [Foot print detection](https://github.com/chenzhaiyu/footprint-detection)
* [Building rooftop extraction from high resolution aerial images using multiscale global perceptron with spatial context refinement](https://www.nature.com/articles/s41598-025-91206-6?fromPaywallRec=false)

