# Rationale

This page aims to document the mapping and visualisation of the example dataset taken from a [camera trap study](https://lifemica.eu/research-innovaties/camera-tracking/) `MICA - Muskrat and coypu camera trap observations in Belgium, the Netherlands and Germany`.
This study is designed to detect invasive muskrat and coypu populations in Belgium, the Netherlands and Germany. The mapping and visualisation is developed for the workshop on managing sampling Event data flows in GBIF, in May 2024, Ithaca, US. The example dataset is thoroughly documented [here](https://camtrap-dp.tdwg.org/example/) and can be downloaded as a camtrapDP package.

This repository contains the functionality to standardize the raw data to:
- a camtrap DP package
- a Darwin Core Event schema
- a Darwin Core Occurrence schema

Each mapping includes a diagram to facilitate the visualization of the data.

# Repo structure

```
├── README.md              : Description of this repository
├── LICENSE                : Repository license
├── camera-trap-data.Rproj : RStudio project file
├── .gitignore             : Files and directories to be ignored by git
│
├── data                
│   ├── camtrapDP
│   └── dwc_event
|   └── dwc_occurrence
|
├── src
│   ├── dwc_mapping.Rmd    : Darwin Core mapping script
```




