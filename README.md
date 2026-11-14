CO2 Emissions Analysis: Zimbabwe

## Overview
This repository presents an exploratory data analysis and visualization of historical Carbon Dioxide ($\text{CO}_2$) emissions in **Zimbabwe** using R. All data processing steps, R scripts, and output visualizations are documented below.

## Data Source
- **Dataset:** Our World in Data (OWID) — $\text{CO}_2$ and Greenhouse Gas Emissions Dataset (`owid-co2-data.csv`)
- **Primary Underlying Source:** Global Carbon Budget
- **Variables Analyzed:**
  - `co2`: Annual total territorial $\text{CO}_2$ emissions (measured in million tonnes)
  - `co2_per_capita`: Annual $\text{CO}_2$ emissions per person (measured in tonnes)
  - `coal_co2`, `oil_co2`, `cement_co2`: Breakdown of emissions by fuel and industrial source

## Methodology & Steps Taken
1. **Data Acquisition:** Loaded the global OWID $\text{CO}_2$ dataset directly into RStudio using `read.csv()`.
2. **Data Filtering & Cleaning:** Filtered records specifically for `country == "Zimbabwe"` from 1950 onward and selected key emission indicators using `tidyverse` (`dplyr`).
3. **Visualization:** Used `ggplot2` to generate three time-series plots illustrating total emissions, per capita trends, and sectoral breakdowns by fuel type.
4. **Export:** Saved all output figures at 300 DPI inside the `figures/` directory.

## Output Figures & Key Findings

### 1. Annual Total $\text{CO}_2$ Emissions
![Total CO2 Emissions in Zimbabwe](figures/01_zimbabwe_total_co2.png)
- **Observation:** Zimbabwe's total annual $\text{CO}_2$ emissions peaked around the early-to-mid 1990s (reaching roughly 17–18 million tonnes), dipped during the economic contraction of the 2000s, and has gradually rebounded in recent years (reaching ~16–17 million tonnes). Overall, Zimbabwe accounts for less than 0.05% of global annual $\text{CO}_2$ emissions.

### 2. Per Capita $\text{CO}_2$ Emissions
![Per Capita CO2 Emissions in Zimbabwe](figures/02_zimbabwe_per_capita_co2.png)
- **Observation:** While total emissions have recovered toward 1990s levels, per capita emissions have trended downward since the mid-20th century (currently around ~0.8 to 1.0 tonnes per person) because population growth has outpaced the growth in fossil fuel consumption.

### 3. Emissions by Fuel and Industry Type
![CO2 Emissions by Source in Zimbabwe](figures/03_zimbabwe_co2_by_source.png)
- **Observation:** **Coal** is historically and currently the dominant driver of Zimbabwe's $\text{CO}_2$ emissions (primarily due to coal-fired thermal power generation), followed by **oil** (transportation) and smaller contributions from **cement** manufacturing.

## Repository Structure
```text
├── README.md                              # Project documentation and findings
├── zimbabwe_co2_analysis.R                # R script for data cleaning and plotting
└── figures/
    ├── 01_zimbabwe_total_co2.png          # Total emissions line plot
    ├── 02_zimbabwe_per_capita_co2.png     # Per capita area/line plot
    └── 03_zimbabwe_co2_by_source.png      # Emissions by fuel source plot
