# KS Field Dataset (2022) + Site Locations (2022–2023)

This repository provides a subset of field observations used in our maize canopy
biophysical parameter study. The shared materials include (i) an Excel workbook
with biophysical measurements and (ii) point shapefiles describing site locations
for 2022 and 2023.

> **Scope note**: The 2022 KS-related and 2023 SPAD dataset are fully shared here.
> Additional years/sites can be made available by the corresponding author upon
> reasonable request, subject to project/data management constraints.
---

## Contents

### 1) Tabular data
- `data.xlsx`  
  Multi-sheet field dataset with the following sheets:
  - `Height` (2022-06-19 to 2022-09-25)
  - `LAI` (2022-06-19 to 2022-09-25)
  - `FVC` (2022-06-19 to 2022-09-25)
  - `SPAD` (2023-06-12 to 2023-09-20)
  - `Biomass` (2022-06-19 to 2022-09-23)

### 2) Spatial data (site/plot point locations)
Shapefile sets (each set includes `.shp .shx .dbf .prj .cpg`):
- `2022sites_sign.*` – site locations for 2022
- `2023sites_sign.*` – site locations for 2023

CRS: **CGCS2000 / EPSG:4490** (geographic coordinates).
---

## Data Description (data.xlsx)

### Common fields
- **Date**: Observation date in `YYYYMMDD` numeric format (e.g., `20220619`).
- **Site / Sites**: Site/plot identifier (e.g., `Y1`, `Y2`, ...).
Missing values may appear as blank cells (Excel empty) depending on sheet.
---

### Sheet: `LAI`
Leaf Area Index observations at multiple points.
- **Columns**
  - `Date`, `Site`
  - `Point 1` ... `Point 6`: LAI at each sampling point (unitless)
---

### Sheet: `Height`
Plant height measurements with a reference LAI column.
- **Columns**
  - `Date`, `Site`
  - `LAI`: site-level LAI value associated with the height record (unitless)
  - `Point 1` ... `Point 6`: plant height at each sampling point (unit: see manuscript; commonly cm)
---

### Sheet: `FVC`
Fractional Vegetation Cover.
- **Columns**
  - `Date`, `Site`
  - `Point 1` ... `Point 6`: FVC at each sampling point (range 0–1)
---

### Sheet: `SPAD`
SPAD meter readings (chlorophyll proxy) recorded at canopy layers.
- **Columns**
  - `Date`, `Site`
  - `Point 1 top layer` ... `Point 6 top layer`
  - `Point 1middle layer` ... `Point 6middle layer`
  - `Point 1 down layer` ... `Point 6 down layer`
- **Units**
  - SPAD values are instrument units (unitless index)
---

### Sheet: `Biomass`
Above-ground biomass components for stem and leaf at point level.
- **Columns**
  - `Date`
  - `Sites`: site/plot identifier
  - `Point`: sampling point index
  - `FAGB Stem (kg/m2)`
  - `AGB Stem (kg/m2)`
  - `FAGB Leaf (kg/m2)`
  - `AGB Leaf (kg/m2)`
- **Notes**
  - Variable definitions (e.g., whether AGB refers to dry mass) follow the manuscript.
---

## Spatial Data Description (2022sites_sign.*, 2023sites_sign.*)

The shapefiles store point geometries with associated attributes (field names may
include):
- `O_Name`: point label/index
- `O_Lat`, `O_Lng`: latitude/longitude (degrees)
- `O_Alt`: altitude (if provided; often 0 in this dataset)
- `O_Com`: comment/label (may include non-ASCII characters depending on encoding)

CRS information is included in the `.prj` file. Recommended to open in:
- QGIS / ArcGIS / GeoPandas
---

## Reproducibility & Method Disclosure

Stage-specific LAI-based regression equations used in SRM are provided in the
manuscript Appendix:
- **Appendix A2. Stage specific LAI based regression equations used in SRM**

We do not release the full implementation code at this stage. Please contact the
corresponding author if additional technical details are required for academic
verification.

---

## How to Use

- For tabular data: open `data.xlsx` directly or export each sheet to CSV.
- For spatial data: load `2022sites_sign.shp` / `2023sites_sign.shp` in GIS software.
---

## Citation

If you use this dataset, please cite:
- **[Haiye yu, Bingze Li, Yuanyuan Sui]**, **[2026]**. *Improved stage specific parameterization for maize canopy biophysical parameters based on LAI trajectory segmentation*.
  GitHub repository: **[INSERT REPOSITORY URL]**.

(The DOI will be provided later.)

---

## License

Data and documentation in this repository are released under **CC BY 4.0**
unless otherwise stated. See `LICENSE`.

---

## Contact

Corresponding author: **[Yuanyuan Sui]**  
Email: **[suiyuan@jlu.edu.cn]**  
Affiliation: **[School of Biological and Agricultural Engineering, Jilin University, 130022, Changchun, China]**

---
