This annotated dataset comes from the Environmental Data Automated Track Annotation System (Env-DATA) on Movebank (movebank.org). The environmental data attributes are created and distributed by government and research organizations. For general information on the Env-DATA System, see Dodge et al. (2013) and movebank.org/node/6607.

Terms of Use: Verify the terms of use for relevant tracking data and environmental datasets prior to presenting or publishing these data. Terms of use for animal movement data in Movebank are defined by the study owners in the License Terms for the study. Terms of use for environmental datasets vary by provider; see below for details. When using these results in presentations or publications, acknowledge the use of Env-DATA and Movebank and cite Dodge et al. (2013). Sample acknowledgement: "[source product/variable] values were annotated using the Env-DATA System on Movebank (movebank.org)." Please send copies of published work to support@movebank.org.

Contact: support@movebank.org. Include the access key below with questions about this request.

---------------------------

Annotated data for the following Movebank entities are contained in this file:
Movebank study name: At-sea distribution Antarctic Petrel, Antarctica 2012 (data from Descamps et al. 2016)
Annotated Animal IDs: 4165869
Requested on Wed Apr 22 08:22:31 CEST 2020
Access key: 6644783168583569612
Requested by: Ethan Ashby

---------------------------

File attributes

Attributes from the Movebank database (see the Movebank Attribute Dictionary at http://www.movebank.org/node/2381):
Location Lat: latitude in decimal degrees, WGS84 reference system
Location Long: longitude in decimal degrees, WGS84 reference system
Timestamp: the time of the animal location estimates, in UTC
Study-specific Measurement
Tag Tech. Spec.
Comments
Modelled
Update Ts

Locations are the the geographic coordinates of locations along an animal track as estimated by the processed sensor data.


---------------------------

Attributes from annotated environmental data:
Name: OSU Ocean NPP 0.083deg Monthly NPP
Description: Net primary productivity in the ocean; the net rate at which carbon from the atmosphere is taken up by plants. Negative values indicate net carbon release to the atmosphere.
Unit: mgC m^-2 day^-1
No data values: -9999 (provider), NaN (interpolated)
Interpolation: inverse-distance-weighted

Name: ECMWF Interim Full Daily SFC Sea Ice Cover
Description: Fraction of the model grid cell that is covered with sea ice.
Unit: (0-1)
No data values: NaN (interpolated)
Interpolation: inverse-distance-weighted

Name: ETOPO1 Elevation
Description: Elevation of the land surface over land and the ocean floor over ocean. Over the Antarctic and Greenland ice sheets values indicate the elevation of the top of the ice sheets.
Unit: m amsl
No data values: -32768 (provider), NaN (interpolated)
Interpolation: nearest-neighbour

Name: MODIS Ocean Aqua OceanColor 4km Daily Daytime SST
Description: Daytime water temperature near the ocean's surface computed from MODIS bands 31 (10.780–11.280 um) and 32 (11.770–12.270 um).
Unit: deg C
No data values: -32767S (provider), NaN (interpolated)
Interpolation: inverse-distance-weighted

---------------------------

Environmental data services

Service: ETOPO1 1-arc-minute Global Relief Model
Provider: NOAA National Geophysical Data Center
Datum: N/A
Projection: N/A
Spatial granularity: 1 arc-minute
Spatial range (long x lat): E: 180.0    W: -180.0 x N: 90    S: -90
Temporal granularity: N/A
Temporal range: N/A
Source link: https://www.ngdc.noaa.gov/mgg/global/
Terms of use: http://dx.doi.org/10.7289/V5C8276M
Related websites:
http://dx.doi.org/10.7289/V5C8276M
http://www.ngdc.noaa.gov/mgg/global/

Service: Oregon State Ocean Productivity Reanalysis/MODIS-based 0.083-deg Monthly
Provider: Oregon State University
Datum: N/A
Projection: N/A
Spatial granularity: 1/12 degree
Spatial range (long x lat): E: 180.0    W: -180.0 x N: 90    S: -90
Temporal granularity: monthly
Temporal range: 2002 to 2015
Source link: http://orca.science.oregonstate.edu/data/2x4/monthly/vgpm.r2014.m.chl.m.sst/hdf/
Terms of use: http://orca.science.oregonstate.edu/2160.by.4320.monthly.hdf.vgpm.m.chl.m.sst.php
Related websites:
http://www.science.oregonstate.edu/ocean.productivity/
http://www.science.oregonstate.edu/ocean.productivity/vgpm.model.php
http://www.science.oregonstate.edu/ocean.productivity/references.php
http://orca.science.oregonstate.edu/1080.by.2160.8day.hdf.vgpm.m.chl.m.sst.php
http://dx.doi.org/10.4319/lo.1997.42.1.0001

Service: MODIS Ocean/Aqua Mapped OceanColor 4-km Daily
Provider: NASA Goddard Space Flight Center Ocean Biology Processing Group
Datum: N/A
Projection: N/A
Spatial granularity: 4.64 km
Spatial range (long x lat): E: 180.0    W: -180.0 x N: 90    S: -90
Temporal granularity: daily
Temporal range: 2002 to present
Source link: https://oceandata.sci.gsfc.nasa.gov/MODIS-Aqua/Mapped/Daily/4km/
Terms of use: https://oceancolor.gsfc.nasa.gov/citations/
Related websites:
https://oceancolor.gsfc.nasa.gov/data/aqua/
https://oceancolor.gsfc.nasa.gov/atbd/

Service: ECMWF Global Atmospheric Reanalysis/Interim Full Daily at Surface
Provider: European Centre for Medium-Range Weather Forecasts
Datum: N/A
Projection: N/A
Spatial granularity: 0.75 degrees
Spatial range (long x lat): E: 180.0    W: -180.0 x N: 89.463    S: -89.463
Temporal granularity: 6 hourly
Temporal range: 1979-01-01 to present
Source link: http://apps.ecmwf.int/datasets/data/interim_full_daily/?levtype=sfc
Terms of use: https://www.ecmwf.int/en/faq/how-do-i-cite-era-interim-my-publication
Related websites:
https://www.ecmwf.int/en/research/climate-reanalysis
https://www.ecmwf.int/node/8174
https://doi.org/10.21957/m1cs7h
http://apps-dev.ecmwf.int/codes/grib/param-db

---------------------------

Dodge S, Bohrer G, Weinzierl R, Davidson SC, Kays R, Douglas D, Cruz S, Han J, Brandes D, Wikelski M (2013) The Environmental-Data Automated Track Annotation (Env-DATA) System: linking animal tracks with environmental data. Movement Ecology 1:3. doi:10.1186/2051-3933-1-3

Development and maintenance of Env-DATA is funded by the Max Planck Society, and has been supported by US National Science Foundation Biological Infrastructure award 1564380, NASA ABoVE project NNX15AT91A, and NASA Earth Science Division, Ecological Forecasting Program Project NNX11AP61G.