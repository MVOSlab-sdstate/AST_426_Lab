<h1 style="font-family: Georgia;">AST 426L: Technology Applications for Precision Agriculture</h1>
<p style="font-family: Georgia;"><strong>Instructor:</strong> Dr. Pappu Kumar Yadav</p>

# Lab 6: Analysis of healthy and corn leaf diseases using histogram analysis and machine learning for classification

## Overview

Corn is a critical crop globally, contributing significantly to food security and industrial
applications. However, its productivity is frequently threatened by various diseases, such as
corn blight, common rust, and gray leaf spot, which can severely affect crop health and
yield. Early detection and accurate classification of these diseases play a crucial role in
implementing effective management strategies to mitigate crop loss.
In this lab, we explore the application of machine learning techniques to classify healthy
and diseased corn leaves. By utilizing image processing techniques, specifically histogram
analysis, we can extract useful features from corn leaf images. Histograms capture pixel
intensity distributions, which can highlight differences in texture, color, and disease
patterns across healthy and diseased leaves. These features are then used to train
machine learning models, such as Random Forest and Support Vector Machine (SVM),
to automatically classify corn leaves into four categories: healthy, blight, common rust,
and gray leaf spot. This approach provides an efficient and scalable solution for the automated
detection and classification of crop diseases, supporting farmers and agronomists in monitoring
and managing corn health effectively.

This lab offers hands-on experience in integrating image processing with machine learning to
address a critical challenge in precision agriculture.

## Technical Background

### Histogram Analysis
Histogram analysis is a method for representing the distribution of pixel intensities in an image. It is widely used in image processing to extract meaningful features from images.
By analyzing the histogram of a leaf image, we can identify patterns that differentiate healthy leaves from diseased ones.

### Random Forest
Random Forest is a powerful and versatile machine learning algorithm that belongs to the
family of ensemble learning methods. It operates by constructing multiple decision trees
during training, each trained on different random subsets of the data. The final classification
decision is made by averaging or taking the majority vote of the individual trees. This "forest"
of decision trees helps mitigate the risk of overfitting and improves the model's accuracy and
generalization ability. In the classification of corn leaf diseases, Random Forest excels at
handling the complexity of high-dimensional data such as image features, including
histograms, and produces robust and reliable predictions by aggregating the outputs of
multiple decision trees.

### Support Vector Machine
Support Vector Machine (SVM) is a supervised learning algorithm commonly used for
classification tasks. SVM works by finding the optimal hyperplane that best separates the
data points of different classes in a high-dimensional space. The algorithm focuses on
maximizing the margin between the nearest points from each class, known as support
vectors, to create a clear boundary between categories. SVM is particularly effective when
dealing with complex datasets and is capable of handling both linear and non-linear
classification problems through the use of kernels. In the case of corn leaf disease
classification, SVM helps distinguish between healthy and diseased leaves by learning the
boundary that separates different disease patterns based on the histogram features extracted
from the leaf images.

## Objectives

i. To learn about histogram analysis for healthy and three corn leaf diseases.
ii. To understand the basics of image data preparation for machine learning classifiers.
iii. To train Random Forest (RF) and Support Vector Machine (SVM) classifiers for classifying images of corn leaves as healthy or belonging to three disease categories.
iv. To use the trained RF and SVM classifiers for classifying new test images.

## Experimental Steps and Procedure

### Experiment 1: Histogram Analysis of Corn Leaf Images

#### Procedure:

1. Go to the following website to download the dataset: https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset
2. Extract the downloaded zipped file and then upload on your Google Drive. This can
take 15-20 minutes depending on your internet speed and computer hardware. So
have patience.
3. Now open the following Colab Notebook and make a copy of it in your Google Drive
as you have done in the previous labs. Then name it as per your lab section and
group. Then start making edits and run the codes.
4. Then follow the instructions in the Colab Notebook and generate results. Make sure
to save generated output and put in your Lab report.
5. Make sure to explain the generated results in your lab reports.
6. Submit lab report.

### Experiment 2: Train RF and SVM Classifiers for classification of corn leaf images belonging to healthy and three disease conditions

#### Procedure:

1. Use the steps in the same Colab Notebook and generate the outputs.
2. Make sure to save all the generated outputs and put in your lab report.
3. Explain all the generated outputs.
4. Submit lab report.
