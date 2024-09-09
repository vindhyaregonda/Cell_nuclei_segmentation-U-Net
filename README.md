# U-Net for Cell Nuclei Segmentation

This project implements a U-Net architecture for the segmentation of cell nuclei from microscopy images. The U-Net is a convolutional neural network that is widely used for biomedical image segmentation tasks. 

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [References](#references)

## Project Overview
The goal of this project is to segment the nuclei of cells in microscopy images. Segmentation is a crucial step in many biomedical tasks, as it allows for the identification and quantification of cells in an image. This project uses the U-Net architecture, a popular model for biomedical segmentation.

## Dataset
The dataset consists of microscopy images of cells and their corresponding binary masks, where each mask indicates the location of cell nuclei. The images are preprocessed by resizing them to a fixed size to match the input dimensions expected by the U-Net model.

- **Training images**: Input microscopy images.
- **Training masks**: Binary masks corresponding to the cell nuclei.

## Model Architecture
The U-Net model consists of a contracting path (downsampling) and an expansive path (upsampling). Skip connections are used between corresponding layers in the downsampling and upsampling paths to retain spatial information. This architecture allows for precise localization, making it ideal for segmentation tasks.

### Key Components:
- **Convolutional layers**: Used to extract features from the images.
- **Max pooling**: Reduces the spatial dimensions of the image, allowing the model to capture context.
- **Upsampling layers**: Increase the spatial dimensions, allowing the model to produce output masks with the same dimensions as the input images.
- **Skip connections**: Help retain spatial information that might be lost during downsampling.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repository/unet-cell-segmentation.git
    ```
2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Results
The model is trained for 12 epochs, and early stopping is applied to avoid overfitting. After training, predictions are made on the test set, and sample predictions are visualized for inspection.

## References
- [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597)
- [Kaggle Data Science Bowl 2018 - Cell Segmentation](https://www.kaggle.com/c/data-science-bowl-2018)
