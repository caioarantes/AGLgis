
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
  - name: Universidade Estadual de Campinas (UNICAMP)
    index: 1
  - name: Universidade Federal de Viçosa (UFV)
    index: 2
repository: https://github.com/caioarantes/AGLgis
archive: https://zenodo.org/record/1234567
keywords:
  - QGIS
  - Google Earth Engine
  - Sentinel-1
  - SAR
  - Remote Sensing
  - Geospatial
  - Plugin
  - Data Preparation
  - Open Source
---

# Summary

AGLgis is an open-source QGIS plugin [@qgis] designed to simplify the preparation and analysis of Sentinel-1 Synthetic Aperture Radar (SAR) Backscatter data [@sentinel1] using Google Earth Engine (GEE) [@earthengine]. The plugin provides a graphical interface for configuring and running the [ee-s1-ard](https://pypi.org/project/ee-s1-ard/) package [@ees1ard], which implements the data processing workflow described by Mullissa et al. (2021) [@mullissa2021], enabling users to process SAR data without writing code. Key features include area selection, date range configuration, border noise correction, terrain flattening, speckle filtering, and export of analysis-ready results. AGLgis aims to make advanced SAR data workflows accessible to a broader geospatial community, supporting research and operational applications in remote sensing.

# Statement of Need

Sentinel-1 SAR data [@sentinel1] is widely used in earth observation for applications such as land cover mapping, flood monitoring, and agricultural analysis. However, preparing analysis-ready SAR data typically requires complex processing steps and programming expertise. AGLgis addresses this gap by integrating the [ee-s1-ard] package [@ees1ard] into QGIS [@qgis], providing a user-friendly interface for non-programmers and researchers to access advanced SAR processing capabilities. The plugin streamlines workflows, reduces barriers to entry, and promotes reproducible research in geospatial science [@earthengine].

# Features

- Graphical interface for area, date, and parameter selection
- Direct integration with Google Earth Engine and the [ee-s1-ard] package
- Support for border noise correction, terrain flattening, and speckle filtering
- Export of results in analysis-ready formats

The user can select all main processing parameters directly through the plugin's graphical user interface (GUI), making configuration simple and accessible. The supported parameters are:

| Parameter                     | Type         | Description                                         | Default      |
|-------------------------------|--------------|-----------------------------------------------------|--------------|
| geometry                      | ee.Geometry  | Area of interest                                    | Required     |
| start_date                    | str          | Start date (YYYY-MM-DD)                             | Required     |
| stop_date                     | str          | End date (YYYY-MM-DD)                               | Required     |
| polarization                  | str          | Polarization (VV, VH, VVVH)                         | VVVH         |
| apply_border_noise_correction | bool         | Apply border noise correction                       | True         |
| apply_terrain_flattening      | bool         | Apply terrain flattening                            | True         |
| apply_speckle_filtering       | bool         | Apply speckle filtering                             | True         |
| output_format                 | str          | Output format (LINEAR, DB)                          | DB           |


# Implementation

AGLgis is implemented in Python and leverages QGIS's PyQt framework for the user interface [@qgis]. The plugin communicates with Google Earth Engine [@earthengine] via the [ee-s1-ard] package [@ees1ard], handling authentication, data selection, and processing. Users can install the plugin in QGIS and follow the documentation for setup and usage [@aglplugin].

# Availability

- Source code: https://github.com/caioarantes/AGLgis
- Documentation: See `index.html` in the repository and online at [GitHub Pages](https://caioarantes.github.io/AGLgis/)
- License: GNU General Public License v2 or later

# Acknowledgements

We thank the QGIS and Google Earth Engine communities for their support and open-source contributions.

# References

