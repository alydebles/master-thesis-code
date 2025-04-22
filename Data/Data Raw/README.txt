This folder contains three subfolders with the raw data used for my thesis:

- Sea Surface Temperature
- Thermocline Depth
- Wind Stress

The folders are here to show the structure, but the actual data is not included because the files are too large.

---

What is inside each foler and what you need to download:

1. Sea Surface Temperature 
   - Monthly gridded SST data.
   - Download from this link: https://psl.noaa.gov/thredds/fileServer/Datasets/noaa.ersst.v5/sst.mnmean.nc
   - You need to download the **NetCDF monthly data** 
   - Place the `.nc` files in the folder `Sea Surface Temperature/`

2. Thermocline Depth
   - This folder contains the subsurface ocean temperature data used to calculate the 20°C isotherm depth (z20).
   - Download all NetCDF files for the period 1940 to 2023
   - Keep the downloaded `.zip` file and place .zip files into `Thermocline Depth/`
   - Download this: https://www.metoffice.gov.uk/hadobs/en4/EN.4.2.2.analyses.g10.download-list.txt (but only from 1940 to 2023)

3. Wind Stress:
   - Monthly averaged zonal and meridional wind stress data
   - Download from: https://psl.noaa.gov/thredds/fileServer/Datasets/ncep.reanalysis/Monthlies/surface_gauss/uflx.sfc.mon.mean.nc
   - Variable to download; 'uflx'
   - Place it inside `Wind Stress/`



