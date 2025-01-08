# 🌾 Crop Yield Analysis: Soybean Yield vs. Rainfall and Temperature 🌦️🌡️

Welcome to this repository dedicated to the analysis of **soybean yield** in relation to **rainfall** and **temperature** variations in **Indore, India**. This study aims to uncover trends, correlations, and to build regression models to better understand how climatic factors influence soybean production. 🌱

## 📂 Contents

- **`data_stream-oper_stepType-accum.nc`**: NetCDF file containing accumulated temperature data.
- **`data_stream-oper_stepType-instant.nc`**: NetCDF file containing instantaneous temperature data.
- **`data_stream-oper_stepType-max.nc`**: NetCDF file containing maximum temperature data.
- **`output.png`**: Visualization plot showcasing rainfall, temperature, and yield trends over the years.
- **`rainfall_data/`**: Folder with rainfall data files for the years 2014–2023.
  - **`RF25_indYYYY_rfp25.nc`**: NetCDF files containing rainfall data for the years 2014–2023.
- **`yield-analysis.ipynb`**: Jupyter Notebook for performing data analysis and generating plots.
- **`README.md`**: This file with detailed instructions and analysis overview.

## 📋 Installation

To get started with the analysis, you’ll need the following Python packages:

```bash
pip install numpy pandas netCDF4 xarray matplotlib seaborn scikit-learn
```

Ensure that you have the `.nc` files (rainfall and temperature data) and place them in the correct directories.

## 🌾 Dataset Description

### Soybean Yield Data
This dataset represents **soybean production** and **yield** in **Indore, India** from 2013–2023, with the following columns:
- **Year**: The year of data (2013–2023).
- **Area (Hectare)**: Area under soybean cultivation (in hectares).
- **Production (Tonnes)**: Total soybean production (in tonnes).
- **Yield (Tonne/Hectare)**: Soybean yield per hectare (in tonnes).

### Rainfall Data
Rainfall data for Indore (2014–2023), provided in **NetCDF** format, includes daily rainfall measurements in millimeters.

### Temperature Data
Maximum temperature data from **`data_stream-oper_stepType-max.nc`**, which provides daily temperature variations for Indore.

## 🔍 Analysis Workflow

1. **Data Preprocessing**:
   - Process rainfall data to calculate the **total yearly rainfall** for Indore (2014–2023).
   - Extract and analyze **temperature data** for the same period.
   - Merge soybean yield data with rainfall and temperature information for comprehensive analysis.

2. **Plotting**:
   Visualize the following time series:
   - Yearly **rainfall** (mm) in Indore 🌧️.
   - Yearly **maximum temperature** (°C) in Indore 🌡️.
   - Yearly **soybean yield** (Tonne/Hectare) in Indore 🌾.

3. **Correlation Analysis**:
   - **Pearson correlation** is computed between rainfall and soybean yield, as well as temperature and soybean yield. 
   - The correlation results will be printed for interpretation.

4. **Linear Regression Models**:
   - Develop **linear regression models** to predict soybean yield based on rainfall and temperature. 📈

5. **Heatmap**:
   - A **correlation heatmap** will be generated to visualize the relationships between rainfall, temperature, and soybean yield. 🔥

## 📈 Results

Running the notebook will generate:
- A **plot** that illustrates trends for rainfall, temperature, and yield over time.
- **Correlation statistics** between rainfall, temperature, and soybean yield.
- **Linear regression equations** for predicting yield based on climatic factors.
- A **correlation heatmap** summarizing the relationships between the variables.

## 🛠️ How to Run

1. Clone or download the necessary files.
2. Ensure that the required `.nc` files are present in the `rainfall_data/` folder.
3. Open **`yield-analysis.ipynb`** in **Jupyter Notebook** or **JupyterLab**.
4. Run the cells to view the analysis and generated plots.

## 🙌 Acknowledgments

- The **rainfall** and **temperature** data are sourced from trusted climate databases.
- The **soybean yield** data is sourced from agricultural records in Indore, India.

## 📬 Contact

For any questions or suggestions, feel free to open an issue on GitHub or reach out via my profile.

Happy analyzing! 🚜
