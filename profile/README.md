# [modeling under the NOAA Office of Coast Survey](https://coastaloceanmodels.noaa.gov/)
##### under the U.S. National Oceanic and Atmospheric Administration (NOAA) National Ocean Service (NOS)

NOAA's [Office of Coast Survey](https://nauticalcharts.noaa.gov/) develops computer models that forecast oceanic variables (sea level, currents, temperature, salinity, etc.) in U.S. coastal regions. 
These models can be grouped into three categories: **tidal models**, **storm surge models**, and **operational forecast systems**.

- **Tidal models** are necessary for determining a reference sea level, the main application of which is nautical charting.
- **Storm surge models** predict events of extreme sea level rise and inundation of coastal areas in response to strong winds and low atmospheric pressure conditions.
- **Operational forecast systems (OFS)** provide information on tidal and non-tidal sea level variations, as well as currents, temperature, and salinity, in three dimensions. 
These variables can provide guidance to ship operators for route planning (i.e. avoiding strong opposing currents to save fuel) and route monitoring (safe and efficient coastal navigation, i.e. avoiding low water levels and grounding risks). This navigation guidance is part of the [NOS Precision Navigation](https://marinenavigation.noaa.gov/) initiative, which aims to integrate important data streams into single-dissemination, so that mariners can make decisions driven by data.

## Repositories
### [CoastalApp](https://github.com/noaa-ocs-modeling/CoastalApp)
CoastalApp is a framework for building coupled FORTRAN modeling applications utilizing the NOAA Environmental Modeling System (NEMS), the National Unified Operational Prediction Capability (NUOPC), and Unified Forecast System (UFS) best practices. 
Supported models include [ADCIRC](https://github.com/adcirc/adcirc-cg), [SCHISM](https://github.com/schism-dev/schism), [NWM](https://github.com/noaa-ocs-modeling/nwm_public_nuopc), and [WW3](https://github.com/noaa-ocs-modeling/WW3).
### [CoupledModelDriver](https://github.com/noaa-ocs-modeling/CoupledModelDriver)
CoupledModelDriver provides configuration generation and HPC job manager submission for coupled modeling systems.
### [OCSMesh](https://github.com/noaa-ocs-modeling/OCSMesh)
OCS mesh is a mesh preparation tool for coastal modeling applications.
### [EnsemblePerturbation](https://github.com/noaa-ocs-modeling/EnsemblePerturbation)
EnsemblePerturbation is a Python application providing perturbation capability for NHC track ensembles, as well as results combination of ADCIRC ensemble outputs.
