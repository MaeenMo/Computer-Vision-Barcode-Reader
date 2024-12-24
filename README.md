# Computer Vision Project

## Overview

This project implements a pipeline for processing and analyzing barcode images using computer vision techniques. The goal is to enhance, clean, and extract useful information from images with various distortions like noise, blur, low contrast, or misalignment.

The implementation leverages Python libraries such as OpenCV, NumPy, and Matplotlib for preprocessing and visualization.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Implementation Details](#implementation-details)
6. [References](#references)

---

## Introduction

Barcodes are widely used for encoding information in a compact, machine-readable format. However, real-world images of barcodes can often be distorted by various factors such as:
- Noise (e.g., salt-and-pepper noise).
- Low contrast or poor lighting conditions.
- Blur caused by motion or defocus.
- Misalignment or rotation.

This project provides a robust solution to preprocess and decode barcodes from such images.

---

## Features

- **Noise Reduction**: Removes salt-and-pepper noise using median and Gaussian filters.
- **Blur Detection and Correction**: Detects blurred images and sharpens them using Laplacian filters.
- **Contrast Enhancement**: Enhances low-contrast images using histogram stretching.
- **Rotation Alignment**: Detects and corrects misaligned images using Hough Transform.
- **Barcode Cropping and Enhancement**: Identifies and isolates the barcode region for further processing.

---

## Installation

To run this project, ensure you have the following dependencies installed:

- Python 3.8 or higher
- OpenCV
- NumPy
- Matplotlib

### Installation Steps

1. Clone this repository:
   ```bash
   git clone https://github.com/MaeenMo/Computer-Vision-Barcode-Reader
2. Navigate to the project directory:
   ```bash
   cd computer-vision-project
3. Install the required Python libraries:
   ```bash
   pip install opencv-python
   pip install matplotlib

## Usage

1. Prepare your barcode image dataset in the Test Cases/ directory.
2. Open the Jupyter Notebook Computer_Vision.ipynb and run the cells sequentially.
3. Adjust hyperparameters such as threshold, kernel_size, and morphological parameters as needed to suit your dataset.

## Implementation Details

### Preprocessing Pipeline

#### Noise Removal
- Applied median filtering to reduce salt-and-pepper noise while preserving barcode edges.
- **Example**:
   ```python
   Filtered_Image = cv2.medianBlur(image, 7)

#### Blur Detection and Correction
- Detected blurred images using the mean absolute difference between the original and blurred versions.
- Sharpened blurred images using the Laplacian filter.

#### Contrast Enhancement
- Enhanced low-contrast images by normalizing pixel intensity using histogram stretching.
- Example:
  ```python
   image = histogram_stretching(image)
#### Rotation Correction
- Detected and corrected misaligned images using the Hough Transform to compute rotation angles.

#### Barcode Cropping and Enhancement
- Isolated the barcode region using contours and morphological operations.
- Example:
  ```python
  kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (1, 200))
  eroded_image = cv2.erode(dilated_image, kernel, iterations=1)

## Notebook Structure

- Phase 1: Image loading and preprocessing.
- Phase 2: Noise removal and blurring.
- Phase 3: Contrast enhancement and thresholding.
- Phase 4: Barcode cropping and enhancement.

## References

- OpenCV Documentation: https://docs.opencv.org
- NumPy Documentation: https://numpy.org/doc/
- Matplotlib Documentation: https://matplotlib.org/stable/contents.html

## Contributors
- Omar Alaa Elnahass
- Abdelrahman Mohamed Barakat
- Maeen Mohamed Sayed
- Tsneam Ahmed Eliwa
