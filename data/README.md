# Data Description

This directory contains the datasets used to construct and analyze accessibility networks for the New York Metro.

## File Overview

### `New_York_Accessible_Network.csv`
This file contains the accessible network used in the analysis. It represents the subset of stations and connections included in the accessibility network.

### `New_York_Income_Data.xlsx`
This file contains income-related data used in the analysis. These data are linked to stations through geographic matching.

### `New_York_Population_Data`
Income data are obtained from the U.S. Census Bureau American Community Survey (ACS) 5-Year Estimates (2021) using the Census API. These data are not stored directly in this repository but can be retrieved programmatically.

### `New_York_Metro_Network.csv`
This file contains the named connections between stations in the London Underground network. It is used to construct the full network graph.

## Data Integration

The datasets are combined as follows:

- `New_York_Metro_Network.csv` is used to build the full transit network
- `New_York_Accessible_Network.csv` defines the accessible subnetwork used in the analysis
- `New_York_Income_Data.xlsx` and `New_York_Population_Data.xlsx` provide contextual socioeconomic and demographic information

## Sources

These datasets are based on publicly available transit and demographic data sources, including Metropolitan Transit Authority (MTA), U.S. Census Bureau, and related public datasets.

Income data: U.S. Census Bureau, American Community Survey (ACS) 5-Year Estimates (2021)
    - Example API query:
            https://api.census.gov/data/2021/acs/acs5?get=NAME,B19013_001E&for=tract:*&in=state:36%20county:{county}


## Notes and Limitations

- Accessibility is treated as a static property
- Network edges represent connectivity only and do not include travel time or service frequency
- Income and population data are linked through geographic aggregation and may not align exactly with individual station locations


## Licensing

The datasets in this directory are derived from publicly available sources:

- MTA data: subject to MTA data usage policies
- U.S. Census data: public domain (no restrictions on use)

Users must comply with the original data licenses and provide appropriate attribution.

Any derived datasets (e.g., accessibility network) reflect transformations applied in this repository but remain subject to the terms of the original data sources.
