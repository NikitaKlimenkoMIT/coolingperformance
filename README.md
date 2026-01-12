# Cooling Performance: Analysis Code and Dataset

This repository contains data and notebooks used to process thermal imagery and extract temperature information from urban tree canopies and their surroundings.The notebooks contain reference to model weights from external sources which are referenced in the scripts. Each notebook correspond to different part of data analysis performed, illustrated with an example of one city. 

---

## Notebooks

#### 1. Assign & Plot Temperature Values (Boston Example)
`1_assign_and_plot_temperature_values_Boston_example.ipynb`
This notebook demonstrates how the collected thermal data was processed to assign temperature values to individual tree crowns and the surrounding urban context.  
It includes steps for loading preprocessed scalebar data, mapping temperature values to image regions, and visualizing spatial temperature distributions across the scene.


#### 2. Plot Temperature Delta (Boston Example)
`2_plot_species_delta_Boston_example.ipynb`
This notebook shows how the processed crown temperature values were visualized


#### 3. Compute Shade Temperature (Boston Example)
`3_assign_temperature_values_shade_Boston_example.ipynb`
This notebook shows how temperature in shade was computed

#### 4.1. Run YOLO
`4.1_run_yolo_Boston_example.ipynb`
This notebook shows a tree object detection pipeline to add tree position bounding boxes to the dataset.
Later, these tree bounding boxes are used to compute the region directly below the tree

#### 4.2. Compute Region Temperature
`4.2_assign_temperature_values_region_tree_Boston_example.ipynb`
This notebook shows the temperature in the region directly below the tree was computed


#### 5. Plot Water Consumption Delta (Boston Example)
`5_plot_species_delta_water_consumption_Boston_example`
This notebook shows how water consumption differences were plotted

---

## Dataset

The dataset is available at:
https://drive.google.com/drive/folders/1vP_dADtvM_g9SVFshW4xq_w5_CAN9l1L?usp=sharing

It contains 4 folders, each corresponding to a city. The corresponding folder contains a CSV file 
that contains rows with thermal-color image pairs as well as all the values extracted during the experiments.
These values can be plotted using notebooks 1 and 5. Note that due to slight differences in data collection organization,
the organization of subfolders is different between cities. Nevertheless, they all feature folders 'ir' (thermal images), 'rgb' (color images) and 'scalebars' (temperature scaling arrays)

---
