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
  - name: State University of Campinas (UNICAMP)
    index: 1
  - name: Universidade Federal de Viçosa (UFV)
    index: 2
date: 2025-09-05
bibliography: paper.bib
---

# Summary

AGLgis is an open-source QGIS plugin [@qgis] designed to simplify the preparation and analysis of Sentinel-1 Synthetic Aperture Radar (SAR) Backscatter data [@sentinel1] using Google Earth Engine (GEE) [@earthengine]. The plugin provides a graphical interface for configuring and running the [ee-s1-ard](https://pypi.org/project/ee-s1-ard/) package [@ees1ard], which implements the data processing workflow described by Mullissa et al. (2021) [@mullissa2021], enabling users to process SAR data without writing code. Key features include area selection, date range configuration, border noise correction, terrain flattening, speckle filtering, and export of analysis-ready results. AGLgis aims to make advanced SAR data workflows accessible to a broader geospatial community, supporting research and operational applications in remote sensing.

# Statement of Need

Sentinel-1 SAR data [@sentinel1] can be used in earth observation for land cover mapping, flood monitoring, and agricultural analysis. Pre-processing SAR data may require multiple processing steps and familiarity with tools like Google Earth Engine's Code Editor, which can be a barrier for users without programming experience. AGLgis bridges this gap by integrating the [ee-s1-ard] package [@ees1ard] into QGIS [@qgis], offering a graphical interface that enables non-programmers and researchers to access SAR processing workflows. This approach streamlines data preparation, lowers the barrier to entry, and supports reproducible research in geospatial science [@earthengine].


# Features and Demonstration

The main capabilities and results include:

- Selection of area of interest and date range
- Automated border noise correction, terrain flattening, and speckle filtering
- Interactive visualization of VV/VH time series and RGB composites within QGIS, where VV, VH, and VV/VH ratios are mapped to the red, green, and blue channels.
- Direct and batch download of processed bands cliped to area of interest.

All major processing parameters—geometry, temporal range, polarization, and correction options are accessible via the plugin's interface.

The figures below illustrate the plugin's interface and typical results:

![Oveview tab for setting selection](medias/view.png)

![Demonstration of AGLgis results: time series visualization and RGB view](medias/demo.png)

# Implementation

AGLgis is implemented in Python and leverages QGIS's PyQt framework for the user interface [@pyqt]. The plugin communicates with Google Earth Engine [@earthengine] (which requires authenticatin and a Google Cloud Project) and applies the  [ee-s1-ard] package [@ees1ard], handling data selection, and processing. Users can install the plugin in QGIS and follow the documentation for setup and usage.

# Availability

- Source code: [https://github.com/caioarantes/AGLgis](https://github.com/caioarantes/AGLgis)
- Documentation: Online at [GitHub Pages](https://caioarantes.github.io/AGLgis/)
- License: GNU General Public License v2 or later

# Acknowledgements

We thank the QGIS and Google Earth Engine communities for their support and open-source contributions.

# Reference