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
