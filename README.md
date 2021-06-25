# mfr_dl


This python package is used for space weather research.  We try to predict the magnetic field of the magnetic flux rope (MFR) within an interplanetary coronal mass ejection (ICME) at Earth (L1) with machine learning algorithms.

by Martin Reiss, U.V. Amerstorfer, Hannah Rüdisser, R. L. Bailey, and [C. Möstl](https://www.iwf.oeaw.ac.at/en/user-site/christian-moestl/), IWF Graz, Austria.

Current status (June 2021): **Work in progress!** 

If you want to use parts of this code for generating results for peer-reviewed scientific publications, 
please contact us per email (christian.moestl@oeaw.ac.at) or via https://twitter.com/chrisoutofspace .

  
For installation instructions, see below.  
  
## 1. Machine learning  

    conda activate mfrpred
    jupyter lab
    
Run the mfrpred_mreiss_bz.ipynb and mfrpred_mreiss_btot notebooks in jupyter lab.    


---


## 2. Installation 

Install python 3.7.6 with miniconda:

on Linux:

	  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
	  bash Miniconda3-latest-Linux-x86.sh

on MacOS:

	  curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
	  bash Miniconda3-latest-MacOSX-x86_64.sh

go to a directory of your choice

	  git clone https://github.com/helioforecast/Papers
      cd Reiss2021_MLrope

Create a conda environment for the mfrpred_... notebooks:

	  conda env create -f environment.yml

	  conda activate mfrpred

	  pip install -r requirements.txt
	  

Create a conda environment for the detection_... notebooks:

	  conda env create -f environment_detect.yml

	  conda activate detect

	  pip install -r requirements_detect.txt
	  




Before running the scripts, you need to download three data files (in total 1.8 GB) from this figshare repository, 

    https://doi.org/10.6084/m9.figshare.12058065.v8

and place them in the data/ folder.

    data/stereoa_2007_2021_sceq_ndarray.p
    data/stereob_2007_2014_sceq_ndarray.p
    data/wind_2007_2021_heeq_ndarray.p
        


A catalog for interplanetary coronal mass ejections (HELCATS ICMECAT v2.0) is included in this repo, for updates see:

    https://helioforecast.space/icmecat

