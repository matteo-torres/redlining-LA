# Exploring Historical Redlining in Los Angeles County

## About

This study aims to explore the historical practice of redlining in Los Angeles County and its legacy on present-day environmental justice, as well as its impact on the collection of bird observations.
- Building effective maps to convey outcomes   
- Manipulating vector and raster data to develop multi-layered maps 
- Visualizing statistics through plots

## Repository Structure

```bash
redlining-LA
├── README.md
├── .gitignore
├── redlining-project.qmd
├── Rmd/Proj files
└── data
    ├── ejscreen
    │   └── EJSCREEN_2023_BG_StatePct_with_AS_CNMI_GU_VI.gdb
    ├── gbif-birds-LA
    │   └── gbif-birds-LA.shp
    └── mapping-inequality
        └── mapping-inequality-los-angeles.json
```

## Data

All data has been downloaded and organized within the data folder of this repository. The files are stored in separate subfolders, named for easy access. For the EJScreen dataset, Los Angeles County was filtered to retain only relevant data, with excess polygons removed to ensure accuracy and focus.

```bash
los_angeles <- ejscreen %>%
    dplyr::filter(CNTY_NAME %in% c("Los Angeles County") & ID != '060379902000' &
                  ID !='060379901000' &
                  ID != '060379903000' &
                  ID != '599100')
```

## References

Global Biodiversity Information Facility. (n.d.). GBIF backbone taxonomy. Retrieved from https://www.gbif.org/dataset/4fa7b334-ce0d-4e88-aaae-2e0c138d049e

Digital Scholarship Lab. (n.d.). Mapping inequality: Redlining in New Deal America. Retrieved from https://dsl.richmond.edu/panorama/redlining/data

U.S. Environmental Protection Agency. (n.d.). EJScreen data download. Retrieved from https://www.epa.gov/ejscreen/download-ejscreen-data

## Acknowledgements

This repository was created for a final project related to the course EDS 223: Geospatial Analysis & Remote Sensing.

This course is an academic requirement for the Master of Environmental Data Science (MEDS) program at the Bren School of Environmental Science & Management, University of California, Santa Barbara.
