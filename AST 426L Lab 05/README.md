<h1 style="font-family: Georgia;">AST 426L: Technology Applications for Precision Agriculture</h1>
<p style="font-family: Georgia;"><strong>Instructor:</strong> Dr. Pappu Kumar Yadav</p>

# Lab 5: Using Google Earth Engine and Geemap Python Package on Google Colab for Crop Nitrogen Estimation


## Overview


In modern precision agriculture, satellite imagery and advanced data analysis tools are crucial for monitoring crop health, optimizing inputs, and increasing productivity.
This lab introduces the use of Google Earth Engine (GEE) and the Geemap Python package for analyzing satellite data, specifically tailored for agricultural applications.
GEE is a powerful cloud-based platform that provides access to a vast archive of satellite images, which can be processed and analyzed at scale.
Geemap simplifies the integration of GEE with Python, enabling users to perform spatial analysis and visualization with ease.

In this lab, you will learn the capabilities of GEE and Geemap within Google Colab, a cloud-based environment, to analyze satellite data for agricultural fields.
By the end of this lab, you will learn how to extract and process satellite data for precision agriculture tasks such as monitoring crop growth, estimating nitrogen levels, and creating vegetation indices like NDVI.


## Technical Background


### Linear Regression Model
Linear regression is a fundamental statistical technique used to understand the relationship between two variables, typically one independent (predictor) and one dependent (response).
The model assumes the relationship can be represented by a straight line: y = mx + b, where y is the dependent variable (output or prediction),
x is the independent variable (input), m is the slope of the line, and b is the y-intercept. Linear regression is widely used in predictive modeling for making forecasts or predictions based on known data.

### Crop Nitrogen Uptake
Nitrogen is a critical nutrient for crop growth, playing a central role in photosynthesis, protein synthesis, and overall plant development.
Crops like corn and soybean depend on nitrogen uptake to maximize yield potential. Nitrogen uptake is commonly evaluated using NDVI (Normalized Difference Vegetation Index),
an index based on plant health, which correlates with nitrogen availability. Insufficient nitrogen levels can lead to reduced growth and chlorosis (yellowing of leaves).


## Objectives


1. To learn the basics of Google Earth Engine (GEE) and Geemap Python Package in Google Colab environment.
2. To use Geemap on Google Colab to load Sentinel 2 and Landsat satellite images.
3. To use Sentinel 2 satellite images using Geemap on Google Colab and generate NDVI map of a farm in South Dakota.
4. To use the generated NDVI map of 2-year time period for the estimation of nitrogen uptake by the crop(s) located in the farm.


## Experimental Steps and Procedure


### Experiment 1: Getting used to GEE and Geemap on Google Colab.

#### Procedure:

1. First create your account on Google Earth Engine using the link: https://earthengine.google.com/.
2. Once you are successfully logged in and created a new project, on the top right corner, click your account, then project info and then copy the name of the project info as shown below:
3. After this Open a new Colab notebook and give it a name: AST426L-Lab5-
YourSec-YourGroup#. Then write the following Python scripts in different code
cells as shown. Please make sure to run the code cell in sequential order.
4. In a new code cell add the code and run it.



### Experiment 2: Use Sentinel 2 Satellite data using Geemap on Google Colab and generate NDVI map of a farm in South Dakota and then use it to estimate Nitrogen status of crops.

#### Procedure:

1. Open Google Colan Notebook shared to you using the following link:
https://colab.research.google.com/drive/10TS0lzV5USugNP6AbJk_gquUDRxrz7-
F?usp=sharing
2. Make sure to save a copy of the Notebook in your drive immediately and then
rename the Notebook as in Experiment#1 but add”Exp2” in the name of the
notebook.
3. After you authorize GEE account in the second code cell, try to find GPS coordinates
of the field assigned to your lab section and group during Lab#2. You need to find the
top-left and bottom-right corners coordinates and swap the latitude and longitudes.
Replace this in the third code cell line#2. Then run it and see the output. Make sure to
slide the slider for “ESRI:WorldImagery” basemap to visualize the AOI i.e., your
field.
4. Then continue to run the other code cells and visualize the results. Make sure to move
the slider for basemap to visualize results for your farm.
5. When you reach the code cell “Create Time Series Mean NDVI Values”, try to type
“46” in the last line as shown below and then run the code cell.
6. Then continue to run different code cells sequentially and make sure to save the
results as you get them.
7. In the last step, try to generate a Nitrogen estimate time series graph only for the crop
that exists in your assigned farm. To determine which crop was there visit the USDA
CroplandCROS Database at: https://croplandcros.scinet.usda.gov/. Use the GPS
coordinates of your field to search for the crop on the map.
8. Write a report and explain the time-series estimated Nitrogen status of the crop
located in the farm assigned to your group.
9. Submit lab report and also share your Notebook by providing link to your notebook in
the report.

