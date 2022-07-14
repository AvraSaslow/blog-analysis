# NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP) Data
This file describes the analysis done by the Resource Watch team for Facebook to be used in displaying Representative Concentration Pathways (RCP) in their newly launched [Climate Science Center](https://www.facebook.com/climatescienceinfo/). RCPs are hypothetical models that predict how various concentrations of greenhouse gases in the atmosphere will change due to future human activities. The goal of this analysis is to demonstrate two RCPs with differing levels of future concentrations: 4.5 (moderate levels of greenhouse gases) and 8.5 (very high levels of greenhouse gases).

Check out the Climate Science Center (CSC) for up-to-date information on climate data in your area from trusted sources. And go to [Resource Watch](https://resourcewatch.org/) to explore over 300 datasets covering topics from food, forests, water, oceans, cities, energy, climate, and society. This analysis was originally performed by [Avra Saslow](https://www.wri.org/profile/avra-saslow) and was QC'd by [Kristine Lister](https://www.wri.org/profile/kristine-lister).

### Data Sources
This analysis was done using the data from the [NASA Earth Exchange Global Daily Downscaled Projections (NEX-GDDP) dataset](https://www.nccs.nasa.gov/services/data-collections/land-based-products/nex-gddp), which provides four global models that predict change in greenhouse gases. The administrative global area is from [GADM](https://gadm.org/). 

### Methods
The objective of this analysis is to aggregate raster image files associated with a specific RCP and calculate the average value per RCP over state/country level regions. 

The first objective of this analysis is to fetch the state level burned area data from 2002 to 2019, and aggregate country level and continent level burned area. This analysis was done using the file [Fire_by_LULC.py](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/Fire_by_LULC.py), following the steps:
1. Download the NEX-GDDP data from Resource Watch.
2. Aggregate mean RCP values 4.5 and 8.5 over state regions.
3. Aggregate mean RCP values 4.5 and 8.5 over country regions.
4. Export the results as a CSV file. 

### Final Data
The final data can be viewed in the directory [data](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/data/).
1. [state_02_19.csv](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/data/state_02_19.csv)
    - State level burned area data from 2002 to 2019 by LULC.
2. [country_02_19.csv](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/data/country_02_19.csv)
    - Country level burned area data from 2002 to 2019 by LULC.
3. [continent_02_19.csv](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/data/continent_02_19.csv)
    - Continent level burned area data from 2002 to 2019 by LULC.
4. [USA_02_20.csv](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/data/USA_02_20.csv)
    - State level burned area data from 2002 to 2020.
5. [USA_state_level_statistics](https://github.com/resource-watch/blog-analysis/blob/master/req_021_facebook_fires/data/USA_state_level_statistics)
    - State level monthly burned area data for 2020.


### References
- Gassert, F., E. Cornejo, and E. Nilson. 2021. “Making Climate Data Accessible: Methods for Producing NEX-GDDP and LOCA Downscaled Climate Indicators” Technical Note. Washington, DC: World Resources Institute. Available online at https://www.wri.org/research/making-climate-data-accessible. www.resourcewatch.org.

- Global Administrative Areas (2021). GADM database of Global Administrative Areas, version 3.6. \[online\] URL: [www.gadm.org](www.gadm.org).
