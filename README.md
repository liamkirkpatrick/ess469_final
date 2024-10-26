# ess469_final
Liam Kirkpatrick
Fall Quarter 2024 (Extending into Winter due to fieldwork)
Final Project for ESS 469

## Project Summary
*Summary of this project goals*

I am working to interpret the water isotope record from the Denali Ice Core. Alpine ice core water isotope records are more difficult to interpret than similar records in alpine cores, which are widely used as proxies for site and moisture source temperature. However, extreme topography and seasonal weather patterns in alpine ice core sites complicate the drivers, and so the interpreation, of water isotope signals at these sites.

I'm interested in understanding *why* the water isotope record at the ice core site shows the variability that it does. I have already found that it's difficult to explain all of the variability with point reanalysis data just from the ice core site. In this project, I'd like to explore if using machine learning approaches combined with reigonal reanalysis datasets can provide insight into the drivers of water isotope variability. For example, it might be that the reanalysis models fail to capture how extreme winter storms interact with the Alaska range, but the broader context of the Aleutian Low and storm patterns interpreted with machine learning might be able to predict the water isotope record.

For now, the analysis will be limited to the observational era. The goal will be to develop interpretable AI which might provide insight into the *why*, rather than just simple prediction. That said, a solid predictive ML model might have applications in data assimilation over the last millenium.

I will use ERA5 data, the best preforming reanalysis product, at 0.25 degree resolution. I'll use monthly data, as this is the best resolution that could be expected in a century-scale reanalysis product, and because it reduces data to gigabyte scale that I can handle on my computer. Here I start with MSLP, SP, and SST fields. Once I work out issues with the CDS API I would also like to include temperature at the ground and 500hPa levels (roughly the ice core site elevation). I have built my code to make it easy to drop these in later.

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
   - This includes both reanalysis data and ice core data (the ML target).
4. ai_ready/ - *contains AI ready data*
### Notebooks
1. Download_Data.ipynb - *Downloads data. Currently troublyshooting CDS API for ERA5 downloads*
2. Clean_Data.ipynb - *Cleans data. This involves applying a land mask to the SST fields*
3. Prepare_AI_Ready_Data.ipynb - *Prepares data for AI Use. This includes filtering for a subset in all dimensions (lat/lon/time). It also includes moving the varaibles into anomaly space by removing the annual monthly climatology*
4. EDA.ipynb (Exploratory Data Analysis) - *Explores the data, including plots of mean/std/min/max over the subset timeperiod. Also shows correlation to the pressure at the ice core site and the ice core water isotope record*
5. Dimensionality_Reduction.ipynb - *Applies a PCA and ICA to reduce the dimensionality of the data. Includes a discussion of the physical meaning of each PC/IC, their timeseires, and explained variance*

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
