Data sets for testing ML algorithms for deforestation mapping in Brazilian Amazonia.
================

<img src="sits_sticker.png" alt="SITS icon" align="right" height="150" width="150"/>

This project contains data sets for testing machine learning algorithms for deforestation mapping and monitoring in Brazilian Amazonia. These data sets consists of image time series of one Sentinel-2 tile (20LMR) for year 2022, as well R scripts used to perform land use classification together with training data sets. 

To load these data sets, run:

`devtools::install_github("e-sensing/rondonia-20LMR")`

## Image data cube for Sentinel-2 tile 20LMR for year 2022

The directory `/images` contains a regular series of images covering MGRS tile 20LMR, with 23 time instances for the period 2022-01-05 to 2022-12-23. Each time instances contains 10 bands (B02, B03, B04, B05, B06, B07, B08, B8A, B11, B12), three indices (NDVI, EVI, NBR) and 3 mixture model endmembers (VEGETATION, LAND, and SHADOW). Image names folow the standard `SENTINEL-2_MSI_20LMR_<band>_<year-month-date>.tif`. 

## Training samples for deforestation mapping

The directory `/samples`  contains time series to be used for classification with machine learning methods which are available when the package is loaded. All satellite image time series have the following columns: 

- longitude (East-west coordinate of the time series sample in WGS 84).
- latitude (North-south coordinate of the time series sample in WGS 84).
- start_date (initial date of the time series).
- end_date (final date of the time series).
- label (the class label associated to the sample).
- cube (the name of the image data cube associated with the data).
- time_series (list  with the values of the time series).

License: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).

## Scripts to produce deforestation maps

The directory `/scipts` contains R scripts that use the `sits` package for mapping deforested area in the image data cube.  For description of how these scripts work, please see chapter ["Introduction"](https://e-sensing.github.io/sitsbook/introduction.html) in the `sits` [reference book](https://e-sensing.github.io/sitsbook/index.html).

License: Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0).





