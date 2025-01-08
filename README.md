# Crop Yield Analysis: Soybean Yield vs. Rainfall and Temperature

This repository contains the analysis of soybean yield data in relation to rainfall and temperature variations in Indore, India. The goal is to identify trends, correlations, and to build regression models to understand how climatic factors impact soybean yield.

## Contents

- `data_stream-oper_stepType-accum.nc`: NetCDF file containing accumulated temperature data.
- `data_stream-oper_stepType-instant.nc`: NetCDF file containing instantaneous temperature data.
- `data_stream-oper_stepType-max.nc`: NetCDF file containing maximum temperature data.
- `output.png`: Generated output plot showcasing rainfall, temperature, and yield trends over the years.
- `rainfall_data/`: Directory containing rainfall data files for various years.
  - `RF25_indYYYY_rfp25.nc`: NetCDF files containing rainfall data for the years 2014–2023.
- `yield-analysis.ipynb`: Jupyter Notebook for performing data analysis and generating plots.
- `README.md`: This file.

## Installation

To run the analysis, you will need the following Python packages:

```bash
pip install numpy pandas netCDF4 xarray matplotlib seaborn scikit-learn
```

Additionally, ensure you have the required `.nc` files (rainfall and temperature data) and place them in the respective directories.

## Dataset Description

### Soybean Yield Data:
A dataset representing soybean production and yield in Indore, India for the years 2013–2023. The dataset includes the following columns:
- **Year**: Year of data (2013–2023).
- **Area (Hectare)**: Area of soybean cultivation (in hectares).
- **Production (Tonnes)**: Total production of soybeans (in tonnes).
- **Yield (Tonne/Hectare)**: Yield of soybeans (in tonnes per hectare).

### Rainfall Data:
Rainfall data for Indore from 2014 to 2023, provided in the form of `.nc` files. Each file contains daily rainfall data recorded in millimeters.

### Temperature Data:
Maximum temperature data from `data_stream-oper_stepType-max.nc`, which provides temperature variations in Indore.

## Analysis Workflow

1. **Data Preprocessing**:
   - The rainfall data is processed to compute total yearly rainfall for Indore from 2014 to 2023.
   - The temperature data is extracted for the same period to understand temperature trends.
   - Soybean yield data for the corresponding years is merged with the rainfall and temperature data.

2. **Plotting**:
   The analysis visualizes the following time series:
   - Yearly rainfall (mm) in Indore.
   - Yearly maximum temperature (°C) in Indore.
   - Yearly soybean yield (Tonne/Hectare) in Indore.
   
3. **Correlation Analysis**:
   - Pearson correlation is computed between rainfall and soybean yield, as well as temperature and soybean yield.
   - Results are printed for interpretation.

4. **Linear Regression Models**:
   - Linear regression models are built to predict soybean yield based on rainfall and temperature.

5. **Heatmap**:
   - A heatmap is generated to visualize correlations between rainfall, temperature, and yield.

## Results

The notebook will output:
- A plot showing trends for rainfall, temperature, and yield.
- Correlation statistics between rainfall, temperature, and soybean yield.
- Linear regression equations for predicting yield based on rainfall and temperature.
- A correlation heatmap to provide an overview of the relationships between the variables.

## How to Run

1. Clone the repository or download the necessary files.
2. Ensure that the required `.nc` files are in the `rainfall_data/` directory.
3. Open `yield-analysis.ipynb` in Jupyter Notebook or JupyterLab.
4. Run the cells to see the analysis and plots.

## Acknowledgments

- The rainfall data and temperature data are sourced from climate databases.
- The soybean yield data is collected from agricultural records in Indore, India.
## Contact

For any questions or suggestions, feel free to open an issue in the repository or contact me via GitHub.
