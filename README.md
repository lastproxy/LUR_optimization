# Optimize LUR
Land-use regression (LUR) for modelling nitrogen dioxide (NO2) is optimized through assimilating both ground-based observations (point data) and satellite observations (block data). The ground-based sensor data was collected from the [air quality e-reporting database website][1]. The TROPOMI VCDs were used and downloaded from the [Tropospheric Emission Monitoring Internet Service (TEMIS) website][2].

## lib
The [lib][3] folder contains the scripts for preprocessing, applying the Generalized Likelihood Uncertainty Estimation (GLUE), analyzing the uncertainty, and visualizing the results:

0. Preprocessing
1. Preprocessing & GLUE
2. GLUE
3. Uncertainty analysis

Due to various reasons, all the necessary preprocessed data created by the scripts is provided in the [data][4] folder.

| script     | reason      |
|--------------|-----------|
|0_0_predictor_createCloneMap.py| large size of the predictor maps|
|0_0_predictor_remove_mv.py| large size of the predictor maps|
|0_1_predictor_merge_road345.R| large size of the predictor maps|
|0_2_predictor_normalize.R| large size of the predictor maps|
|1_0_sensor_extract_TROPOMI_predictor.R|large size of the predictor maps|
|2_0_A_LURmodel_GLUE_stochastic_final.R|irreproducible because of the seeds|
|3_0_A_Uncertainty_allStudyArea.py|the processing time|



[1]:https://www.eea.europa.eu/data-and-maps/data/aqereporting-8#tab-figures-produced
[2]:http://www.temis.nl/
[3]:https://github.com/co822ee/LUR_optimization/tree/master/lib
[4]:https://github.com/co822ee/LUR_optimization/tree/master/data
[5]:data.zip