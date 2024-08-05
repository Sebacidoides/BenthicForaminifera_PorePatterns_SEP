# Benthic Foraminifera Pore Patterns in the Southeast Pacific

A repository of "A species-specific approach to benthic foraminifera pore patterns as a paleoxygenation proxy in the Southeast Pacific" (Garrido et al., in review)

## Repository's Overview

This repository contains data and scripts related to the article "A species-specific approach to benthic foraminifera pore patterns as a paleoxygenation proxy in the Southeast Pacific" by Garrido et al. (in review). The research focuses on the use of pore patterns in benthic foraminifera as proxies for past bottom water dissolved oxygen (BWDO) levels in the Southeast Pacific (SEP), providing insights into changes in ocean oxygenation conditions over the geological past.

First, here is an overview of our research to help you understand the goal and context of this repository.

## Research's Abstract

Calcareous benthic foraminifera can develop pores in their test walls to facilitate gas exchanges (e.g., O<sub>2</sub>, CO<sub>2</sub>) with the surrounding seawater. The patterns of these pores, such as porosity, pore density, and pore size, vary based on environmental factors, including BWDO. Some species react to lower BWDO levels by increasing test porosity, making them useful proxies for reconstructing past BWDO concentrations.
This study validates this proxy in the Southeast Pacific (SEP) by comparing the pore patterns of six benthic foraminifera species with BWDO. Specimens dated from the Holocene to the modern era were collected from surface sediment samples along the SEP (12°–44°S) from 24 to 3,252 m water depth. Our findings reveal species-specific pore pattern responses to BWDO, with notable differences between *Cibicidoides* and *Planulina* species. These results support the use of benthic foraminifera pore patterns as reliable indicators for quantitatively reconstructing past BWDO levels, with an error range of ±5–20 µmol/kg.

## Authors

- Sebastián Garrido <sup>1,2</sup>
- Babette Hoogakker <sup>1</sup>
- Julien Richirt <sup>3</sup>
- Dharma Reyes-Macaya <sup>1,2,4</sup>
- Iván Hernández-Almeida <sup>5</sup>
- Jorge Cardich <sup>6,7</sup>
- Alexis Castillo Bruna <sup>2,7,8</sup>
- Marie P.A. Fouet <sup>9</sup>
- Eugenia M. Gayo <sup>2,10</sup>
- Dierk Hebbeln <sup>4</sup>
- Frans Jorissen <sup>11</sup>

Affiliations:

<sup>1</sup> Lyell Centre, Heriot-Watt University, Edinburgh, UK

<sup>2</sup> ANID - Millennium Science Initiative Program Nucleo Milenio UPWELL, La Serena, Chile

<sup>3</sup> Japan Agency for Marine-Earth Science and Technology (JAMSTEC), Yokosuka, Japan

<sup>4</sup> MARUM - Center for Marine Environmental Sciences, University of Bremen, Germany

<sup>5</sup> PAGES - University of Bern, Switzerland

<sup>6</sup> Universidad Peruana Cayetano Heredia (UPCH), Lima, Perú

<sup>7</sup> J’EAI-CHARISMA, Colombia

<sup>8</sup> CIEAM - Centro de Investigación y Estudios Avanzados del Maule, Universidad Católica del Maule, Chile

<sup>9</sup> UMR EPOC, Université de Bordeaux, France

<sup>10</sup> Departamento de Geografía, Universidad de Chile, Santiago, Chile

<sup>11</sup> Université d'Angers, Nantes Université, Le Mans Université, CNRS, France

## Research's Data and Methods

### Regional Setting and Samples
- The Southeast Pacific (SEP) features significant vertical, latitudinal, and longitudinal gradients in hydrological parameters (Silva et al., 2009, Paulmier and Ruiz-Pino, 2009).
- Our samples were collected from the Southeast Pacific between 12°S and 44°S along the continental margin of Chile and Peru, at depths ranging from 24 to 3,252 m (Figure 1).
- Sampling methods included Multicorer, box-corer, Petersen grab, and gravity core through the cruises (SONNE 156, SONNE 211, SONNE 161, Meteor 92, USNS Eltanin, BIAC072014)

<figure>
  <img src="Figure 1.png" alt="Map" width="800">
  <figcaption>Figure 1: Locations of the surface sediment samples used in this study. (a) Map showing the locations of the samples along the Chilean and Peruvian coasts. (b) Longitudinal  profile of the samples, illustrating their bottom water oxygen content (BWDO), samples cover BWDO from 3 to 245 µmol/kg. Main water masses of the SEP: STW = Subtropical Water, SAAW = Subantarctic Surface Water, ESSW = Equatorial Subsurface Water, AAIW = Antarctic Intermediate Water, PDW = Pacific Deep Water; the dotted gray line represents boundaries between water masses. Water masses distribution and characteristics from Reyes-Macaya et al. (2022).</figcaption>
</figure>

### Specimen Selection and Imaging
- Specimens were wet-sieved to > 63 µm, oven-dried, and Rose Bengal stained.
- Selected specimens were cleaned, mounted on stubs, and imaged using a TM4000Plus HITACHI Scanning Electron Microscope (SEM).

### Pore Patterns Measurements
- Pore patterns were measured using ImageJ software with custom Java macros.
- Measurements included porosity, pore density, and pore size.
- Data and codes to perform this part are in folder **"ImageJ-Scripts"**.

### Statistical Analysis
- Principal component analysis (PCA) and regression analysis were performed to explore the relationship between pore patterns and environmental parameters.
- Weighted Least Squares (WLS) regression was used to account for heteroscedasticity.
- Data and codes to perform this part are in folder **"DataAnalysis"**.

## Repository Structure and Requirements

The repository is organized into the following folders:

- **ImageJ-Scripts**: Contains Java macros for measuring pore patterns using ImageJ software. Moreover, you can find here images as example for you to run the macros. 
  
  - **Requirements**: To run the scripts and use the macros provided in this repository, you will need the following software and packages installed:
    
      - **ImageJ**: Download and install ImageJ from [imagej.net](https://imagej.net/software/imagej/).
        
      - **Java**: Ensure you have Java installed, as ImageJ requires Java to run. You can download it from [java.com](https://www.java.com/).
    
  - `PoresSEP_75x50_x400.ijm`: Macro for measuring penultimate and antepenultimate chambers (PAC).
    
    - Images to run the PAC pore measurements:
      
      - Umbilical PAC:
          - *Cibicidoides wuellerstorfi* forma *plana* from sample GeoB7150-1:
              - `28-11-22__0114.tif` (Penultimate chamber)
              - `28-11-22__0115.tif` (Antepenultimate chamber)
        
      - Spiral PAC:
          - *Cibicidoides wuellerstorfi* forma *convexa* from sample GeoB7209-2:
              - `30-11-22__0060.tif` (Penultimate chamber)
              - `30-11-22__0061.tif` (Antepenultimate chamber)
            
  - `PoresSEP_x60.ijm`, `PoresSEP_x80.ijm`, `PoresSEP_x100.ijm`, `PoresSEP_x120.ijm`, `PoresSEP_x150.ijm`, `PoresSEP_x180.ijm`, `PoresSEP_x200.ijm`, `PoresSEP_x250.ijm`, `PoresSEP_x300.ijm`: Macros for measuring the entire umbilical and spiral sides at various magnifications (For more detail about this, see Appendix A of this article).
     
    - Images to run the entire umbilical and spiral side pore measurements:
      
      - Umbilical side:
          - `28-11-22__0038.tif` (*Cibicidoides wuellerstorfi* forma *plana* from sample GeoB7157-1)
          - `28-11-22__0081.tif`(*Cibicidoides ungerianus* from sample GeoB7156-1)
        
      - Spiral side:
          - `28-09-22__0075.tif` (*Cibicidoides wuellerstorfi* forma *convexa* from sample GeoB7137-1)
          - `28-09-22__0202.tif` (*Cibicidoides wuellerstorfi* forma *plana* from sample GeoB7115-1)
          
- **DataAnalysis**: Contains scripts and datasets used for statistical analysis of pore measurements and proxy calibration.

  - **Requirements**: To run the scripts and use the macros provided in this repository, you will need the following software and packages installed:
    
      - **Python**: Ensure you have installed Python 3.7 or later. You can download it from [anaconda.com](https://www.anaconda.com/download).
        
      - **Python Packages**: Install the necessary packages using pip. You can do this by running the following command in your terminal:
        
          ```sh
          pip install numpy pandas matplotlib statsmodels seaborn scikit-learn
          ```  

  - `PorePatternsSEP-Script.py`: Python script using numpy, pandas, matplotlib, statmodels, seaborn, and sklearn packages to perform Weighted Least Squares (WLS) regression and analyze pore patterns. This script includes functions for data cleaning, statistical analysis, and visualization. Details of how the code works are included at the beginning of the code within a Jupyter Notebook; click on the notebook, and you will find the instructions. 
    
  - `Dataset Pore Measurements Garrido et al..csv`: This is a dataset with pore measurements used as input for the analysis. This dataset includes:
 
      - **Location Data**: Site, Latitude, Longitude, Water depth
      - **Foraminifera Collection**: Sample, Image, Cruise, Year
      - **Porosity Measurements**: Average porosity, Std deviation, Threshold, Average number of pores, Std deviation of pore number, Average pore diameter, Std deviation of pore diameter, Average test area, Std deviation of test area
      - **Specimen Measurements**: Size, Std deviation of size, Average pore density, Std deviation of pore density
      - **Specimen Details**: Side, Chamber, SpecimenID, Morphotype (for C. wuellerstorfi), Species, Preservation status, Missing chambers (ventral/dorsal), Chambers in last whorl, Image pixel size, Image magnification, Staining status
      - **Sediment Details**: Fraction, <sup>14</sup>C age, Error, Organic carbon, Carbonate content, Opal content, C/N ratio, Granulometry (mean, median, mode, StdDev, skewness, kurtosis, %Clay, %Silt, %Sand)
      - **Bottom Water Environmental Parameters**: Oxygen, Temperature, Salinity, pH, Carbonate content, δ¹³C of DIC, Nitrate, Phosphate, Silica, Chlorophyll content, Primary productivity, El Niño/La Niña, PDO indices
      - **Additional Information**: Age assigned, Comments (penultimate/antepenultimate details)
    
## Usage

### ImageJ Macros to Measure Pore Patterns 

1. **Open ImageJ**.
2. **Load the image** of the benthic foraminifera specimen you want to measure.
3. **What kind of measurement are you performing now?** This is important because you need to decide whether you will use the macros for penultimate and antepenultimate chambers (PAC) or for the entire spiral or umbilical side.
4. **Use the provided Java macros** to measure pore patterns on the images. You can load the macros by navigating to `Plugins > Macros > Run...` and selecting the appropriate `.ijm` file from the `ImageJ-Scripts` folder.
      - If you are performing PAC measurements, add the appropriate macro. Use `PoresSEP_75x50_x400.ijm` to measure the penultimate and antepenultimate chambers (PAC).
      - If you are measuring umbilical or spiral side measurements (all chambers included), check the magnification in the bottom left corner (60x, 80x, 100x, 120x, 150x, 180x, 200x, 250x, 300x). Use the other macros (`PoresSEP_x60.ijm`, `PoresSEP_x80.ijm`, etc.) to measure the entire umbilical and spiral sides at the specified magnifications.

### Data Analysis

1. **Run the Analysis Script**:
      - Navigate to the `DataAnalysis` folder.
      - Run the `PorePatternsSEP-Script.py` script to perform the statistical analysis and generate visualizations of pore patterns.
2. **Input Data**:
      - The script uses the `Dataset Pore Measurements Garrido et al..csv` file as input. Ensure this file is in the same directory as the script.
3. **Output**:
      - We recommend an environment similar to the one in `PorePatternsSEP-ScriptFiles.zip`. This folder also contains the Python script (`PorePatternsSEP-Script.py`). Moreover, you can find the same dataset (`Dataset Pore Measurements Garrido et al..csv`) in the folder `Datasets`. In that folder (`Datasets`), you can find two folders `Created datasets` and `Created Figures`, where the code will create secondary datasets and figures from the main analysis. Ensure the directories match in the Python code. 


## Acknowledgements

- We thank the crews and scientific teams of the research expeditions PG4, M92, SONNE 156, SONNE 161, and SONNE 211 expeditions, and the GeoB Core Repository at MARUM, University of Bremen (special thanks to Jürgen Titschack).
- We thank the teams at the Université d'Angers (Frans Jorissen, Marie Fouet, Christine Barras, Sophie Sanchez, Eleonora Fossile), Heriot-Watt University (Lilja Alam, Sarah Collet), and the British Geological Survey (Melanie Leng, Kotryna Savickaite). 
- We also thank Laura Farias for the regional CTDO data (BIOSPE, FIP_2006, Galathea, Jamstec, and Samfloc).
- Sebastián Garrido acknowledges funding from the ANID Scholarship Program DOCTORADO BECAS CHILE 2019 / 72200463. 
- This study was supported by the FARGO project (MR/S034293/1 to BH) and ANID Millennium Science Initiative Program NCN19_153.

## References

Paulmier, A., Ruiz-Pino, D., 2009. Oxygen minimum zones (OMZs) in the modern ocean. Prog Oceanogr 80. https://doi.org/10.1016/j.pocean.2008.08.001

Silva, N., Rojas, N., Fedele, A., 2009. Water masses in the Humboldt Current System: Properties, distribution, and the nitrate deficit as a chemical water mass tracer for Equatorial Subsurface Water off Chile. Deep Sea Research Part II: Topical Studies in Oceanography 56, 1004–1020. https://doi.org/10.1016/j.dsr2.2008.12.013

## Contact

For any questions or further information, please contact Sebastián Garrido at [sag15@hw.ac.uk](mailto:sag15@hw.ac.uk) or [sebagarridomedina@gmail.com](mailto:sebagarridomedina@gmail.com).
