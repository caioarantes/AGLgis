---
title: "AGLgis: A QGIS Plugin for Accessing and Visualizing Processed Sentinel-1 SAR Data"
authors:
  - name: Caio Simplicio Arantes
    orcid: 0009-0006-6926-9368
    affiliation: 1
  - name: Mateus Pinto da Silva
    orcid: 0000-0001-8940-2716
    affiliation: 2
affiliations:
  - name: State University of Campinas (UNICAMP)as (UNICAMP)
    index: 1
  - name: Federal University of Viçosa (UFV)
    index: 2
date: 2025-09-05
bibliography: paper.bib
---

# Summary

AGLgis is an open-source QGIS plugin [@qgis] designed to simplify the preparation and analysis of Sentinel-1 Synthetic Aperture Radar (SAR) Backscatter data [@sentinel1] using Google Earth Engine (GEE) [@earthengine]. The plugin provides a graphical interface for configuring and running the [ee-s1-ard](https://pypi.org/project/ee-s1-ard/) package [@ees1ard], which implements the data processing workflow described by Mullissa et al. (2021) [@mullissa2021], enabling users to process SAR data without writing code. Key features include area selection, date range configuration, border noise correction, terrain flattening, speckle filtering, and export of analysis-ready results. AGLgis aims to make advanced SAR data workflows accessible to a broader geospatial community, supporting research and operational applications in remote sensing.

# Statement of Need

Sentinel-1 SAR data [@sentinel1] is widely used in earth observation for applications such as land cover mapping, flood monitoring, and agricultural analysis. However, preparing analysis-ready SAR data typically requires complex processing steps and programming expertise. AGLgis addresses this gap by integrating the [ee-s1-ard] package [@ees1ard] into QGIS [@qgis], providing a user-friendly interface for non-programmers and researchers to access advanced SAR processing capabilities. The plugin streamlines workflows, reduces barriers to entry, and promotes reproducible research in geospatial science [@earthengine].

# Features

- Graphical interface for area, date, and parameter selection
- Direct integration with Google Earth Engine and the [ee-s1-ard] package
- Support for border noise correction, terrain flattening, and speckle filtering
- VV/VH time series visualization within QGIS
- RGB view and download of VV, VH, and VV/VH bands for selected dates directly in QGIS
- Export of results in analysis-ready formats

The user can select all main processing parameters directly through the plugin's graphical user interface (GUI), making configuration simple and accessible. The supported parameters include geometry (area of interest), temporal range (start and stop dates), polarization options (VV, VH, or VVVH), and processing flags for border noise correction, terrain flattening, and speckle filtering. All parameters have sensible defaults, with VVVH polarization and all correction options enabled by default.

# Implementation

AGLgis is implemented in Python and leverages QGIS's PyQt framework for the user interface [@qgis]. The plugin communicates with Google Earth Engine [@earthengine] via the [ee-s1-ard] package [@ees1ard], handling authentication, data selection, and processing. Users can install the plugin in QGIS and follow the documentation for setup and usage.

# Availability

- Source code: https://github.com/caioarantes/AGLgis
- Documentation: See `index.html` in the repository and online at [GitHub Pages](https://caioarantes.github.io/AGLgis/)
- License: GNU General Public License v2 or later

# Acknowledgements

We thank the QGIS and Google Earth Engine communities for their support and open-source contributions.

# Reference