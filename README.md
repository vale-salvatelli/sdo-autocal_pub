# Frontier Development Lab - SDO Team

The goal of the project is to use data from the Solar Dynamic Observatory (SDO) to expand the capabilities
of this extreme UV (EUV) telescope and of future solar missions. EUV telescopes operating in space are known to 
degrade over the course of months to years. The rate of degradation is, a priori, unknown. Over the same time 
scales, the Sun's activity also changes. This project uses spatial patterns of features on the Sun to arrive at 
a self-calibration of EUV instruments. This approach avoids the need to calibrate against other sources.

To reference the software in this repository please use 
[DOI: 10.5281/zenodo.4434743](https://zenodo.org/record/4434744#.X_4MIen7R-V).

The main dataset used for the project can be retrieved from [here](https://github.com/fluxtransport/SDOML) 
and it is described in [Galvez et al. (2019, ApJS)](https://iopscience.iop.org/article/10.3847/1538-4365/ab1005).
The data uncorrected for degradation is instead available [here](https://zenodo.org/record/4430801#.X_xiP-lKhmE).


# How to use the repo
1) Reusable code lives inside src in the form of a package called sdo that can be installed. 
    
    In order to install the package:
    
        1) cd expanding-sdo-capabilities
        2) pip install --user -e .
        
2) The pipeline to train and test the autocalibration model can be started by running:
   
        1) export CONFIG_FILE=./config/autocal_paper_config.yaml 
        2) ./src/sdo/main.py -c $CONFIG_FILE 

    it requires access to a SDOML dataset in numpy memory mapped objects format.
    
 3) Some scripts for data pre-processing are contained in scripts/data_preprocess.
 
 4) Notebooks with some analysis of the results live in the notebooks folder.s

# Publications
This repo contains the code developed to produce the paper:
* "Multi-Channel Auto-Calibration for the Atmospheric Imaging Assembly using Machine Learning"
   Accepted for A&A publication.
   https://arxiv.org/abs/2012.14023.

Other publications made under the FDL - SDO project:
* "Auto-Calibration of Remote Sensing Solar Telescopes with Deep Learning"
    NeurIPS 2019 - ML4PS Workshop
    https://arxiv.org/abs/1911.04008
    
* "Using U-Nets to Create High-Fidelity Virtual Observations of the Solar Corona"
    ML4PS NeurIPS 2019 - ML4PS Workshop
    https://arxiv.org/abs/1911.04006

# More on this project 
This project started as part of the [2019 Frontier Development Lab (FDL) SDO team](https://frontierdevelopmentlab.org/2019-sdo). 
A description of this program is available [here](https://frontierdevelopmentlab.org/about-1).

