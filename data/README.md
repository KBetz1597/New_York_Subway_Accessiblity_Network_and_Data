# Data Description

This directory contains the datasets used to construct and analyze accessibility networks for the New York Metro.

## File Overview

### `New_York_Accessible_Network.csv`
This file contains the accessible network used in the analysis. It represents the subset of stations and connections included in the accessibility network.

### `New_York_Income_Data.xlsx`
This file contains income-related data used in the analysis. These data are linked to stations through geographic matching.

### `New_York_Population_Data.csv`
This file contains population-related data used in the analysis. These data are used to provide demographic context for the network.

### `New_York_Metro_Network.csv`
This file contains the named connections between stations in the London Underground network. It is used to construct the full network graph.

## Data Integration

The datasets are combined as follows:

- `New_York_Metro_Network.csv` is used to build the full transit network
- `New_York_Accessible_Network.csv` defines the accessible subnetwork used in the analysis
- `New_York_Income_Data.xlsx` and `New_York_Population_Data.csv` provide contextual socioeconomic and demographic information

## Sources

These datasets are based on publicly available transit and demographic data sources, including Metropolitan Transit Authority (MTA) and related public datasets.

## Notes and Limitations

- Accessibility is treated as a static property
- Network edges represent connectivity only and do not include travel time or service frequency
- Income and population data are linked through geographic aggregation and may not align exactly with individual station locations


## Licensing

The datasets in this directory are derived from publicly available sources.

- Transit data: Transport for London (TfL) open data (Open Government Licence)
- Socioeconomic data: UK public datasets (Open Government Licence or similar)

Users must comply with the original data licenses and provide appropriate attribution.

Any derived datasets (e.g., accessibility network) reflect transformations applied in this repository but remain subject to the terms of the original data sources.
