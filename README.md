# Weather Effects on Wastewater Viral Load in Zurich

**Analysis of weather effects on respiratory virus concentrations in Zurich wastewater using R.**

*R-Bootcamp Data Analysis Project · MSc Applied Information and Data Science*

## Overview

This project investigates whether weather conditions, specifically air temperature and rain duration, are associated with changes in respiratory virus concentrations measured in Zurich wastewater.

The analysis combines public health and weather data and applies exploratory data analysis, lagged weather analysis, Generalized Additive Models (GAMs), and wave onset detection to examine seasonal patterns and short-term weather associations.

The project was developed as part of the R-Bootcamp in the MSc Applied Information and Data Science program and demonstrates a reproducible data analysis workflow using R and R Markdown.

The analysis focuses on four respiratory viruses:

- SARS-CoV-2
- Influenza A
- Influenza B
- Respiratory Syncytial Virus (RSV)

The project combines wastewater data with weather data. We first conduct exploratory analyses and compare lagged weather conditions. We then apply Generalized Additive Models (GAMs) and a wave onset detection method to study seasonal patterns and the early growth of viral waves.

## Project Structure

The R Markdown file is located in the `scripts` folder, while the datasets are stored in the `data` folder.

The project uses relative paths. For example:

`../data/RESPVIRUSES_wastewater.csv`

The repository is structured as follows:

```text
weather-wastewater-zurich/
├── README.md
├── data/
│   ├── RESPVIRUSES_wastewater.csv
│   ├── OSTLUFT_Rain_duration_Measurements_2023-2026.xlsx
│   └── OSTLUFT_Temperature_Measurements_2023-2026.xlsx
└── scripts/
    └── Weather_Effects_Wastewater_Viral_Load_Zurich.Rmd
```

## Installation

### Prerequisites

- R (≥ 4.2)
- RStudio

### Required R Packages

The analysis relies on the following R packages:

- `dplyr`
- `ggplot2`
- `readr`
- `janitor`
- `lubridate`
- `readxl`
- `tidyr`
- `scales`
- `zoo`
- `plotly`

### Installing Packages

The required packages can be installed in R using:

```r
install.packages(c(
  "dplyr",
  "ggplot2",
  "readr",
  "janitor",
  "lubridate",
  "readxl",
  "tidyr",
  "scales",
  "zoo",
  "plotly"
))
```

The packages are then loaded in the R Markdown analysis:

```r
library(dplyr)
library(ggplot2)
library(readr)
library(janitor)
library(lubridate)
library(readxl)
library(tidyr)
library(scales)
library(zoo)
library(plotly)
```

## Datasets

The project combines wastewater surveillance data with weather measurements for Zurich.

### Wastewater Data

**File:** `RESPVIRUSES_wastewater.csv`

**Source:** Swiss Federal Office of Public Health (FOPH) via Open Data Switzerland.

The dataset contains wastewater measurements for respiratory viruses.

### Weather Data

**Files:**

- `OSTLUFT_Rain_duration_Measurements_2023-2026.xlsx`
- `OSTLUFT_Temperature_Measurements_2023-2026.xlsx`

**Source:** Ostluft Open Data Platform.

The weather data were downloaded from the Ostluft website using their data selection tool. During the download, only the relevant variables and metadata were selected.

## Authors

- Nina Balmer
- Dara Velkov

## Contributions

Both authors contributed equally to the project. The work was carried out collaboratively, including data preparation, exploratory data analysis, statistical modelling, visualisation, interpretation of results, and documentation.
