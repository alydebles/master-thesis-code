# An Unobserved Components Model for ENSO: Capturing Dynamics in Both El Niño and La Niña Phases

**Author:** Alyde Bles  
**Date:** 01/01/2025

This repository contains scripts and data required to perform the analysis for ENSO forecasting using an UCM. The analysis is divided into three scripts, which should be run in the following order:

1. `thesis_prepare_variables.ipynb`
2. `thesis_correlation_analysis.ipynb`
3. `thesis_main.ipynb`

Additionally, raw data is stored in the `Data/Data Raw` directory, which is processed in the first script. Subsequent scripts use data from `Data/Data Top` and `Data/Data Process`.

## 1. `thesis_prepare_variables.ipynb`

This script prepares the dataset for analysis by constructing the Niño 3.4 index and explanatory variables, including SST anomalies, zonal wind stress, and thermocline depth. It calculates the thermocline depth dataset using subsurface temperatures and prepares SST, zonal wind stress, and Niño 3.4 datasets. Visualisations such as summary statistics, long-term means, spatial plots, Hovmöller diagrams, and Niño region plots are also generated.

## 2. `thesis_correlation_analysis.ipynb`

This script identifies the regions most correlated with the Niño 3.4 index for different variables and time lags. It calculates the top 10 regions per lag for SST, zonal wind stress, and thermocline depth, which guide the selection of explanatory variables for the forecasting model. Additionally, it creates visualisations, including maps showing the region sizes tested and correlation plots highlighting spatial patterns for each variable and lag. The results, including the selected regions, are saved in the Data/Data Top folder.

## 3. `thesis_main.ipynb`

This script performs the main analysis and forecasting using the prepared data and the results from the correlation analysis. It defines and implements the UCM model with a Kalman Filter, tests explanatory variables, and generates forecasts across lead times. The script evaluates seasonal dependence, forecast bias, and specific ENSO events. It also validates the model's assumptions and produces comprehensive plots for cycles, forecasts, and specific ENSO events.

## Data Workflow

Raw data is stored in Data/Data Raw. This data is processed in the first script, thesis_prepare_variables.ipynb, and the outputs are saved in Data/Data Top and Data/Data Process. These processed files are used in the next scripts, following a structured and sequential workflow. The raw data is too large to upload to this repository. However, a README.txt file in the Data/Data Raw folder explains where and how to download the data.

## Notes

The scripts can be executed independently, as the processed data is already included in the provided zip file. However, if you wish to update the variables or data, the scripts must be run sequentially, as each depends on the outputs of the previous one. Additionally, certain steps in the scripts can take a significant amount of time to complete (over an hour). These include the thermocline depth calculation from subsurface data in thesis_prepare_variables.ipynb and the RMSE variable testing in thesis_main.ipynb. Instructions are provided within the code to indicate how to skip these lengthy computations if desired.

