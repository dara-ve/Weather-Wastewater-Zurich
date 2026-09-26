# Weather_Effects_Wastewater_Viral_Load_Zurich
Analysis of weather effects on respiratory virus concentrations in Zurich wastewater using R.
Weather Effects on Wastewater Viral Load in Zurich

R-Bootcamp Data Analysis Project

# Overview
This project was created as a part of the R-Bootcamp in the MSc Applied Information and Data Science program and demonstrates applied data analysis, modelling, and visualisation skills using real-world public health and weather data.

The goal of the project is to analyse wastewater viral load data from Zurich and examine whether weather conditions, specifically air temperature and rain duration, are associated with changes in measured viral concentrations.

The analysis focuses on four respiratory viruses:
- SARS-CoV-2
- Influenza A
- Influenza B
- Respiratory Syncytial Virus (RSV)
The project combines wastewater data with weather data. We first conduct simple exploratory analysis and compare lagged weather. Then we apply Generalized Additive Models (GAMs) and a wave onset detection method to study seasonal patterns and the early growth of viral waves.


# Working Directory

Before proceeding, it is assumed that the R Markdown file is located in the scripts folder and the datasets are stored in the project folder named data. For loading, the datasets are using the relative path. For example: ../data/RESPVIRUSES_wastewater.csv

weather-wastewater-zurich/
├── README.md
├── data/
│   ├── RESPVIRUSES_wastewater.csv
│   ├── OSTLUFT_Rain_duration_Measurements_2023-2026.xlsx
│   └── OSTLUFT_Temperature_Measurements_2023-2026.xlsx
└── scripts/
    └── Weather_Effects_Wastewater_Viral_Load_Zurich.Rmd

The two additional files named Declaration_of_Originality_Group2.pdf and Team_Agreement_Group2.pdf are not required to run or load the project. They are included only for formal reasons, as they attest that the work was completed independently and outline the team agreement.


# Installation

## Prerequisites:
- R (≥ 4.2)
- RStudio

## Required R Packages
The analysis relies on the following R packages:
- dplyr
- ggplot2
- readr
- janitor
- lubridate
- readxl
- tidyr
- scales
- zoo
- plotly

## Installing Packages
Run the following command in R or RStudio:
```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = FALSE,
                      message = FALSE,
                      warning = FALSE)
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

# Datasets
The data files should be placed in the working directory. The project analyzes the following datasets:

## Wastewater Data (RESPVIRUSES_wastewater.csv) 
Source: Swiss Federal Office of Public Health (FOPH) via Open Data Switzerland

## Weather Data
- Rain Duration (OSTLUFT_Rain_duration_Measurements_2023-2026.xlsx)
- Temperature (OSTLUFT_Temperature_Measurements_2023-2026.xlsx)
Source: Ostluft Open Data Platform
The weather data were downloaded from the Ostluft website using their data selection tool. During the download, only the relevant variables and metadata were selected.


# Authors
- Nina Balmer
- Dara Velkov
