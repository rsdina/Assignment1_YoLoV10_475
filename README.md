# Dental X-ray Object Detection Project

This project demonstrates a complete workflow for processing, visualizing, and training object detection models on a Dental X-ray dataset. It specifically focuses on the Dental X-ray subset, utilizing COCO-formatted annotations and the ultralytics library for advanced object detection tasks.

## Table of Contents

* Overview

* Key Features

* Environment Setup

* Workflow

* Dataset Structure

* Results and Visualization


## Overview

The primary goal of this notebook is to provide a comprehensive guide for handling dental imaging data. It covers everything from environment configuration and coordinate conversion (normalized COCO to pixel coordinates) to training a YOLO-based model and evaluating its performance.

## Key Features
* **Environment Configuration:** Seamless setup using the ultralytics library.

* **Coordinate Processing:** Converts normalized COCO bounding box coordinates (center x, center y, width, height) into pixel coordinates for visualization.

* **Data Visualization:** Draws colored bounding boxes and class labels onto images using OpenCV for ground truth verification.

* **Persistence:** Automatically organizes processed images and copies corresponding label files into an output directory.

* **Model Training:** Includes training routines and logs final loss values (Box Loss, Class Loss, and Segment Loss) for both training and validation sets.

## Environment Setup
To run this project, you need the following dependencies:

**Python 3.x**

**Ultralytics:** For object detection utilities.

**OpenCV:** For image processing and drawing bounding boxes.

**Matplotlib:** For displaying visualization samples.

**Pandas:** For handling training results and loss logs.

### Install the core library via pip:

pip install -U ultralytics --no-deps

## Workflow
* **Environment Setup:** Installing necessary libraries.

* **Data Organization:** Defining root directories for raw images and labels.

* **Bounding Box Processing:** Iterating through images to convert coordinates and draw annotations.

* **Data Persistence:** Saving the "boxed" images and labels to a structured output directory (e.g., /kaggle/working/dental_xray_boxed).

* **Visualization:** Displaying random samples to verify the accuracy of labels.

* **Training & Evaluation:** Training the model and printing final performance metrics.

## Dataset Structure
The project expects a structured dataset containing:

* **Images:** Dental X-ray images.

* **Labels:** Text files in COCO format containing object classes and normalized bounding box coordinates.

## Results and Visualization
The notebook provides a summary of the training process, including final loss metrics such as:

* Train/Val Box Loss

* Train/Val Class Loss

* Train/Val Segmentation Loss (if applicable)

Sample images with verified bounding boxes are displayed at the end of the processing pipeline to ensure data integrity.
