# CamVid Dataset Segmentation with Deep Learning

## Project Overview
This project focuses on the semantic segmentation of the CamVid dataset using deep learning techniques. Semantic segmentation involves partitioning an image into segments where each pixel is assigned a label corresponding to a specific object or class. The goal of this project is to accurately classify each pixel in urban scene images into one of several predefined classes, exploring whether traditional models or simplified groupings yield better results.

## Data
We utilized the CamVid dataset, which includes:
- **Origin**: Urban driving scenes.
- **Content**: 701 labeled frames with pixel-wise annotations.
- **Classes**: 32 different classes such as cars, pedestrians, trees, roads, etc.
- **Resolution**: 720x960 pixels.

To facilitate comparison with state-of-the-art methods and reduce model complexity, the 32 classes were also grouped into 11 broader categories.

## Methodology
- **Data Preprocessing**: Involved resizing images, splitting the dataset into training, validation, and test sets, normalization, and data augmentation.
- **Model Development**: Various model architectures were developed, starting from simple autoencoders to more complex models with skip connections and data augmentation.
- **Training Setup**: Models were trained with several hyperparameters, including early stopping, learning rate reduction, and model checkpointing.
- **Evaluation Metrics**: Mean Intersection over Union (IoU) and accuracy were used to evaluate model performance, with special attention to class imbalance.

## Results
The project yielded significant improvements through iterative model enhancements:
- **32 Classes Model**:
  - Mean IoU: 43.82%
  - Accuracy: 89.82%
- **11 Classes Model**:
  - Mean IoU: 67.31%
  - Accuracy: 90.98%

These results demonstrate the effectiveness of our models in accurately classifying urban scene elements.

## Project Structure
- **1_notebooks**: Contains Jupyter notebooks for various stages of the project.
  - `1_Exploration.ipynb`: Data exploration and preprocessing.
  - `2_Training_32_classes.ipynb`: Training the model on all 32 classes.
  - `3_Training_11_classes.ipynb`: Training the model on a simplified set of 11 classes.
  - `4_Model_Evaluation_32_classes.ipynb`: Evaluating the model trained on 32 classes.
  - `5_Model_Evaluation_11_classes.ipynb`: Evaluating the model trained on 11 classes.
- **2_test_results**: Contains the test results for the models.
  - `1_32_classes`: Results for the model trained on 32 classes.
    - `best_model_test_results_32_classes.xlsx`
    - `validation_results_32_classes.xlsx`
  - `2_11_classes`: Results for the model trained on 11 classes.
    - `best_model_test_results_11_classes.xlsx`
    - `validation_results_11_classes.xlsx`
- **Report.pdf**: Detailed project report.

