[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3462869.svg)](https://doi.org/10.5281/zenodo.3462869)


### Please note that all information contained in this repository is preliminary or provisional and is subject to revision

## Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa

<p align="center">
  <img width="500" height="250" src=/Scripts/Images/Mo3.jpg >
</p>


### Executive Summary
Excessive nutrient discharge to tropical island coastlines can cause algal blooms and eutrophication. To address these issues, environmental regulatory agencies often set water quality standards for discharging surface waters. However, such standards typically only consider surface water nutrient concentrations, which do not account for groundwater discharge, variability in flow, or dilution effects. Calculation of nutrient loads by multiplying concentrations of nutrients or other constituents in discharging waters by volumetric rates of water discharge, can provide better predictions of water quality conditions that influence nearshore biota, and may be a more accurate indicator of terrestrial impact. This report documents the development and application of an island-wide dissolved inorganic nitrogen (DIN) loading model for the island of Tutuila, in the Territory of American Samoa.
The DIN loading model integrates island-wide water quality information from extensive water sampling data with water flux estimates derived from an open-source water budget model and publically available streamflow data. The model workflow used observed DIN loading rates from all hydrologic pathways in watersheds where sufficient samples were available as model calibration data. The three hydrologic pathways considered were (1) stream baseflow from shallow aquifers, (2) surface runoff generated during rainfall events, and (3) submarine groundwater discharge (SGD). The anthropogenic DIN sources included in the model were on-site wastewater disposal systems (OSDS), livestock pigs, and synthetic fertilizer inputs to agricultural lands. Measurements of historical and contemporary stream flow were also assessed to (1) validate water-budget calculated surface runoff rates, and (2) separate baseflow and SGD rates from water-budget calculated net-infiltration in ungauged watersheds.
Final island-wide DIN loading rates were optimized by calibrating individual N-release rates for different modeled nutrient source types on Tutuila with the observed DIN loading rates in each fully sampled watershed. Overall, model results indicated SGD is an important coastal delivery mechanism for terrigenous N, that OSDS units are the predominant anthropogenic source of DIN to Tutuila’s coastal waters, and that the Tafuna-Leone Plain, various watersheds in the Pago Harbor area, the Tula region, and areas down gradient from Aasu and Aoloau Villages are likely hot-spots for coastal nutrient impacts.


#### Use of the model

This project is separated into two scrpts, script 1 of 2 needs the ArcPy module, and thus an ESRI ArcGIS/ArcPro licence to run. Script 2 of 2 does not anc can be run independently. 


#### Script 1 of 2  -   "R2R_SWB2_post-processing_Final.ipynb"
Contains computational steps used to format existing output from a Tutuila Water Budget Model for use in the Tutuila-wide DIN loading model, which is documented in the report "Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa" as authored by Shuler Hydrologic LLC and delivered to the American Samoa Environmental Protection Agency.

###### The Tutuila Water Budget Model is freely available at:  https://github.com/UH-WRRC-SWB-model 

#### Script 2 of 2  -   "R2R_DIN_loading_model_Final.ipynb"
Is the DIN Loading Module script, contains the computational steps used to develop a Tutuila-wide DIN loading model as documented in the report "Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa" as authored by Shuler Hydrologic LLC and delivered to the American Samoa Environmental Protection Agency. The purpose of posting this project online in an open-source setting is to increase its methodological transparency and make the study entirely reproducible or modifiable as the user’s discretion.

  
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
