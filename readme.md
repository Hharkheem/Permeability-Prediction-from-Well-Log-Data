# Permeability Prediction from Well Log Data

## Overview
This repository contains a Jupyter Notebook (`main.ipynb`) that demonstrates a workflow for predicting permeability from well log data. The project involves data loading, preprocessing (handling missing values, setting depth as index), descriptive statistical analysis, and correlation analysis of various well log parameters.

## Key Features
- **Data Loading**: Reads well log data from a CSV file (`15_9-F-1_A_INPUT.LAS.csv`).
- **Data Preprocessing**:
  - Sets 'Depth' as the DataFrame index.
  - Identifies and handles missing data by dropping rows with NaN values.
- **Descriptive Statistics**: Provides a comprehensive statistical summary of the well log parameters (count, mean, standard deviation, min, max, and quartiles).
- **Correlation Analysis**: Calculates and visualizes the correlation matrix between different well log curves to understand their relationships.
- **Permeability Prediction (Planned/Future Work)**: The notebook structure suggests an intention to predict permeability (`KLOGH`) based on other well log attributes. While the prediction model itself isn't fully implemented in the provided snippet, the groundwork for data preparation is laid out.
- **Log Visualization**: Includes code to plot various well log curves (`CALI`, `GR`, `DTS`, `DT`, `RHOB`, `NPHI`, `PEF`, `SW`, `VSH`, `KLOGH`, `RT`, `ROP`) against depth, allowing for visual inspection of log characteristics and their relationship with permeability.
- **Predicted Permeability Saving**: Saves the predicted permeability data to a CSV file (`Predicted_Permeability(NEW WELL).csv`).

## Installation
To run this notebook, you'll need to have Python and Jupyter installed. It's recommended to use a virtual environment.

1. Clone the repository:
   ```bash
   git clone https://github.com/Hharkheem/Permeability-Prediction-from-Well-Log-Data.git
   cd Permeability-Prediction-from-Well-Log-Data
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   # On Windows
   .\venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

## Usage
1. **Place your data**: Ensure the `15_9-F-1_A_INPUT.LAS.csv` file is in the same directory as the `main.ipynb` notebook, or update the file path in the notebook accordingly.
2. **Open the Jupyter Notebook**:
   ```bash
   jupyter notebook main.ipynb
   ```
3. **Run the cells**: Execute the cells sequentially to perform data loading, preprocessing, analysis, and visualization.

## Data
The primary dataset used in this project is `15_9-F-1_A_INPUT.LAS.csv`. This CSV file contains various well log measurements, including:
- **Depth**: Measurement depth.
- **CALI**: Caliper log.
- **DRHO**: Density correction.
- **DT**: P-wave sonic transit time.
- **DTS**: S-wave sonic transit time.
- **GR**: Gamma Ray log.
- **NPHI**: Neutron porosity.
- **PEF**: Photoelectric Factor.
- **RACEHM, RACELM, RPCELM, RT**: Resistivity logs (various depths of investigation).
- **RHOB**: Bulk density.
- **ROP**: Rate of Penetration.
- **PHIF**: Formation porosity.
- **KLOGH**: Horizontal permeability (target variable for prediction).
- **SAND_FLAG**: Indicator for sand presence.
- **SW**: Water saturation.
- **VSH**: Shale volume.

## Results
The notebook generates:
- Descriptive statistics of the well log data.
- A correlation matrix heatmap to visualize relationships between logs.
- Well log plots showing various curves against depth.
- A CSV file named `Predicted_Permeability(NEW WELL).csv` containing the predicted permeability values (after the prediction model is fully implemented).
- A JPEG image of the well logs plot saved as `well_logs.jpg`.

## Contributing
Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please open an issue or submit a pull request.

## License
This project is open-source and available under the MIT License.
