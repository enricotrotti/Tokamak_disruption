# Tokamak_disruption

## Project Overview

The aim of this project is to build an anomaly detection algorithm that can predict disruptions in a fusion reactor **at least 30 milliseconds in advance**. The dataset required for this task is available at the following link:  
`dataverse_files/var/www/html/reports/20JA/20JA72/20ja072_fig4_data/C_Mod_for_nn.mat`.

## Relevant Features
The following features from the dataset will be used to train the model:
- `Greenwald_fraction`
- `Mirnov_norm_btor`
- `Te_peaking_ECE`
- `beta_p`
- `ip_error_normalized`
- `kappa`
- `li`
- `lower_gap`
- `n_equal_1_normalized`
- `q95`
- `radiated_fraction`
- `v_loop`
- `z_error`

## Dataset Details
The dataset is structured with two key indexes:
- **`shot`**: Represents a specific experimental run.
- **`time`**: Denotes the timestamp, measured in seconds.

### Label Information
The label for the prediction can be derived from:
- **`time_until_disrupt`**:  
  - If this value is `NaN`, it indicates that the shot did not result in a disruption.

**Note**: All time measurements in the dataset are expressed in seconds.

## Presentation Requirements
The results of your work are to be presented in a **20-minute session** aimed at the **head technician**. While the audience has technical expertise, they are **not familiar with machine learning**, so the focus is on:
- Demonstrating the **technical soundness** and **reliability** of the algorithm.
- Emphasizing the **practical advantages** and benefits of the approach.
