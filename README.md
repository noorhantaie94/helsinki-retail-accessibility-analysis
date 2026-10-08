#  Spatial Accessibility & Dominance Areas Analysis

This repository contains the completed solutions for **Exercise 4** of the *Automating GIS Processes* course. The exercise focuses on analyzing travel time matrix datasets, determining spatial accessibility, and mapping shopping centre dominance areas in the Helsinki Metropolitan Area using Python and GeoPandas.

---

##Project Overview

The main objective of this exercise is to work with multi-source spatial data and travel time matrices to perform accessibility modeling:

* * 1: Shopping Centre Accessibility**
  * Integrated YKR grid data with travel time datasets for specific shopping centres (*Itis* and *Myyrmanni*).
  * Classified public transport travel times using custom bin ranges and visualized accessibility patterns across the metropolitan region.
  * Generated output plot: `data/shopping_centre_accessibility.png`.

* *2: Shopping Centre Dominance Areas**
  * Loaded and processed travel time matrices for all 7 major shopping centres (*Dixi, Forum, Iso Omena, Itis, Jumbo, Myyrmanni, Ruoholahti*).
  * Handled missing data (`-1` values representing unreachable cells) by converting them to `NaN`.
  * Computed the minimum travel time (`min_t`) to any shopping centre for every grid cell.
  * Identified the closest/dominant shopping centre (`dominant_service`) per grid cell using `idxmin()`.
  * Visualized the results using a $2 \times 1$ subplot map comparing dominance areas and minimum travel times.
  * Generated output plot: `data/dominance_areas.png`.

---

##  Repository Structure

```text
exercise-4-main/
│
├── data/
│   ├── YKR_grid_EPSG3067.gpkg          # YKR Grid Shapefile/GeoPackage
│   ├── travel_times_to_*.txt           # Travel time matrices for shopping centres
│   ├── shopping_centre_accessibility.png # Output map for Problem 1
│   └── dominance_areas.png              # Output map for Problem 2
│
├── Exercise-4-problem-1.ipynb          # Jupyter Notebook for Problem 1
├── Exercise-4-problem-2.ipynb          # Jupyter Notebook for Problem 2
├── .gitignore                          # Git ignore configuration
└── README.md                           # Project documentation
