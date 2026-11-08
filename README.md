# Investigating Potential West Coast Marine Aquaculture

## Purpose
The analysis completed in this repository is intended to determine which Exclusive Economic Zones (EEZ) on the West Coast of the U.S. are best suited to developing marine aquaculture for several species (including oysters and red rock shrimp). Locations suitable for species were determined by meeting conditions for the species' optimal sea surface temperature (SST) AND depth. In this analysis, a function was made to make the workflow generalizable to determine the optimal marine aquaculture location for any species along the west coast. The output of the function is a map of EEZ regions colored by the amount of suitable area in each EEZ region based on the species, its minimum/maximum SST, and its minimum/maximum depth. 

## Repository Overview
- `west-coast-aquaculture-analysis.qmd`: Quarto document containing all code, maps, and written interpretation.
- `west-coast-aquaculture-analysis.pdf`: Rendered version of the Quarto document.
- `data/`: All data used in the analysis. This folder is listed in .gitignore.

```{r}
west-coast-marine-aquaculture
│   README.md
│   west-coast-aquaculture-analysis.pdf
│   west-coast-aquaculture-analysis.qmd
├── .quarto
     └───typst
└───data
    ├── average_annual_sst_2008.tif
    ├── average_annual_sst_2009.tif
    ├── average_annual_sst_2010.tif
    ├── average_annual_sst_2011.tif
    ├── average_annual_sst_2012.tif
    ├── depth.tif
    ├── wc_regions_clean.dbf
    ├── wc_regions_clean.prj
    ├── wc_regions_clean.shp
    └── wc_regions_clean.shx
```

## Data Access

### Suitable Growing Conditions
#### Oysters
Research has shown that oysters need the following conditions for optimal growth:

- **Sea surface temperature:** 11–30°C
- **Depth:** 0–70 meters below sea level

#### Red Rock Shrimp

Temperature and depth requirements for red rock shrimp were obtained from [SeaLifeBase](https://www.sealifebase.ca/search.php), a database of marine species information. Red rock shrimp were chosen because of their potential for commercial aquaculture.

- **Sea surface temperature:** 10–20°C
- **Depth:** 0–60 meters below sea level

### Sea Surface Temperature
Average annual sea surface temperature (SST) from 2008 to 2012 is used to characterize average sea surface temperature in the region. This data was originally generated from [NOAA's 5km Daily Global Satellite Sea Surface Temperature Anomaly v3.1](https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php).

### Bathymetry
Ocean depth is characterized using the [General Bathymetric Chart of the Oceans (GEBCO)](https://www.gebco.net/data_and_products/gridded_bathymetry_data/#area).

### Exclusive Economic Zones
Maritime boundaries are defined using Exclusive Economic Zones (EEZs) off the West Coast of the United States from [Marineregions.org](https://www.marineregions.org/eez.php).

## Author
Sarah A. Hinkley: [GitHub Profile](https://github.com/sarahhinkley)

## References
- Flanders Marine Institute (2023). Maritime Boundaries Geodatabase: Maritime Boundaries and Exclusive Economic Zones (200NM), version 12. Accessed on November 02, 2026 at [https://www.marineregions.org/eez.php](https://www.marineregions.org/eez.php).

- GEBCO Bathymetric Compilation Group 2026 (2026). The GEBCO_2026 Grid - a continuous terrain model for oceans and land at 15 arc-second intervals. Accessed on November 02, 2026 at [https://www.gebco.net/data-products/gridded-bathymetry-data#area](https://www.marineregions.org/eez.php).

- NOAA Coral Reef Watch (2026). NOAA Coral Reef Watch Version 3.1 Daily Global 5km Satellite Sea Surface Temperature Anomaly Product, 2008–2012. College Park, Maryland, USA: NOAA Coral Reef Watch. Accessed on November 02, 2026 at [https://coralreefwatch.noaa.gov/product/5km/index_5km_ssta.php](https://www.marineregions.org/eez.php).
