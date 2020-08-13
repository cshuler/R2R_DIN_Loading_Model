[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3462869.svg)](https://doi.org/10.5281/zenodo.3462869)


### Please note that, although published this project is dynamic and thus is subject to revision.
Published article is archived [Here:](https://link.springer.com/article/10.1007/s00267-020-01314-4)

Preprint article is archived [Here:](https://www.preprints.org/manuscript/202003.0101/v1)

## Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa

<p align="center">
  <img width="500" height="250" src=/Docs/Figs/Results_Prioritization_Rank.jpg >
</p>

For Model Ouptuts click [here!](Final_products):


### Executive Summary
Excessive nutrient discharge to tropical island coastlines can cause algal blooms and eutrophication. To address these issues, environmental regulatory agencies often set water quality standards for discharging surface waters. However, such standards typically only consider surface water nutrient concentrations, which do not account for groundwater discharge, variability in flow, or dilution effects. Calculation of nutrient loads by multiplying concentrations of nutrients or other constituents in discharging waters by volumetric rates of water discharge, can provide better predictions of water quality conditions that influence nearshore biota, and may be a more accurate indicator of terrestrial impact. This report documents the development and application of an island-wide dissolved inorganic nitrogen (DIN) loading model for the island of Tutuila, in the Territory of American Samoa.
The DIN loading model integrates island-wide water quality information from extensive water sampling data with water flux estimates derived from an open-source water budget model and publically available streamflow data. The model workflow used observed DIN loading rates from all hydrologic pathways in watersheds where sufficient samples were available as model calibration data. The three hydrologic pathways considered were (1) stream baseflow from shallow aquifers, (2) surface runoff generated during rainfall events, and (3) submarine groundwater discharge (SGD). The anthropogenic DIN sources included in the model were on-site wastewater disposal systems (OSDS), livestock pigs, and synthetic fertilizer inputs to agricultural lands. Measurements of historical and contemporary stream flow were also assessed to (1) validate water-budget calculated surface runoff rates, and (2) separate baseflow and SGD rates from water-budget calculated net-infiltration in ungauged watersheds.
Final island-wide DIN loading rates were optimized by calibrating individual N-release rates for different modeled nutrient source types on Tutuila with the observed DIN loading rates in each fully sampled watershed. Overall, model results indicated SGD is an important coastal delivery mechanism for terrigenous N, that OSDS units are the predominant anthropogenic source of DIN to Tutuila’s coastal waters, and that the Tafuna-Leone Plain, various watersheds in the Pago Harbor area, the Tula region, and areas down gradient from Aasu and Aoloau Villages are likely hot-spots for coastal nutrient impacts.


## How to Use the model

### If you are interested in outputs only please see the output shapefile and results table [Here](Final_products): 
Otherwise familiarity with Jupyter Notebooks and Python will allow for more in-depth exploration of the model. 

This project is separated into two scrpts, script 1 of 2 needs the ArcPy module, and thus an ESRI ArcGIS/ArcPro licence to run. Script 2 of 2 does not anc can be run independently. 


#### Script 1 of 2  -   "R2R_SWB2_post-processing_Final.ipynb"
Contains computational steps used to format existing output from a Tutuila Water Budget Model for use in the Tutuila-wide DIN loading model, which is documented in the report "Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa" as authored by Shuler Hydrologic LLC and delivered to the American Samoa Environmental Protection Agency.

###### The Tutuila Water Budget Model is freely available at:  https://github.com/UH-WRRC-SWB-model 

#### Script 2 of 2  -   "R2R_DIN_loading_model_Final.ipynb"
Is the DIN Loading Module script, contains the computational steps used to develop a Tutuila-wide DIN loading model as documented in the report "Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa" as authored by Shuler Hydrologic LLC and delivered to the American Samoa Environmental Protection Agency. The purpose of posting this project online in an open-source setting is to increase its methodological transparency and make the study entirely reproducible or modifiable as the user’s discretion.

  
&nbsp;

&nbsp;


## Model Methods: 

We developed a method to assess nutrient loads by integrating commonly available datasets within a geospatial modeling framework for Tutuila, American Samoa.  The DIN loading model used an open-source water budget model, water sampling data, and publically available streamflow data to predict watershed-scale DIN loading to the island’s entire coastline. The Tutuila DIN loading model considered three hydrologic pathways including (1) stream base flow from shallow aquifers, (2) surface runoff generated during rainfall events, and (3) submarine groundwater discharge (SGD) across the ocean-land interface into the ocean.

 ### SWB calculated baseflow, Surface Runoff, and SGD
<p align="center">
  <img width="900" height="145" src=/Docs/Figs/SWB_spatial_3pathways.jpg >
</p>
 
&nbsp;

&nbsp;


### Geospatial definition of terrestrial Dissolved Inorganic Nitrogen (DIN) sources
The SWB2 calculated water fluxes, calulated at the watershed scale, we then geospatially combined with four geospatial maps representing terrestrial DIN sources as defined by Shuler et al. 2017. Three of these were anthropogenic drivers On-Site Wastewater Disposal Systems (OSDS), piggeries, and agricultural fertilizer input. DIN from natural sources was also considered. To resolve the spatial distribution of anthropogenic DIN sources to a watershed scale, we mapped locations of every OSDS unit, every pig, and all known agricultural land and geospatially intersected these anthropogenic DIN sources to watershed boundaries. DIN release rates from each source were determined through model calibration for the equivalent source-activities on Tutuila. These rates were 0.021 kg-DIN/day per OSDS unit, 0.0381 kg-DIN/day per pig, and 0.77 kg-DIN/day per km2 of agricultural land (Shuler et al. 2017).

  
 <p align="center">
  <img width="700" height="380" src=/Docs/Figs/DIN_sources_land_use.jpg >
 </p>


  
&nbsp;

&nbsp;

### Model calibration 

The model was calibrated by parameterizing an individual DIN release rate for each of the anthropogenic sources. Parameter optimization was performed using the Nelder-Mead unconstrained minimization method, and observation data in the form of watershed scale DIN loads,  were calculated by multiplying measured DIN concentrations with water discharge rates. Measured DIN concentrations were from a total of 424 individual stream samples that were collected from 38 individual stream sites and 26 coastal springs at a monthly interval for a one-year period from September 2016 to September 2017 (Comeros-Raynal et al 2018). 


<p align="center">
  <img width="700" height="380" src=/Docs/Figs/Watershed_sampling_map.jpg >
</p>
 
##### Locations of stream and coastal spring sample sites shown as circles and triangles, respectively, with shaded model watersheds draining to each site. Model designated watershed ID numbers are also shown for reference. 


&nbsp;

&nbsp;


## Model Results
The optimization routine provided calibrated values for DIN release rates from each of the three anthropogenic nutrient sources accounted for in the model by minimizing error between observed and modeled watershed-scale DIN loading rates. Multiplication of these release rates by the number of anthropogenic DIN sources in each watershed yielded absolute loading rates ranging from 0.1 kg-DIN/day for some of the smallest watersheds, to 88.2 kg-DIN/day for the largest watershed on the Tafuna-Leone Plain. 

<p align="center">
  <img width="800" height="400" src=/Docs/Figs/Results_Absolute_DIN_loads.jpg >
</p>
 
##### Comparisons between modeled DIN loading rates as separated by each nutrient source. Upper left panel shows total modeled DIN loads from all sources, and the other three panels (clockwise from upper right) show the absolute magnitude of DIN loaded to each watershed from OSDS units, pigs, and agriculture, respectively.


### For interpretation, these coastal DIN loading rates were also scaled by watershed area:

<p align="center">
  <img width="600" height="300" src=/Docs/Figs/Results_AreaScaled_DIN_loads.jpg >
</p>
 

##### Relative model calculated DIN loading rates for each watershed scaled by sub watershed area, in kg-DIN/day per km2 of land and Numbers within watersheds show each of the DIN loads in kg/day/km2.

### and by length of watershed coastline


<p align="center">
  <img width="600" height="300" src=/Docs/Figs/Results_CoastlineScaled_DIN_loads.jpg >
</p>
 
##### Relative model calculated DIN loading rates for each watershed, scaled by length of watershed shoreline in kg-DIN/day per km of coastline. Numbers within watersheds show each of the DIN loads in kg/day/km.


&nbsp;

&nbsp;


### Impact Prioritization Ranking 
Each of the above three ways of scaling DIN loading provides a different and unique presentation of impacts, while at the same time being limited by different biases. Thus, to simplify model results and aid coastal managers, a single watershed prioritization scheme was developed. Thus, to simplify model results and aid coastal managers, a single watershed prioritization scheme was developed. This scheme incorporates each of the three aforementioned loading metrics, and weights them equally in the output. 

<p align="center">
  <img width="700" height="350" src=/Docs/Figs/Results_Prioritization_Rank.jpg >
</p>


##### Relative impact prioritization through equal-weight ranking of absolute, area-scaled, and coastline length-scaled DIN fluxes from each watershed to the nearshore. Both colors and numeric labels in watersheds indicate the DIN impact prioritization ranking in each watershed with 1 being the most impacted and 93 the least. Note that if two watersheds had the same final score they were assigned the same rank number; thus some numbers are repeated. 



&nbsp;

&nbsp;



# Disclaimer
This script is provided as open-source software on the condition that neither Shuler Hydrologic LLC nor the American Samoa EPA shall be held liable for any damages resulting from the authorized or unauthorized use of the information. No warranty, expressed or implied, is made by Shuler Hydrologic LLC or the American Samoa EPA as to the accuracy and functioning of the program and related program material nor shall the fact of distribution constitute any such warranty and no responsibility is assumed by Shuler Hydrologic LLC in connection therewith. This information is preliminary or provisional and is subject to revision. This software is provided "AS IS." Note that sensitive information, or datasets that are not publically available, are not posted in raw forms. The model code is licensed under the GNU General Public License v3.0 which is an open-access license designed to explicitly affirm any user’s unlimited permission to run, copy, and use the unmodified code from this repository. Please note that some raw datasets used in this work are not owned by the authors and may be subject to other licenses or conditions.


&nbsp;

&nbsp;

###### This project was prepared for:
the American Samoa Environmental Protection Agency, P.O. Box PPA, Pago Pago, AS 96799

###### And was prepared by:
Shuler Hydrologic LLC, Honolulu, HI 96826   




  <p align="center">
  <a href="https://sites.google.com/site/shulerhydrologicllc/"><img src=/Scripts/Images/SHLLCLogo.jpg width="82" height="86" title="White flower" alt="Flower"></a>
  </p>
