# Possession, Protection, Protest
**State-Gendered Violence and Male Mobilization: The Moderating Role of Social Gender Expectations?**

MA thesis, Social Sciences, UC3M (Universidad Carlos III de Madrid)
Author: Jorge Carpio Herrero
Supervisor: Prof. Juan Jesús Fernández González

## Overview

This repository contains the replication code for a cross-national quantitative study examining whether 
state-perpetrated gendered violence activates male mobilization, and whether social gender norms moderate that response. 
The analysis combines individual-level data from the World Values Survey (WVS) with country-year measures of 
gendered state violence derived from ACLED and political/economic indicators from V-Dem and the World Bank/IMF.

Two identification strategies are used: a midpoint-fieldwork-anchored strategy (primary) and 
an interview-date-anchored strategy (robustness).

## What's in this repository

This repository contains **only the analysis code**, provided as a single Quarto document (`clean_tfm.qmd`):

  - full data cleaning
  - variable construction (Kwak weighting, CFA, exposure windows, anchoring strategies)
  - model estimation
  - and figure/table generation for all results reported in the thesis.

**Raw data files are not included** due to size and licensing restrictions. 

## Data sources

To reproduce the analysis, download the following datasets and place them in a local `data/` folder:

| Dataset | Source | Access |
|---|---|---|
| World Values Survey (all waves) | [worldvaluessurvey.org](https://www.worldvaluessurvey.org/WVSContents.jsp) | Free registration required |
| ACLED (Armed Conflict Location & Event Data) | [acleddata.com](https://acleddata.com/data-export-tool/) | Free academic access upon registration |
| V-Dem (Varieties of Democracy), v15 | [v-dem.net](https://www.v-dem.net/data/the-v-dem-dataset/) | Open access |
| World Bank World Development Indicators | [data.worldbank.org](https://data.worldbank.org/) | Open access |
| IMF Data Mapper (GDP, inflation) | [imf.org/external/datamapper](https://www.imf.org/external/datamapper/) | Open access |

Exact variable codes, filters, and merging procedures are documented in the Quarto file itself.
Only the WVS and ACLED packages need downloading, as VDEM and WB data were obtained through R packages.
To facilitate the data cleaning, ACLED was filtered to exclude battles, explosions, and remote violence 
before downloading it from the web.

## Reproducing the analysis

1. Clone this repository
2. Create a `data/` folder in the project root (this folder is `.gitignore`d)
3. Download the datasets above into `data/`
4. Open `clean_tfm.qmd` in RStudio
5. Required R packages are listed at the top of the document
6. Change working directories in the .qmd doc

## Citation

If you use this code, please cite:

> Carpio Herrero, J. (2026). *Possession, Protection, Protest: State-Gendered Violence and Male Mobilization: The Moderating Role of Social Gender Expectations?*. MA Thesis, Universidad Carlos III de Madrid.

## Contact

Questions or comments are welcome — please open an issue or reach out directly.

## License

This code is shared for academic transparency and replication purposes. Please do not use without attribution.
