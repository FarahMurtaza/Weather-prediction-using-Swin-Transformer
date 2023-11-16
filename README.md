# Weather Prediction using Swin Transformer

## Overview

This project focuses on predicting weather using the Swin Transformer, a state-of-the-art transformer architecture known for its effectiveness in handling sequential data.

## Data Preprocessing

### File: `dataPreprocess.ipynb`

In the `dataPreprocess.ipynb` notebook, the following steps were taken to prepare the weather data for training:

1. **Read Temperature Data:**
   - Utilized the `netCDF4` library to read the `TempAir.nc` file, extracting crucial temperature data.

2. **Data Dimensions:**
   - Examined the dimensions of the data:
      - Name: 'time', Size: 744
      - Name: 'lon', Size: 720
      - Name: 'lat', Size: 360

3. **Memory Adjustment:**
   - To optimize memory usage, the data was trimmed to:
      - Time: 6 (out of 744)
      - Latitude: 360
      - Longitude: 720
      This resulted in a reduced data size of 1555200.

4. **Data Cleaning:**
   - Employed the MissForest imputation algorithm and a scaler to clean and preprocess the data.

5. **Data Splitting:**
   - The preprocessed data was split into training and testing datasets.

<br>

## Swin Transformer Classes and Functions

### File: `Swin_functiona_and_classes.py`
The `Swin_functiona_and_classes.py` file contains all the classes and functions from the official Swin Transformer. These components are crucial for implementing the Swin Transformer architecture in the context of this weather prediction project.

<br>

## Swin Transformer Implementation

### File: `Swin_transformer.ipynb`

In the `Swin_transformer.ipynb` notebook, I implemented the Swin Transformer model with the following key steps:

1. **Data Representation:**
   - Read the data and generated a 2D array where rows represent latitudes, columns represent longitudes, and the values are the corresponding climate data.
   - Array Size: 360 * 720 = 259200

2. **Patch Embedding:**
   - Utilized the `PatchEmbed` function to generate patches of size 3.
   - Patch Size: 3
   - Total Patches: 28800

3. **Swin Transformer Block:**
   - Applied the Swin Transformer Block, incorporating the window and shifted window technique.
   - Window Size: 6
   - Shift Size: 2

4. **Patch Merging:**
   - Implemented Patch Merging to combine the generated patches.

Feel free to explore the `Swin_transformer.ipynb` notebook for a detailed walkthrough of these steps and gain a deeper understanding of the Swin Transformer model applied to weather prediction.

   


