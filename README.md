# Greener Pastures: 2024-2027 Economic Expansion Roadmap

[![Live Report](https://img.shields.io/badge/View-Live%20Report%20(GitHub%20Pages)-007100?style=for-the-badge&logo=github)](https://andrewsrea.github.io/greener-pastures-case-study/)

## Executive Overview

The **Greener Pastures** project delivers an institutional-grade investment roadmap ranking top U.S. 
Metropolitan Statistical Areas (MSAs) through 2027 based on migration velocity, job growth, and wealth 
gap metrics. By fusing multi-source federal datasets with predictive modeling and spatial analytics,
this study surfaces high-potential regional expansion corridors while rigorously validating 
macroeconomic resilience and downside protection.

---

## Methodology & Tools

This end-to-end data analysis pipeline was built entirely in **R** and rendered into a dynamic 
executive report using **Quarto**.

### Core Analytical Approach

* **Weighted Composite Scoring**: Custom multi-factor ranking model weighing migration velocity (40%), job growth (30%), and wealth gap metrics (30%).
* **Spatial Analytics**: Cartographic boundary mapping using `tigris` and `sf`, leveraging `st_point_on_surface()` to establish reliable points coordinates and `geom_text_repel` for high-density labeling.
* **Resilience Validation**: Pearson correlation analysis ($r = 0.84$) connecting momentum scores directly to historical labor market expansion.
* **Downside Stress Testing**: Scenario-based sensitivity models simulating localized economic and demographic shocks (e.g., Las Vegas, NV) to evaluate structural defense postures.

### Tech Stack & Key R Packages

* **Environment**: Posit Cloud workspace (`R`, `Quarto`)
* **Data Transformation & Mapping**: `dplyr`, `stringr`
* **Spatial Analysis & Mapping**: `sf`, `tigris`
* **Data Visualization**: `ggplot2`, `ggrepel`
* **Reporting & Tables**: `knitr` (`knitr::kable`)

### Authoritative Data Sources

* **U.S. Census Bureau**: Population Estimates (CBSA-MET-EST2024-COMP), American Community Survey (ACS Table S0701 Geographic Mobility and Table B01003 Total Population vintages 2021-2024), and Metropolitan Statistical Area Delineation Files.
* **U.S. Bureau of Economic Analysis (BEA)**: Regional Economic Accounts (CAGDP1 GDP summary and MARPP regional price parities).
* **U.S. Bureau of Labor Statistics (BLS)**: State and Area Employment (SM) time-series flat files (`sm.series`, `sm.area`, and `sm.data.54.TotalNonFarm.All`).

---

## Repository Structure

```text
greener-pastures-case-study/
|--- index.qmd            # Main Quarto executive report document
|--- _quarto.yml          # Quarto configuration and YAML styling options
|--- data/                # Processed and cleaned federal datasets
|--- figures/             # Exported spatial maps and correlation plots
|___ README.md            # Project documentation and executive overview
```

## Author & Contact

**Andrew S. Rea**

*Data Analysis Portfolio Project*

(GitHub Profile)[https://github.com/AndrewSRea]