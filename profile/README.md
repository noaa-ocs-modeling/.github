# [Coastal Marine Modeling Branch (CMMB)](https://coastaloceanmodels.noaa.gov/)
##### under the U.S. National Oceanic and Atmospheric Administration (NOAA) National Ocean Service (NOS) Office of Coast Survey (OCS) 

NOAA's [Office of Coast Survey](https://nauticalcharts.noaa.gov/) develops computer models that forecast oceanic variables (sea level, currents, temperature, salinity, etc.) in U.S. coastal regions. 
These models can be grouped into three categories: **tidal models**, **storm surge models**, and **operational forecast systems**.

- **Tidal models** are necessary for determining a reference sea level, the main application of which is nautical charting.
- **Storm surge models** predict events of extreme sea level rise and inundation of coastal areas in response to strong winds and low atmospheric pressure conditions.
- **Operational forecast systems (OFS)** provide information on tidal and non-tidal sea level variations, as well as currents, temperature, and salinity, in three dimensions. 
These variables can provide guidance to ship operators for route planning (i.e. avoiding strong opposing currents to save fuel) and route monitoring (safe and efficient coastal navigation, i.e. avoiding low water levels and grounding risks). This navigation guidance is part of the [NOS Precision Navigation](https://marinenavigation.noaa.gov/) initiative, which aims to integrate important data streams into single-dissemination, so that mariners can make decisions driven by data.

The [NOAA Water Initiative](https://www.noaa.gov/water/explainers/noaa-water-initiative-vision-and-five-year-plan) calls for integrated prediction of river, ocean, and ice dynamics. 
This requires an investment in research and collaboration with scientists across the board, both at **NOAA** and academic partners, in order to reach the goals of accurate forecasting within U.S. marine and riverine areas.

- Commercial and recreational fishermen use oceanic variables provided by forecasting systems, such as surface currents, locations of temperature fronts and river plumes, near-bottom conditions (temperature, oxygen, etc.), and the depth of the oceanic thermocline, to increase safety and lower operational costs when planning fishing trips.
- The **U.S. Coast Guard**, along with agencies dealing with environmental hazard response, can use information on surface currents to assist search-and-rescue operations and mitigate the impacts of accidents such as oil spills.
- In the future, accurate forecasts of ocean dynamics will become a base for [oceanic ecological forecasting](https://oceanservice.noaa.gov/ecoforecasting), predicting impacts of harmful algae blooms and pathogens, hypoxic conditions, and ocean acidification on U.S. coastal populations.

## CMMB Repositories
### [CoastalApp](https://github.com/noaa-ocs-modeling/CoastalApp)
CoastalApp is a framework for building coupled FORTRAN modeling applications utilizing the NOAA Environmental Modeling System (NEMS), the National Unified Operational Prediction Capability (NUOPC), and Unified Forecast System (UFS) best practices. 
Supported models include [ADCIRC](https://github.com/adcirc/adcirc-cg), [SCHISM](https://github.com/schism-dev/schism), [NWM](https://github.com/noaa-ocs-modeling/nwm_public_nuopc), and [WW3](https://github.com/noaa-ocs-modeling/WW3).
### [CoupledModelDriver](https://github.com/noaa-ocs-modeling/CoupledModelDriver)
CoupledModelDriver provides configuration generation and HPC job manager submission for coupled modeling systems.
### [OCSMesh](https://github.com/noaa-ocs-modeling/OCSMesh)
OCS mesh is a mesh preparation tool for coastal modeling applications.
### [EnsemblePerturbation](https://github.com/noaa-ocs-modeling/EnsemblePerturbation)
EnsemblePerturbation is a Python application providing perturbation capability for NHC track ensembles, as well as results combination of ADCIRC ensemble outputs.
