Landslide Susceptibility Mapping via 2D CNN 
    
   Status: Active Development (Phase: Data Engineering & Multi-Band Stacking)

Project Overview

This project develops a Convolutional Neural Network (CNN) to predict landslide hazards using Digital Elevation Models (DEMs).
By bypassing traditional GIS software, I’ve engineered a programmatic pipeline in Python to transform raw topographic data into deep-learning-ready tensors.

 Technical Workflow (Pure Python & Cloud-Integrated)
This project utilizes a "Headless" workflow optimized for large-scale raster processing:

Data Management:
Managing multi-gigabyte raster datasets within a cloud-based filesystem (Google Drive/Local).

Spatial Feature Engineering: 
Programmatic Multi-Band Stacking using Rasterio and NumPy. This turns static geography into multi-channel inputs (Slope, Aspect, Elevation).

Normalization Logic: 
Developed custom scaling scripts to normalize elevation values, ensuring optimal gradient flow during the PyTorch training phase.

Architecture (WIP): 
Designing a PyTorch-based CNN to recognize complex geomorphological patterns that precede slope failure.

 Repository Structure
01_Data_Pipeline.ipynb: Filesystem management, data loading from Drive, and initial raster checks.

02_Stacking_and_Normalization.ipynb: The core logic for merging raster bands and scaling values. (Current Milestone)

03_CNN_Model_Draft.ipynb: Initial PyTorch model class and loss function definitions.

Roadmap
[x] Automated data loading from cloud storage.

[x] Multi-band raster stacking (Elevation + Derived terrain features).

[x] Min-Max Normalization for input consistency.

[ ] Implementation of a sliding-window Dataset class for PyTorch.

[ ] Model Training and Performance Evaluation.

Tech Stack
Deep Learning: PyTorch

Geospatial Analytics: Rasterio, GDAL, WBT 

Numerical Processing: NumPy, Pandasm geopandas

Visualization: Matplotlib
