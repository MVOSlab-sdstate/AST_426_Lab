<h1 style="font-family: Georgia;">AST 426L: Technology Applications for Precision Agriculture</h1>
<p style="font-family: Georgia;"><strong>Instructor:</strong> Dr. Pappu Kumar Yadav</p>

# Lab 9: Nitrogen Application Prescription Map Generation

## Overview


Precision agriculture leverages satellite and sensor data to enable targeted management
practices that increase efficiency and reduce environmental impact. One key approach is using
prescription maps, which guide variable-rate application of inputs like nitrogen fertilizer.
By aligning the amount applied with the soil’s current nutrient availability, prescription
maps help prevent over-application, reduce waste, and mitigate the risk of nutrient runoff.
In recent years, the availability of high-resolution satellite data from sources such as Sentinel-
2 has made it feasible to monitor crop health and soil conditions across entire fields. This data
can then be analyzed to determine zones within the field that require different levels of inputs
based on indicators such as vegetation indices.

Among these indices, the Normalized Difference Red Edge (NDRE) index is particularly
valuable for assessing soil nitrogen availability. Derived from Sentinel-2's red-edge bands,
NDRE provides insight into the crop's nitrogen status by detecting subtle variations in
chlorophyll content that reflect nitrogen levels. This makes NDRE a robust tool for
generating nitrogen application maps that recommend precise amounts of fertilizer
based on need. Using Google Earth Engine, NDRE can be calculated across a farm area, and
through additional analysis, distinct zones within the field can be color-coded according to
nitrogen requirements.

This lab exercise guides students through the process of generating a prescription map using
Google Earth Engine and Google Colab. By providing top-left and bottom-right GPS
coordinates, students can define an area of interest (farm allocated to your lab group from
previous exercises), calculate NDRE values, and create a visual map indicating
recommended nitrogen application rates. This hands-on experience not only demonstrates
the practical application of satellite data in agriculture but also teaches key skills in geospatial
data processing and analysis, which are essential for modern precision farming practices.


## Technical Background


### Prescription Map
A prescription map is a geospatial tool used in precision agriculture to guide the variable-
rate application of agricultural inputs, such as fertilizers, pesticides, or water. Unlike
traditional uniform application methods, prescription maps divide a field into management
zones, each with specific input requirements based on data-driven insights. These maps are
typically generated using indices derived from satellite or sensor data, such as the
Normalized Difference Vegetation Index (NDVI) or Normalized Difference Red Edge
(NDRE), which reflect the health and nutrient status of crops. By interpreting these indices,
farmers can create maps that assign different rates of input across zones, tailoring
applications to the field’s needs. This approach enhances resource efficiency, reduces input
costs, and minimizes environmental impacts, as nutrients are applied precisely where they
are needed, helping to prevent runoff and nutrient leaching.

### Variable Rate Technology (VRT)
Variable rate technology (VRT) is an advanced approach in precision agriculture that
enables the application of inputs, such as nitrogen fertilizer, at varying rates across a field
rather than a uniform rate. Using data from sources like prescription maps, VRT
equipment can adjust application levels based on the specific requirements of different
field zones. In the case of a nitrogen prescription map, which is generated based on indices
like NDRE that indicate nitrogen availability, each area of the field is assigned a
recommended nitrogen rate. The VRT-enabled equipment, connected to GPS, follows the
map and precisely applies the specified nitrogen rates to each zone. This method optimizes
nutrient use, ensures that plants receive only what they need for optimal growth, and
minimizes the risk of excess fertilizer leaching into the environment. By using nitrogen
prescription maps with VRT, farmers can achieve more sustainable and cost-effective crop
management while improving crop yields and reducing environmental impact.

### Normalized Difference Red-Edge Index (NDRE) for Soil Nitrogen Estimate
The Normalized Difference Red Edge (NDRE) index is a vegetation index commonly used
in precision agriculture to estimate the nitrogen content in soils indirectly through the
nitrogen status of plants. NDRE is derived from red-edge spectral bands, which capture
subtle changes in chlorophyll levels associated with nitrogen content. Unlike indices like
NDVI, which use visible and near-infrared bands, NDRE utilizes the red-edge region of the spectrum, making it highly sensitive to variations in leaf chlorophyll. This sensitivity allows
NDRE to effectively monitor nitrogen availability, particularly in later stages of crop growth
when vegetation is denser. By analyzing NDRE values across a field, agricultural managers
can identify areas with different nitrogen levels, guiding targeted fertilizer applications.
Higher NDRE values typically indicate healthier, nitrogen-rich areas, while lower values
suggest nitrogen deficiencies, making NDRE a valuable tool for generating nitrogen
prescription maps that help optimize fertilizer application for improved crop health and yield.
In this lab, NDRE will be used as a proxy to estimate soil nitrogen availability by
assessing the nitrogen status of the crop canopy, which reflects the nitrogen content in
the soil. The Normalized Difference Red Edge (NDRE) index leverages specific red-edge
bands in Sentinel-2 satellite imagery, which are highly sensitive to chlorophyll variations
related to nitrogen. Since nitrogen is an essential component of chlorophyll, the NDRE index
serves as an indirect indicator of nitrogen levels within plants. When crops have adequate
nitrogen from the soil, chlorophyll production is higher, leading to stronger NDRE
signals. Conversely, areas showing lower NDRE values suggest limited chlorophyll and,
therefore, potential soil nitrogen deficiencies. By mapping NDRE values across a field,
regions can be categorized according to nitrogen availability. These zones are then
translated into nitrogen application rates, with higher applications recommended for
zones with lower NDRE values, ensuring that deficient areas receive the necessary
nutrients. This NDRE-based soil nitrogen availability map provides actionable insights for
generating a precise nitrogen prescription map tailored to the field’s nutrient needs.


## Objectives


1. To use Sentinel 2 satellite data to generate NDRE map and then use it to generate soil
nitrogen availability map of a farm.
2. To use the soil nitrogen availability map to generate prescription map for variable rate
application of nitrogen fertilizer in the farm.


## Experimental Steps and Procedure


### Experiment 1: Generate Soil Nitrogen Availability Map of a Farm

#### Procedure:

1. Use the following link to open the Colab Notebook and then make a copy of it, give
the notebook a name with your lab group section and number.
https://colab.research.google.com/drive/1SOi7-fIVhFzClTdjYwtsOJiBwbKJ2F_N?usp=sharing
2. Follow the steps and run the code cells to generate outputs. Make sure to make
necessary changes as instructed like changing the top-left and bottom-right GPS
coordinates of the farm, allocated to your lab group from previous experiments.
3. Save all the generated outputs and include in your lab report.


### Experiment 2: Generate Nitrogen Application Prescription Map for Variable Rate Application

#### Procedure:

1. Continue following the later steps of the Colab notebook and generate the
prescription map.
2. The prescription map also gets saved in your google drive in .TIF format. If you
know how to use ArcGIS Pro, then you can open the downloaded prescription map
there. 
3. In the final step you should generate legends that describes nitrogen application
rates corresponding to the color code of the prescription map. 
4. Save all the generated outputs and include them in your lab report. Make sure to
discuss the generated output results based on your farm, cropping system, etc. 


### Experiment 3: Generate Nitrogen Application Prescription Maps for different cloud coverage

#### Procedure

1. Repeat the above steps for different cloud coverage percentages : 0%, 10%, 30%
and 50% and generate and save the generated nitrogen application prescription
maps.
2. Make sure to compare and discuss the influence of cloud coverage on your satellite
data, NDRE values and nitrogen application prescription maps.
3. Submit report.
