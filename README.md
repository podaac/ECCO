# ECCO
Code and scripts for working with datasets published to PO.DAAC by Estimating the Circulation and Climate of the Ocean (ECCO) consortium. Example outputs from the notebooks are included in the [outputs](outputs/) folder of this repository. 

For more information about the ECCO V4r4 datasets, please visit the mission page on the PO.DAAC web portal:     
https://podaac.jpl.nasa.gov/ECCO

**Requirements:** Python 3 + netCDF4 library, along with these Python packages - s3fs, requests, pandas, xarray, matplotlib, cartopy

## [cloud_direct_access_s3.ipynb](cloud_direct_access_s3.ipynb)

This notebook gives two examples of in-region access to ECCO data in AWS S3 from the *aws-west-2* region. 

<img src="https://podaac.jpl.nasa.gov/Podaac/thumbnails/ECCO_L4_SSH_05DEG_DAILY_V4R4.jpg" width="80%"/>

You will learn how to 1) identify the S3 bucket/path corresponding to two datasets from ECCO, 2) retrieve AWS credentials and load data from the netCDF files into a multi-file dataset using *xarray*, 3) select/slice the dataset and plot a time series animation with *matplotlib* and *cartopy*, and 4) save animations to disk as MP4 files.

**Example 1** accesses and plots a global, monthly time series animation of sea surface height (SSH) data loaded from netCDF files in S3 (https://doi.org/10.5067/ECG5D-SSH44)

**Example 2** accesses and plots an XYT slice of ocean temperature flux data over the Gulf of Mexico. This example is similar to example 1, but demonstrates the use of a *glob* pattern to select netCDF files inside the S3 bucket to open/read with *xarray* (https://doi.org/10.5067/ECG5D-HEA44)

Both examples work with data represented on the interpolated latitude/longitude grid (0.5-degree resolution; as opposed to the native LLC0090 grid).

## [cloud_harmony_zarr_reformat.ipynb](cloud_harmony_zarr_reformat.ipynb)

This notebook leverages the *Zarr reformatter service* (via the [Harmony API](https://harmony.earthdata.nasa.gov/)) to convert netCDF files containing monthly ocean bottom pressure data from ECCO into Zarr file format and load them with *xarray*. The zarr files are staged in an S3 bucket that is made accessible to the user from the *aws-west-2* region. 

<img src="https://podaac.jpl.nasa.gov/Podaac/thumbnails/ECCO_L4_OBP_05DEG_MONTHLY_V4R4.jpg" width="80%"/>

You will learn how to 1) submit a Harmony API request for ECCO V4r4 data in Zarr format, 2) retrieve AWS credentials and load datasets staged in Zarr format into a multi-file dataset using *xarray*, 3) plot a time series using *xarray*'s interface to *matplotlib*.

More information about ocean bottom pressure data from ECCO V4r4 may be found on the PO.DAAC web portal: https://doi.org/10.5067/ECG5M-OBP44 

## PO.DAAC contacts:
*  jack.mcnelis@jpl.nasa.gov
*  Help Desk: podaac@podaac.jpl.nasa.gov
