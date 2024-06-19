# Urban Heat Island Mitigation using AI-Driven Semantic Segmentation of Satellite Imagery

## Overview

This project aims to mitigate the Urban Heat Island (UHI) effect in Arizona by identifying optimal sites for afforestation using AI-driven semantic segmentation of satellite imagery. We leverage high-resolution NAIP satellite images and deep learning techniques to detect vacant lands suitable for developing urban mini forests, which can significantly reduce local temperatures and improve environmental quality.

## Table of Contents

- [Overview](#overview)
- [Data](#data)
- [Model](#model)
- [Results](#results)
- [Acknowledgements](#acknowledgements)

## Data

### Satellite Imagery
- **Source:** National Agriculture Imagery Program (NAIP)
- **Resolution:** 1m
- **Accessed via:** Google Earth Engine

### Temperature Data
- **Source:** Landsat 9
- **Resolution:** 10m
- **Band:** Thermal (ST B10)

### Population Density
- **Source:** WorldPop Global Project
- **Resolution:** 100m
- **Accessed via:** Google Earth Engine

## Model

### Architecture
- **Simple U-Net:** ~58,000 parameters
- **Complex U-Net:** ~4 million parameters

### Data Augmentation
- Rotations, width and height shifts, horizontal and vertical flips

### Training
- **Validation Split:** 10%
- **Testing Split:** 10%

### Performance Metrics
- **IoU (Intersection over Union):**
  - Simple U-Net: 79.7%
  - Complex U-Net: 84.6%

## Results

- Successfully identified optimal vacant lands for afforestation in Mesa, Phoenix, and Paradise Valley.
- Developed an algorithm to prioritize afforestation sites based on temperature and population density.
- Post-processing techniques improved segmentation accuracy by eliminating noise and small fragmented regions.

## Acknowledgements
- Prof. Shanmuganathan Raman, Project Supervisor
- National Agriculture Imagery Program (NAIP)
- Google Earth Engine
- WorldPop Global Project
- Label Studio
