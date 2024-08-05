# Benthic Foraminifera Pore Patterns in the Southeast Pacific
A repository of "A species-specific approach to benthic foraminifera pore patterns as a paleoxygenation proxy in the Southeast Pacific"

## Repository's Overview

This repository contains data and scripts related to the article "A species-specific approach to benthic foraminifera pore patterns as a paleoxygenation proxy in the Southeast Pacific" by Sebastián Garrido et al. (in review). The research focuses on the use of pore patterns in benthic foraminifera as proxies for past bottom water dissolved oxygen (BWDO) levels in the Southeast Pacific (SEP), providing insights into changes in ocean oxygenation conditions over the geological past.

First, for you to understand the goal and context of this repository, here is an overview of our research.

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

1. Lyell Centre, Heriot-Watt University, Edinburgh, UK
2. ANID - Millennium Science Initiative Program Nucleo Milenio UPWELL, La Serena, Chile
3. Japan Agency for Marine-Earth Science and Technology (JAMSTEC), Yokosuka, Japan
4. MARUM - Center for Marine Environmental Sciences, University of Bremen, Germany
5. PAGES - University of Bern, Switzerland
6. Universidad Peruana Cayetano Heredia (UPCH), Lima, Perú
7. J’EAI-CHARISMA, Colombia
8. CIEAM - Centro de Investigación y Estudios Avanzados del Maule, Universidad Católica del Maule, Chile
9. UMR EPOC, Université de Bordeaux, France
10. Departamento de Geografía, Universidad de Chile, Santiago, Chile
11. Université d'Angers, Nantes Université, Le Mans Université, CNRS, France

## Research's Data and Methods

### Regional Setting and Samples
- The Southeast Pacific (SEP) features significant vertical, latitudinal, and longitudinal gradients in hydrological parameters (Silva et al., 2009, Paulmier and Ruiz-Pino, 2009).
- Our samples were collected from the Southeast Pacific between 12°S and 44°S along the continental margin of Chile and Peru, at depths ranging from 24 to 3,252 m.
- Sampling methods included Multicorer, box-corer, Petersen grab, and gravity core through the cruises (SONNE 156, SONNE 211, SONNE 161, Meteor 92, USNS Eltanin, BIAC072014)

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

- **ImageJ-Scripts**: Contains Java macros for measuring pore patterns using ImageJ software.
  
  - **Requirements**: To run the scripts and use the macros provided in this repository, you will need the following software and packages installed:
    
      - **ImageJ**: Download and install ImageJ from [imagej.net](https://imagej.net/software/imagej/).
        
      - **Java**: Ensure you have Java installed, as ImageJ requires Java to run. You can download it from [java.com](https://www.java.com/).
    
  - `PoresSEP_75x50_x400.ijm`: Macro for measuring penultimate and antepenultimate chambers (PAC).
    
    - Example images to run the PAC pore measurements:
      
      - Umbilical PAC: `28-11-22__0114.tif` (Penultimate chamber), `28-11-22__0115.tif` (Antepenultimate chamber)
        
      - Spiral PAC: `30-11-22__0060.tif` (Penultimate chamber), `30-11-22__0061.tif` (Antepenultimate chamber)
            
  - `PoresSEP_x60.ijm`, `PoresSEP_x80.ijm`, `PoresSEP_x100.ijm`, `PoresSEP_x120.ijm`, `PoresSEP_x150.ijm`, `PoresSEP_x180.ijm`, `PoresSEP_x200.ijm`, `PoresSEP_x250.ijm`, `PoresSEP_x300.ijm`: Macros for measuring the entire umbilical and spiral sides at various magnifications (For more detail about this, see Appendix A of this article).
     
    - Example images to run the entire umbilical and spiral side pore measurements:
      
      - Umbilical side: `28-11-22__0038.tif`, `28-11-22__0081.tif`
        
      - Spiral side: `28-09-22__0075.tif`, `28-09-22__0202.tif`
          
- **DataAnalysis**: Contains scripts and datasets used for statistical analysis of pore measurements and proxy calibration.

  - **Requirements**: To run the scripts and use the macros provided in this repository, you will need the following software and packages installed:
    
      - **Python**: Ensure you have Python 3.7 or later installed. You can download it from [anaconda.com](https://www.anaconda.com/download).
        
      - **Python Packages**: Install the necessary packages using pip. You can do this by running the following command in your terminal:
        
          ```sh
          pip install numpy pandas matplotlib statsmodels seaborn scikit-learn
          ```  

  - `PorePatternsSEP-Script.py`: Python script using numpy, pandas, matplotlib, statmodels, seaborn, and sklearn packages to perform Weighted Least Squares (WLS) regression and analyze pore patterns. This script includes functions for data cleaning, statistical analysis, and visualization.
    
  - `Dataset Pore Measurements Garrido et al..csv`: This is a dataset with pore measurements used as input for the analysis. This includes measurements of porosity, pore density, and pore size for various benthic foraminiferal species.
    

## Usage

### ImageJ Macros to measure pore patterns 

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
