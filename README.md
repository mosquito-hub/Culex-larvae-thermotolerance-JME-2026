# Culex Larval Nutrient Analysis — Gregory *et al.* 2026

This repository contains the R Markdown notebooks used to generate the nutrient analysis figures and statistics presented in **Figure 5** of:

> Gregory *et al.*, "Stage-specific divergence in larval thermal tolerance among populations of the *Culex pipiens* Assemblage." *Journal of Medical Entomology*, accepted for publication June 18, 2026.

The analyses characterize protein, glycogen, total lipid, and triglyceride content of *Culex pipiens* assemblage larvae across five populations (Florida, Maine, Texas, and Illinois Above-Ground/Below-Ground forms) reared on a common diet.

## Repository contents

| File | Description |
|---|---|
| `Culex_Colorimetry_analysis_Gregory-et-al-2026.Rmd` | Principal component analysis (PCA) of the four nutrient measures, generalized linear models (GLMs) testing effects of region of origin and nutrient type (with *post-hoc* pairwise comparisons via `emmeans`), and stacked bar plots of proportional nutrient composition by population. |
| `Nutrient_analysis_Gregory-et-al-2026.Rmd` | Generates the dot/box/violin plots for each individual nutrient (protein, glycogen, total lipids, triglycerides) by population, as shown in Figure 5. |

## Data requirements

The notebooks expect raw data files (included in this repository) to be placed in the same working directory as the `.Rmd` files:

**`Culex_Colorimetry_analysis_Gregory-et-al-2026.Rmd`** requires:
- `Culex_Colorimetry_Data - Gregory et al 2026.xlsx`

**`Nutrient_analysis_Gregory-et-al-2026.Rmd`** requires:
- `Culex_Protein_July2025.xlsx`
- `Culex_Glycogen_July2025.xlsx`
- `Culex_Total Lipids_July2025.xlsx`
- `Culex_Triglycerides_July2025.xlsx`

## Requirements

These notebooks were developed in R and require the following packages:

```r
install.packages(c(
  "tidyverse",
  "readxl",
  "lme4",
  "emmeans",
  "ggfortify",
  "ggbiplot",
  "dplyr",
  "ggpubr",
  "ggplot2"
))
```

`ggbiplot` may need to be installed from GitHub:

```r
remotes::install_github("vqv/ggbiplot")
```

## Usage

1. Clone this repository and place the required `.xlsx` data files in the same directory as the notebooks.
2. Open the desired `.Rmd` file in RStudio.
3. If needed, uncomment and run the `setwd()` line at the top of each notebook to set the working directory to the notebook's location.
4. Knit the notebook or run chunks interactively to reproduce the analyses and figures.

## Citation

If you use these scripts, please cite:

> Gregory *et al.* (2026). Stage-specific divergence in larval thermal tolerance among populations of the *Culex pipiens* Assemblage. *Journal of Medical Entomology*.

## Authors

- Helle Aronson
- Clément Vinauger
