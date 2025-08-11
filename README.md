## AGLgis

AGLgis is a graphical interface designed to simplify the use of the [Sentinel-1 SAR Backscatter Analysis Ready Data Preparation in Google Earth Engine](https://pypi.org/project/ee-s1-ard/) package in QGIS.  

This plugin allows users to configure and run Sentinel-1 SAR data processing without the need to write code.

### Main features

- Graphical interface for selecting area, dates, and processing parameters.
- Direct integration with the `ee-s1-ard` package, making the workflow more accessible.
- Support for border noise correction, terrain flattening, and speckle filtering.
- Export of results ready for analysis and visualization.

### Supported Parameters

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
