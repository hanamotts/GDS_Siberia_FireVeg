# Predicting wildfire occurrence in Alaska

## Hana Matsumoto

_____

## Project overview

This project will investigate wildfire occurrence in Alaska using predictors such as the underlying vegetation and permafrost type using machine learning.

### **Objectives**

1. Define wildfire incidents, vegetation and permafrost for Alaska
	1. Vegetation: forest type
	2. Permafrost: continuous, discontinuous, sporadic, seasonal
2. Create a basic machine learning model to predict wildfire based on vegetation and permafrost type

### **Datasets**

1. Fire
	1. Incidents
		1. [National Interagency Fire Center (NIFC)](https://data-nifc.opendata.arcgis.com/datasets/nifc::wildland-fire-incident-locations/explore?filters=eyJQT09TdGF0ZSI6WyJVUy1BSyJdfQ%3D%3D&location=65.115524%2C-150.698519%2C8.54)
		2. [FIREDpy](https://github.com/earthlab/firedpy)
			1. More information from [this](https://www.nature.com/articles/s41597-022-01572-3#Sec3) paper
2. Vegetation
	1. [USDA Forest Type](https://data.fs.usda.gov/geodata/rastergateway/forest_type/alaska_forest_type_metadata.php)
3. Permafrost zones
	1. [Data Basin](https://databasin.org/datasets/ad1dff8c39634bedadb4fd40d36ead71/)
### **Python packages**

1. geopandas
2. pandas
3. numpy
4. rasterio
5. matplotlib.pyplot
6. sklearn.preprocessing
1. StandardScaler
7. sklearn.model_selection
1. train_test_split
8. sklearn.linear_model
1. LinearRegression
9. sklearn.ensemble
1. RandomForest
10. sklearn.metrics
1. mean_squared_error
### **Methods**

1. Import fire, forest type and permafrost shapefiles into Jupyter Notebook for analyzing
	1. The forest type raster will need to converted to a shapefile beforehand
2. Clean datasets
3. Determine how to correlate fire incidents to underlying vegetation and permafrost
4. Run linear regression and random forest model to see how accurately the models can predict wildfire occurrence based on permafrost and vegetation alone
5. Add additional feature depending on outcome

### **Expected outcomes**

I expect there to be relatively high correlation values with fire occurence and vegetation. The vegetation classes are closely tied to climatic zones and therefore likely good predictors for fire.

Permafrost may also be a predictor of fire severity because permafrost zones are also controlled by climate and have close relations to vegetation type.

Therefore, I think forest type and permafrost zone might be good features on their own. However, if model performs poorly, climate and Alaskan regional zones may be added as features.