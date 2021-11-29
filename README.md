
#### Project Title

# Radiant Earth Spot the Crop Challenge (Sep-2021)

The Radiant MLHub API gives access to open Earth imagery training data for machine learning applications. You can learn more about the repository at the Radiant MLHub site and about the organization behind it at the Radiant Earth Foundation site.

Full documentation for the API is available at docs.mlhub.earth.

Each item in our collection is explained in json format compliant with STAC label extension definition.


## Project structure
├── models\
├── Rishabh_Radiant_Earth_Spot_the_Crop_Model-S2.ipynb\
├── submissions\
├── requirements.txt\
└── License

### Prerequisites

- GPU(s) with 32Gb RAM (e.g. Tesla V100)

```bash
pip install -r requirements.txt
```

### Usage

#### Download and Loading the Data
Download the data from Radiant MLHub and load the properties of each item in the dataset into a DataFrame

#### Description
The dataset for this competition contains a time-series of satellite imagery and labels for crop type that have been collected through aerial and ground survey. Labels are derived from the survey conducted by the Western Cape Department of Agriculture. Satellite data including multispectral Sentinel-2 are then matched with corresponding labels.

#### Variable definitions

The label chips contain the mapping of pixel to crop type label. The following pixel values correspond to the following crop types.
- 0 - No Data
- 1 - Lucerne/Medics
- 2 - Planted pastures (perennial)
- 3 - Fallow
- 4 - Wine grapes
- 5 - Weeds
- 6 - Small grain grazing
- 7 - Wheat
- 8 - Canola
- 9 - Rooibos
- Each label chip also contains a mapping of pixel to field ID. The value of the pixel corresponds to the field ID which the pixel belongs to. These field IDs are the same as the field IDs present in the field_info_(test/train) csv files.

### Summary
 
- Model Quantization
- Unet-like with heavy encoders
- categorical_focal_jaccard_loss