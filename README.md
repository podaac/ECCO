# ECCO Tutorials

A place to find exercises for learning to work with ECCO data archived in AWS by the PO.DAAC. 

<img src="https://podaac.jpl.nasa.gov/Podaac/thumbnails/ECCO_L4_SSH_05DEG_DAILY_V4R4.jpg" width="80%"/>

Most tutorials in this repository take the form of python notebooks. [Jupyter](https://jupyter.org/) is a very popular version of python notebooks, and is used extensively by the PO.DAAC team.

## [data_access](Data_Access/)

### [notebook exercise 1](Data_Access/cloud_direct_access_s3.ipynb) - direct, in-region access to ECCO V4r4 datasets in S3

In this notebook, you will learn to 1) identify AWS S3 endpoints corresponding to two ECCO datasets of interest, 2) retrieve your AWS credentials which provide access to PO.DAAC data in AWS, 3) load the target netCDF files into two multi-file datasets with *xarray*, and 4) slice and plot the datasets as animated time series using *matplotlib* and *cartopy*. The notebook finishes by writing the animations to disk as MP4 files.

Example 1 accesses and plots a global time series animation of monthly [sea surface height (SSH)](https://doi.org/10.5067/ECG5D-SSH44) data loaded from netCDF datasets in S3.

Example 2 accesses and plots an XYT slice of monthly [ocean temperature flux (TFLUX)](https://doi.org/10.5067/ECG5D-HEA44) data over the Gulf of Mexico. Demonstrates the use of a *glob* pattern to select netCDF files inside the S3 bucket to open/read with *xarray*. 

### [notebook exercise 2](Data_Access/cloud_harmony_zarr_reformat.ipynb) - access ECCO V4r4 datasets in Zarr format (via the Harmony API)

In this notebook, you will learn to 1) use the Zarr reformatter service (via Harmony API) to request monthly [ocean bottom pressure (OBP)](https://doi.org/10.5067/ECG5D-HEA44) data from ECCO V4r4 in Zarr format, 2) retrieve your AWS credentials which provide access to PO.DAAC data in AWS, and 3) load the staged zarr datasets into a multi-file dataset with *xarray*. The notebook finishes by drawing static time series plots with *matplotlib* and *xarray*.

## PO.DAAC contacts:
*  jack.mcnelis@jpl.nasa.gov
*  Help Desk: podaac@podaac.jpl.nasa.gov