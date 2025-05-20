# AST 426L: Technology Applications for Precision Agriculture

<strong> Instructor: </strong> Dr. Pappu Kumar Yadav  

---

## Lab 11: UAS Remote Sensing for Soybean Yield Map Generation

### Overview

Uncrewed Aerial Systems (UAS), commonly known as drones, are transforming precision agriculture by delivering rapid, high-resolution crop data. Equipped with the Parrot Sequoia Multispectral Sensor, UAS platforms capture critical information across spectral bands—green, red, red-edge, and near-infrared (NIR). These bands are vital for calculating vegetation indices such as NDVI and NDRE, which predict crop vigor and productivity. 

In this lab, you will use UAS data to:
- Generate NDVI and NDRE maps.
- Define Regions of Interest (ROIs) to exclude non-crop areas.
- Employ K-Means clustering to classify yield maps into zones, visualize spatial variability, and develop actionable management zones. 

This comprehensive lab introduces cutting-edge tools in precision agriculture to enhance resource efficiency and crop productivity.

---

## Technical Background

### 1. DJI Phantom 4 UAS/Drone
The DJI Phantom 4 is a versatile drone ideal for precision agriculture. With high-precision GPS, advanced stabilization, and compatibility with multispectral sensors, it captures high-resolution images for crop monitoring and yield predictions.

### 2. Parrot Sequoia Multispectral Camera
The Parrot Sequoia sensor captures data in four spectral bands critical for vegetation analysis. Its sunshine sensor ensures accurate radiometric calibration for reliable NDVI and NDRE maps.

### 3. Yield Map
Yield maps visualize crop productivity across fields, integrating vegetation indices with machine learning or regression models to highlight zones of high and low productivity.

### 4. K-Means Clustering
K-Means clustering classifies spatial data into zones with similar characteristics. In this lab, it groups soybean yield data into clusters, enabling actionable management for precision farming.

---

## Objectives

1. Explore the role of UAS in precision agriculture.  
2. Process UAS-collected multispectral data for soybean fields.  
3. Extract vegetation indices (NDVI, NDRE) from multispectral imagery.  
4. Generate and visualize yield maps using UAS data.  
5. Integrate remote sensing data with yield prediction models.

---

## Experimental Steps and Procedure

### Generate NDVI, NDRE Images, and Yield Maps with Variable Zones

1. **Open the Google Colab Notebook**  
   Use the following link:  
   [Colab Notebook](https://colab.research.google.com/drive/1cYV38psHzUiMc9dPnp18w_ibiaNXT1jV?usp=sharing).  
   *Save a copy in your Google Drive. Do not edit the original notebook.*

2. **Download Dataset**  
   - Access D2L and download the four orthomosaic images (red, green, NIR, red-edge) from the “Lab11-Dataset” sub-directory.  
   - Create a directory in Google Drive named `AST426L_Lab11` and upload the images.

3. **Follow Notebook Instructions**  
   - Run each code cell sequentially.  
   - Save copies of all generated outputs at each step.  

4. **Generate Yield Maps**  
   - Produce yield maps using both NDVI and NDRE indices.  
   - Perform a comparative analysis and include this in your lab report.

5. **Submit Lab Report**  
   - Include a shareable link to your Colab Notebook in the report.  

---

## Deliverables

- NDVI and NDRE yield maps for soybean fields.  
- ROI-defined maps excluding non-crop regions.  
- K-Means clustered yield zones for actionable insights.  
- Lab report with comparative analysis and Colab link.

---

This README serves as a guide for Lab 11, ensuring clarity and structure for successful completion of the lab objectives.
