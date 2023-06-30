Simón Román - Data Science bootcamps Capstone project - London (June 2023)

This repository contains code and documentation for performing time series analysis to predict electricity consumption for Great Britain by using time series analysis from data gathered in the UK from January 1, 2009 to March 12, 2023. 

1. Dataset
The dataset used for the time series analysis can be found in the data directory in a csv file called `historic_demand_2009_2023_noNaN.csv`.

The data used for the time series was sourced form the National Grid webpage and included, in general terms, energy demand, energy import and export flows and wind and solar capacity and generation. The data consisted of 48 daily measurements in 30-minute intervals and ranged from January 1, 2009, until January 1, 2023.

The following is the description of each column in the dataset as described by the ESO. 

Column summary: 
- SETTLEMET_DATE: date in format dd/mm/yyyy [original df]
- SETTLEMENT_PERIOD: half hourly period for the historic outtunr occurred
- ND (National Demand). National Demand is the sum of metered generation, but excludes generation required to meet station load, pump storage pumping and interconnector exports. . Measured in MW.
- TSD (Transmission System Demand). Transmission System Demand is equal to the ND plus the additional generation required to meet station load, pump storage pumping and interconnector exports. Measured in MW.
- ENGLAND_WALES_DEMAND. England and Wales Demand, as ND above but on an England and Wales basis. Measured in MW.
- EMBEDDED_WIND_GENERATION. This is an estimate of the GB wind generation from wind farms which do not have Transmission System metering installed. These wind farms are embedded in the distribution network and invisible to National Grid ESO. Their effect is to suppress the electricity demand during periods of high wind. The true output of these generators is not known so an estimate is provided based on National Grid ESO’s best model. Measured in MW.
- EMBEDDED_WIND_CAPACITY. This is National Grid ESO’s best view of the installed embedded wind capacity in GB. This is based on publicly available information compiled from a variety of sources and is not the definitive view. It is consistent with the generation estimate provided above. Measured in MW
- EMBEDDED_SOLAR_GENERATION. This is an estimate of the GB solar generation from PV panels. These are embedded in the distribution network and invisible to National Grid ESO. Their effect is to suppress the electricity demand during periods of high radiation. The true output of these generators is not known so an estimate is provided based on National Grid ESO’s best model. Measured in MW.
- EMBEDDED_SOLAR_CAPACITY. As embedded wind capacity above, but for solar generation. Measured in MW.
- NON_BM_STOR (Non-Balancing Mechanism SHort-Term Operating Reserve). For units that are not included in the ND generator definition. This can be in the form of generation or demand reduction. Measured in MW.
- PUMP_STORAGE_PUMPING. The demand due to pumping at hydro pump storage units; the -ve signifies pumping load.
- IFA_FLOW (IFA Interconnector Flow). The flow on on the respective interconnector. -ve signifies export power out from GB; +ve signifies import power into GB. Measured in MW.
- IFA2_FLOW (IFA Interconnector Flow). The flow on the respective interconnector. -ve signifies export power out from GB; +ve signifies import power into GB. Measured in MW.
MOYLE_FLOW (Moyle Interconnector FLow). The flow on the respective interconnector. -ve signifies export power out from GB; +ve signifies import power into GB. Measured in MW.
- EAST_WEST_FLOW (East West Innterconnector Flow). The flow on the respective interconnector. -ve signifies export power out from GB; +ve signifies import power into GB. Measured in MW.
- NEMO_FLOW (Nemo Interconnector FLow). The flow on the respective interconnector. -ve signifies export power out from GB; +ve signifies import power into GB. Measured in MW.
- NSL_FLOW (North Sea Link Interconnector Flow). The flow on the respective interconnector. -ve signifies export power out from GB; +ve signifies import power into GB. Measured in MW.

2. Notebooks. The project is comprised of six notebooks:
    1. `01-data-loading-cleaning-capston.ipynb` in which data is loaded and some changes are made. 
    2. `02-eda-capstone_electriciy_sro.ipynb` in which general EDA an visualizations are performed.
    3. `03-preprocessing-and-baseline models.ipynb`
    4. `04-modeling.ipynb` 
    5. `05-model-analysis.ipynb`
    6. `06-validation-data.ipynb` This notebook contains some data wrangling. 

3. Results
The results of the time series analysis are in notebook `05-model-analysis` and in a business report in the `reports` folder. 

4. Conda environment file is located on the `env` folder as: environment.yml

5. To access the pickled files, data and notebooks access this: https://drive.google.com/drive/folders/1REK5tR_iMnRtSMoJFmaiMva78qFrI2Bh?usp=sharing

The pickled files that are used in notebooks 04 and 05 are located on the `model` folder. 

Data stored from the notebooks is located on the `data` folder. 

Contact
For any questions or inquiries, please contact Simón Román at [simon.roman@gmail.com].

Feel free to explore and adapt this time series analysis code to fit your specific dataset and analysis requirements. 