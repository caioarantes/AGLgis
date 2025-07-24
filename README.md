## AGLgis
AGLgis is a graphical interface designed to simplify the use of the [Sentinel-1 SAR Backscatter Analysis Ready Data Preparation in Google Earth Engine](https://pypi.org/project/ee-s1-ard/) package in QGIS.  
This plugin allows users to configure and run Sentinel-1 SAR data processing without the need to write code.

### Main features

- Graphical interface for selecting area, dates, and processing parameters.
- Direct integration with the `ee-s1-ard` package, making the workflow more accessible.
- Support for border noise correction, terrain flattening, and speckle filtering.
- Export of results ready for analysis and visualization.

### Parâmetros suportados

| Parâmetro                      | Tipo         | Descrição                                   | Padrão   |
|--------------------------------|--------------|---------------------------------------------|----------|
| geometry                       | ee.Geometry  | Área de interesse                           | Obrigatório |
| start_date                     | str          | Data inicial (YYYY-MM-DD)                   | Obrigatório |
| stop_date                      | str          | Data final (YYYY-MM-DD)                     | Obrigatório |
| polarization                   | str          | Polarização (VV, VH, VVVH)                  | VVVH     |
| apply_border_noise_correction  | bool         | Corrigir ruído de borda                     | True     |
| apply_terrain_flattening       | bool         | Aplainamento de terreno                     | True     |
| apply_speckle_filtering        | bool         | Filtragem de speckle                        | True     |
| output_format                  | str          | Formato de saída (LINEAR, DB)               | DB       |
