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
