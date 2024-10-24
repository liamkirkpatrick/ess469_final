# ess469_final
Liam Kirkpatrick
Fall Quarter 2024 (Extending into Winter due to fieldwork)
Final Project for ESS 469

## Project Summary

## Repository Use
*Summary of how to use the data and code in this repository yourself*

1. To install this repository, first you should clone the repository with git (git clone git@github.com:UW-MLGEO/MLGEO2024_liamkp.git)
2. Next, create a conda environment (conda env create -f environment.yml -n YOUR_ENV_NAME_HERE)
3. Finally, activate the conda environment (conda activate YOUR_ENV_NAME_HERE)

To run the notebooks included here:

1. Navigate to your local clone of this repository in terminal
2. Activate the environment (see above)
3. Launch JupyterLab with "jupyter lab" or (prefered) use vs code

## Repository Contents
*Summary of file contents*

### Data
1. raw/ - *contains raw datafiles*
2. clean/ - *contains clean datafiles*
3. ai_ready/ - *contains AI ready data*
### Notebooks
1. download_data.ipynb - *downloads data*
2. clean_data.ipynb - *cleans data, gets into ai_ready state*

## Data

Data:
    Model: ERA5 Reanalysis
    Temporal Resolution: Monthly resolution
    Temporal Extent: Jan 1940 - Dec 2023
    Spatial Resolution: 0.25 degree grid
    Spatial Extent: Global
    Fields: MSLP, 500hPa Height, and SST
    Filetype: .nc (netCDF)
    Filesize: All data is approx 12 GB
Access: Data downloaded through Copernicus Climate Data Score using the CDS online download tool at https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=download
