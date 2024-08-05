# Benthic Foraminifera Pore Patterns in the Southeast Pacific

## Overview

This repository contains data and scripts related to the study "A species-specific approach to benthic foraminifera pore patterns as a paleoxygenation proxy in the Southeast Pacific" by Sebastián Garrido et al. The research focuses on the use of pore patterns in benthic foraminifera as proxies for past bottom water dissolved oxygen (BWDO) levels, providing insights into historical ocean oxygenation conditions.

## Repository Structure

The repository is organized into the following folders:

- **DataAnalysis**: Contains scripts and datasets used for statistical analysis and proxy calibration.
  - `PorePatternsSEP-Script.py`: Python script using numpy, pandas, matplotlib, statmodels, seaborn, and sklearn packages to perform Weighted Least Squares (WLS) regression and analyze pore patterns. This script includes functions for data cleaning, statistical analysis, and visualization.
  - `Dataset Pore Measurements Garrido et al..csv`: Dataset with pore measurements used as input for the analysis. This includes measurements of porosity, pore density, and pore size for various benthic foraminiferal species.

- **ImageJ-Scripts**: Contains Java macros for measuring pore patterns using ImageJ software.
  - `PoresSEP_75x50_x400.ijm`: Macro for measuring penultimate and antepenultimate chambers (PAC).
  - `PoresSEP_x60.ijm`, `PoresSEP_x80.ijm`, `PoresSEP_x100.ijm`, `PoresSEP_x120.ijm`, `PoresSEP_x150.ijm`, `PoresSEP_x180.ijm`, `PoresSEP_x200.ijm`, `PoresSEP_x250.ijm`, `PoresSEP_x300.ijm`: Macros for measuring the entire umbilical and spiral sides at various magnifications.

## Requirements

To run the scripts and use the macros provided in this repository, you will need the following software and packages installed:

### Python Environment

1. **Python**: Ensure you have Python 3.7 or later installed. You can download it from [python.org](https://www.python.org/).

2. **Python Packages**: Install the necessary packages using pip. You can do this by running the following command in your terminal:

    ```sh
    pip install numpy pandas matplotlib statsmodels seaborn scikit-learn
    ```

### ImageJ Environment

1. **ImageJ**: Download and install ImageJ from [imagej.net](https://imagej.net/software/imagej/).

2. **Java**: Ensure you have Java installed, as ImageJ requires Java to run. You can download it from [java.com](https://www.java.com/).

## Usage

### Data Analysis

1. **Run the Analysis Script**:
    - Navigate to the `DataAnalysis` folder.
    - Run the `PorePatternsSEP-Script.py` script to perform the statistical analysis and generate visualizations of pore patterns.

    ```sh
    python PorePatternsSEP-Script.py
    ```

2. **Input Data**:
    - The script uses the `Dataset Pore Measurements Garrido et al..csv` file as input. Ensure this file is in the same directory as the script.

3. **Output**:
    - The script will generate statistical summaries and visualizations which will be saved in the `DataAnalysis` folder.

### ImageJ Macros

1. **Measure Pore Patterns**:
    - Open ImageJ and load the images of benthic foraminifera specimens.
    - Use the provided Java macros to measure pore patterns on the images. You can load the macros by navigating to `Plugins > Macros > Run...` and selecting the appropriate `.ijm` file from the `ImageJ-Scripts` folder.

2. **Select the Appropriate Macro**:
    - Use `PoresSEP_75x50_x400.ijm` for measuring the penultimate and antepenultimate chambers (PAC).
    - Use the other macros (`PoresSEP_x60.ijm`, `PoresSEP_x80.ijm`, etc.) for measuring the entire umbilical and spiral sides at the specified magnifications.

## Abstract

Calcareous benthic foraminifera can develop pores in their test walls to facilitate gas exchanges (e.g., O2, CO2) with the surrounding seawater. The patterns of these pores, such as porosity, pore density, and pore size, vary based on environmental factors, including BWDO. Some species react to lower BWDO levels by increasing test porosity, making them useful proxies for reconstructing past BWDO concentrations.

This study validates this proxy in the Southeast Pacific (SEP) by comparing pore patterns of six benthic foraminifera species with BWDO. Specimens dated from the Holocene to the modern era were collected from surface sediment samples along the SEP (12°–44°S) from 24 to 3,252 m water depth. Our findings reveal species-specific pore pattern responses to BWDO, with notable differences between Cibicidoides and Planulina species. These results support the use of benthic foraminifera pore patterns as reliable indicators for quantitatively reconstructing past BWDO levels, with an error range of ±5–20 µmol/kg.

## Authors

- Sebastián Garrido1,2
- Babette Hoogakker1
- Julien Richirt3
- Dharma Reyes-Macaya1,2,4
- Iván Hernández-Almeida5
- Jorge Cardich6,7
- Alexis Castillo Bruna2,7,8
- Marie P.A. Fouet9
- Eugenia M. Gayo2,10
- Dierk Hebbeln4
- Frans Jorissen11

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

## Data and Methods

### Regional Setting and Samples
- The SEP features significant vertical, latitudinal, and longitudinal gradients in hydrological parameters.
- Samples were collected from 12°S to 44°S along the continental margin of Chile and Peru, at depths ranging from 24 to 3,252 m.
- Sampling methods included Multicorer, box-corer, Petersen grab, and gravity core.

### Specimen Selection and Imaging
- Specimens were wet-sieved to > 63 µm, oven-dried, and Rose Bengal stained.
- Selected specimens were cleaned, mounted on stubs, and imaged using a TM4000Plus HITACHI Scanning Electron Microscope (SEM).

### Pore Patterns Measurements
- Pore patterns were measured using ImageJ software with custom Java macros.
- Measurements included porosity, pore density, and pore size.

### Statistical Analysis
- Principal component analysis (PCA) and regression analysis were performed to explore the relationship between pore patterns and environmental parameters.
- Weighted Least Squares (WLS) regression was used to account for heteroscedasticity.

## Acknowledgements

We thank the crew and scientific teams involved in various research expeditions, the GeoB Core Repository at MARUM, and the team at Université d'Angers for their invaluable assistance. Funding was provided by the National Agency for Research and Development (ANID), the German Federal Ministry of Education and Research, the FARGO project, and the ANID Millennium Science Initiative Program.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or further information, please contact Sebastián Garrido at [sag15@hw.ac.uk](mailto:sag15@hw.ac.uk).
