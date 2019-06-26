## Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa

<p align="center">
  <img width="500" height="250" src=/Scripts/Images/Mo3.jpg >
</p>


This project is separated into two scrpts, script 1 of 2 needs the ArcPy module, and thus an ESRI ArcGIS/ArcPro licence to run. Script 2 of 2 does not anc can be run independently. 


Script 1 of 2 contains computational steps used to format existing output from a Tutuila Water Budget Model for use in the Tutuila-wide DIN loading model, which is documented in the report "Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa" as authored by Shuler Hydrologic LLC and delivered to the American Samoa Environmental Protection Agency.

Script 2 of 2, The DIN Loading Module script, contains the computational steps used to develop a Tutuila-wide DIN loading model as documented in the report "Island Wide Nutrient Modeling and Quantification of Coastal Freshwater Discharge for Tutuila, American Samoa" as authored by Shuler Hydrologic LLC and delivered to the American Samoa Environmental Protection Agency. The purpose of posting this project online in an open-source setting is to increase its methodological transparency and make the study entirely reproducible or modifiable as the user’s discretion.

#### The Tutuila Water Budget Model is freely available here: 
https://github.com/UH-WRRC-SWB-model 

   
 
  <p align="left">
  <img width="35" height="35" src=/Scripts/Images/SHLLCLogo.jpg >
</p>


Prepared by:
  Shuler Hydrologic LLC, Honolulu, HI 96826   

Prepared for:
American Samoa Environmental Protection Agency, P.O. Box PPA, Pago Pago, AS 96799

&nbsp;

&nbsp;


# Disclaimer
This script is provided as open-source software on the condition that neither Shuler Hydrologic LLC nor the American Samoa EPA shall be held liable for any damages resulting from the authorized or unauthorized use of the information. No warranty, expressed or implied, is made by Shuler Hydrologic LLC or the American Samoa EPA as to the accuracy and functioning of the program and related program material nor shall the fact of distribution constitute any such warranty and no responsibility is assumed by Shuler Hydrologic LLC in connection therewith. This information is preliminary or provisional and is subject to revision. This software is provided "AS IS." Note that sensitive information, or datasets that are not publically available, are not posted in raw forms. The model code is licensed under the GNU General Public License v3.0 which is an open-access license designed to explicitly affirm any user’s unlimited permission to run, copy, and use the unmodified code from this repository. Please note that some raw datasets used in this work are not owned by the authors and may be subject to other licenses or conditions.

&nbsp;

&nbsp;

## .................................................. HOW TO USE ..................................................
Thanks for your interest in the Tutuila DIN loading model! Please note that this was originally developed as a research project with the intention of aiding local land use managers. It is not a finished product, it is not peer reviewed, and the authors hold no liability for its use or any occurrence resulting as a result of its use.   With that said, here is how the model is organized.

### Folder Organization 

#### Raw Data
This folder holds all of the data used for input files to the model

#### SWB2_results
Because the SWB2 water budget module of the DIN loading model requires an ArcGIS license to run, it was written into a separate script. 
The SWB2 model script generates an output file that is used as input in the DIN loading model script. This folder is where that file is
written by the SWB2 model script and also where it is read as input by the DIN loading model script.

#### Output
This folder is the specified location to where the model will save (or overwrite) the model output files. These include GIS
shapefile, Figures, and currently a tabular data file.


#### Scripts
This is where the actual model scripts are located. They are in .ipynb format and can be rendered directly in your browser
by clicking on them. This will open a read only version where you can see all the steps calculations, and output figures from 
the modeling process. As stated above the SWB2 model script is separated from the Loading Model due to needing the ArcGIS/ArcPy
module to run.



 ### To run the model   

The whole repository can be downloaded the "clone or download" button on the repository home page can be clicked, and the
repository with all input files, all scripts, and all previously generated outputs will be available for download. 
The scripts are written in Python 3.7 and compiled with Jupyter notebook. Once the user opens an instance of Jupyter Notebooks 
on a computer or server with the appropriate environment installed, they can dynamically interact with the model scripts by 
opening "R2R_DIN_loading_model_Final.ipynb" or "R2R_SWB2_post-processing_Final.ipynb". The model will save any new outputs in the
location of the relative paths in the local copy of the cloned model repository


#### Environment
The Repository contains an environment.yml file that contains a list of all the modules necessary to run the script.
The Anaconda distribution (https://www.anaconda.com/) provides the ability to create the appropriate environment from the .yml file. 

dependencies:
  - python
  - numpy
  - matplotlib
  - pandas
  - scipy
  - notebook 
  - geopandas
  - statsmodels
  - xlrd
