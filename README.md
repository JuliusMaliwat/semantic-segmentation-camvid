# CamVid Dataset Segmentation with Deep Learning

## Table of Contents
- [Project Overview](#project-overview)
- [Data](#data)
- [Methodology](#methodology)
- [Results](#results)
- [Repository Structure](#repository-structure)


## Project Overview
This project aims to classify each pixel in urban scene images from the CamVid dataset into predefined classes using deep learning techniques. The primary objective is to explore different model architectures and evaluate their performance in semantic segmentation tasks.

## Data
The CamVid dataset is utilized in this project. It consists of:
- **Total Frames**: 701 labeled frames
- **Resolution**: 720x960 pixels
- **Classes**: 32 distinct classes including cars, pedestrians, trees, roads, etc.
- **Grouped Classes**: 11 broader categories for simplified analysis and comparison with state-of-the-art methods.

## Methodology
The project involves several key steps:
- **Data Preprocessing**: Resizing, normalization, and data augmentation.
- **Exploratory Data Analysis (EDA)**: Understanding the distribution of classes and visual characteristics of the dataset.
- **Model Development**: Building and refining various deep learning models.
- **Training**: Using techniques like early stopping, learning rate scheduling, and model checkpointing.
- **Evaluation**: Assessing model performance using metrics like Mean Intersection over Union (IoU) and accuracy.

## Results
The project achieved notable results in classifying the CamVid dataset:
- **32 Classes Model**:
  - Mean IoU: 43.82%
  - Accuracy: 89.82%
- **11 Classes Model**:
  - Mean IoU: 67.31%
  - Accuracy: 90.98%

## Repository Structure
The repository is organized as follows:
- `1_notebooks/`: Contains Jupyter notebooks for different stages of the project.
  - `1_Exploration.ipynb`: Data exploration and preprocessing.
  - `2_Training_32_classes.ipynb`: Model training for 32 classes.
  - `3_Training_11_classes.ipynb`: Model training for 11 classes.
  - `4_Model_Evaluation_32_classes.ipynb`: Model evaluation for 32 classes.
  - `5_Model_Evaluation_11_classes.ipynb`: Model evaluation for 11 classes.
- `2_test_results/`: Contains test results.
  - `1_32_classes/`: Test results for 32 classes model.
    - `best_model_test_results_32_classes.xlsx`
    - `validation_results_32_classes.xlsx`
  - `2_11_classes/`: Test results for 11 classes model.
    - `best_model_test_results_11_classes.xlsx`
    - `validation_results_11_classes.xlsx`
- `Report.pdf`: Comprehensive project report detailing methodology, experiments, and results.

