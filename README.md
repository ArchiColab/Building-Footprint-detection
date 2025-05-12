# Building Footprint detection
Final project for the Building AI course

## Summary
This project aims to detect the building footprint from satellite/aerial images with Mask R-CNN and image matting (KNN matting, closed-form matting and Grabcut). Due to the lack of GIS data in some peripheral areas, this script will generate the simplified building footprints for spatial analysis.

## Background
In underdeveloped areas, the GIS database is limited and not complete. For urban design projects, we use the OpenStreetMap database to access the spatial information. However, the rural structure is unclear and missing all building footprints. On the other hand, Google Map provide the aerial images. This script will detect the building footprint and export the shapefiles for lateral design. 

## How is it used?
Dataset:
You can download the [cropped aerial image tiles and raster labels](https://study.rsgis.whu.edu.cn/pages/download/3.%20The%20cropped%20aerial%20image%20tiles%20and%20raster%20labels.zip) from [WHU Building Dataset](https://study.rsgis.whu.edu.cn/pages/download/building_dataset.html).

From dataset > Convolutional Neural Network > Get the building bounding box and building mask > Local semantic segmentation > High accurate mask > Doughlas Peuker algorithm with polygon constraints > vectorial building footprints.


If you need to resize images, you have to use an HTML tag, like this:
<img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Sleeping_cat_on_her_back.jpg" width="300">

This is how you create code examples:
```
def main():
   countries = ['Denmark', 'Finland', 'Iceland', 'Norway', 'Sweden']
   pop = [5615000, 5439000, 324000, 5080000, 9609000]   # not actually needed in this exercise...
   fishers = [1891, 2652, 3800, 11611, 1757]

   totPop = sum(pop)
   totFish = sum(fishers)

   # write your solution here

   for i in range(len(countries)):
      print("%s %.2f%%" % (countries[i], 100.0))    # current just prints 100%

main()
```


## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
If you need to use links, here's an example:
[Twitter API](https://developer.twitter.com/en/docs)

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
  <br>For example: [Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
* etc
