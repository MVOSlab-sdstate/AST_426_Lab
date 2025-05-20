<h1 style="font-family: Georgia;">AST 426L: Technology Applications for Precision Agriculture</h1>
<p style="font-family: Georgia;"><strong>Instructor:</strong> Dr. Pappu Kumar Yadav</p>

# Lab 7: AI for weed detection in corn field

## Overview


Weeds are one of the most significant threats to corn production, leading to reduced yields,
increased production costs, and degraded crop quality. Traditional weed control methods, such
as manual removal and the application of herbicides, are often labor-intensive, costly, and
environmentally damaging. As precision agriculture advances, the integration of artificial
intelligence (AI) and computer vision technologies has shown great potential in transforming
the way farmers detect and manage weeds, leading to more efficient and sustainable practices.
AI-driven weed detection systems utilize advanced machine learning algorithms and deep
learning models to automatically identify and classify weeds within a crop field. In the context
of corn, detecting weeds early is crucial to ensure healthy crop development, as weeds compete
with crops for essential resources such as nutrients, water, and sunlight. By using AI, farmers
can implement site-specific weed management strategies, applying targeted herbicides or other
treatments only to areas that require them, minimizing waste and reducing environmental impact.


One of the most promising approaches to AI-based weed detection is the use of convolutional
neural networks (CNNs), a type of deep learning model that excels in analyzing visual data.
YOLO (You Only Look Once) is a popular object detection algorithm that has demonstrated
exceptional performance in real-time applications. It can identify and localize multiple objects
in an image, making it highly suitable for detecting weeds among corn plants.


In this lab, we will explore how to implement an AI-based object detection system to detect
weeds in corn fields using the YOLOv8 model. By training the model on annotated images of
corn fields containing weeds, students will learn how AI can be leveraged for precision weed
management. The lab will involve training the YOLOv8 model, testing it on real images, and
performing weed detection, which can later be integrated into field-scale precision agriculture
systems.


Through this lab, students will gain hands-on experience in using deep learning techniques for
object detection in agriculture, learning the practical applications of AI for enhancing crop
management and promoting sustainable farming practices.


## Technical Background


### YOLOv8: Real-Time Object Detection
YOLOv8 (You Only Look Once, version 8) is the latest iteration in the YOLO family of
object detection models, known for its speed and accuracy. YOLOv8 builds on the strengths
of previous versions by improving the architecture to achieve better performance in terms of
both precision and inference time. YOLOv8 operates by dividing an image into a grid and
predicting bounding boxes, object classes, and confidence scores simultaneously. This one-
stage detector is highly efficient for real-time applications such as weed detection in
agricultural fields, where quick and accurate decisions are crucial. Its ability to handle
complex environments, such as detecting weeds among dense corn crops, makes it an ideal
choice for AI-based precision agriculture.

### Mean Average Precision (mAP)
Mean Average Precision (mAP) is a widely used metric for evaluating the performance of
object detection models like YOLOv8. mAP measures the model's ability to correctly detect
and localize objects within an image. It is calculated by taking the average precision across all classes and varying levels of Intersection over Union (IoU), which measures the overlap
between predicted and ground truth bounding boxes. A high mAP score indicates that the
model is accurately detecting and localizing objects. In the context of weed detection, mAP
helps quantify how well the model distinguishes between corn plants and weeds, ensuring
effective weed management decisions.

### Precision
Precision is a metric that evaluates the accuracy of the model's predictions by measuring the
proportion of true positive detections (correctly identified weeds) out of all predicted positive
detections (all identified weeds, including false positives). High precision indicates that the
model is highly confident in its predictions and makes few false positive errors. For weed
detection in corn fields, a high precision score means that the model successfully identifies
actual weeds without incorrectly labeling corn plants or other elements in the field as weeds.

### Recall
Recall is another important evaluation metric, focusing on the model's ability to detect all
relevant objects. It is defined as the proportion of true positive detections out of the total
actual objects (weeds) present in the image. High recall means the model is effective in
identifying most, if not all, of the weeds present in a corn field. In precision agriculture, high
recall is crucial for ensuring that weeds do not go undetected, which could otherwise lead to
reduced crop yields. However, recall must be balanced with precision to avoid an excessive
number of false positives.

### Accuracy
Accuracy is a key performance metric that evaluates how well a machine learning model
correctly predicts the outcomes across all classes. In the context of object detection, accuracy
represents the proportion of correct predictions (both true positives and true negatives)
relative to the total number of predictions made by the model. However, for tasks like weed
detection in corn fields, accuracy alone may not provide a complete picture of the model's
performance, especially when dealing with imbalanced datasets where one class (e.g., corn
plants) significantly outnumbers another (e.g., weeds). Despite this, a high accuracy score
indicates that the model is generally effective at distinguishing between weeds and corn
plants, although it should be used in conjunction with other metrics like precision, recall, and
mAP to fully assess the model's capability in real-world scenarios.

### Roboflow: An Annotation Tool for AI Model Training
Roboflow is a popular platform for preparing, annotating, and managing datasets for
computer vision tasks such as object detection, image segmentation, and classification. In
the context of AI and machine learning, annotation refers to the process of labeling images
to indicate the presence and location of objects within them. For object detection tasks,
annotations typically involve drawing bounding boxes around objects of interest (e.g., weeds
in a corn field) and assigning them the correct class labels (e.g., "weed" or "corn"). These
annotated images serve as the ground truth data that a machine learning model, like
YOLOv8, uses to learn and make predictions.

Roboflow simplifies the annotation process by providing an intuitive interface where users
can upload their images, draw bounding boxes, and label objects quickly and accurately.
Additionally, Roboflow supports multiple output formats compatible with various machine
learning frameworks, including YOLOv8, ensuring a smooth workflow from data
preparation to model training. It also provides tools for augmenting datasets (e.g., rotating or
flipping images), which helps improve the model's ability to generalize to new, unseen data.
By using Roboflow, users can efficiently create high-quality datasets, which are crucial for
training robust AI models in precision agriculture applications like weed detection.


## Objectives


1. To learn about Roboflow tool for image annotations.
2. To learn the basics of YOLOv8 for object detection tasks.
3. To train YOLOv8 AI model for detecting weeds in corn fields.
4. To use the trained YOLOv8 AI model for detecting weeds in corn fields on test datasets.


## Experimental Steps and Procedure


### Experiment 1: Roboflow for Image Annotations

#### Procedure:

1. Go to the following website and create an account. https://roboflow.com/
2. Follow the steps as outlined in the code. 
3. Once you reach the step where you need to upload image dataset for annotation, go to
your D2L account and download the zipped folder within “Dataset” directory.
4. After that extract the Zipped folder and then upload all the images to your Roboflow
folder.
5. Then start annotating all the 500 images with two labels: corn, weed. For this treat
anything other than corn as weed.
6. When all the 500 images are annotated, split them into 70% training, 20% validation
and 10% testing.
7. Then Download a zipped folder in YOLOv8 format.
8. Extract the Downloaded file and then upload them on your Google Drive. Make sure
to create a new folder in your Google Drive and give it a name”AST426L_Lab7”. Put
all the files and folders unzipped from Roboflow downloaded zipped folder to this
directory.


### Experiment 2: Train YOLOv8 AI model for weed and corn detection in a corn field

#### Procedure:

1. Open the following Colab Notebook and follow the steps in a sequential manner.
https://colab.research.google.com/drive/14RPROVm9EbMNMHeQJJK02eIr-18N1JgK?usp=sharing
2. Make sure to save all the generated outputs and put in your lab report.
3. Explain all the generated outputs.
4. Submit lab report.
