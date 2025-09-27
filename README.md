# Calibration of Detectors for Cosmic On Air Citizen Science Project

A Python-based data analysis project that calibrates gamma ray detectors to improve data quality and measurement consistency across multiple sensors. The project demonstrates **statistical calibration techniques**, full **error propagation**, and professional **visualization** with Matplotlib and Plotly.

**Key Libraries:** `pandas`, `numpy`, `scipy`, `matplotlib`, `plotly`

## 🎯 Project Overview

The goal of this project was to calibrate three radiation detectors used in the Cosmic On Air citizen science project by:
1. Measuring count rates from a **⁶⁰Co gamma-ray source** at multiple distances (1cm, 3cm, 6cm) and with lead collimation.
2. Applying **background correction** and **uncertainty propagation** to obtain accurate count rates.
3. Calculating **absolute efficiencies** using geometric modeling and source activity measurements.
4. Analyzing detector performance and identifying measurement inconsistencies across different setups.

## 📊 Key Results

The calibration revealed significant differences in detector performance and efficiency:

- **RadiaCode detector** showed highest sensitivity: **155.4 ± 0.3 counts per second at 1cm distance**
  (picture here)
- **Absolute efficiencies** varied considerably across measurement configurations
- **Lead-collimated setup** produced highest efficiency values for all detectors
(picture here)
The analysis provided crucial insights for improving data quality in citizen science radiation monitoring.

## ⚙️ How It Works: Analysis Pipeline

The analysis is structured in a clear pipeline within the `Codes` directory:

1. **Data Collection & Background Correction:** Raw count rates were measured and background radiation was subtracted using uncertainty propagation.
   
![Count Rate Measurement](results_plots/detector_count_rates.png)

*Figure 1: Sample count rate measurements from RadiaCode detector with lead collimation.*

2. **Efficiency Calculation:** Absolute efficiencies were calculated using `ε = R / (D × Ω)`, where R is count rate, D is source activity, and Ω is the solid angle.

3. **Uncertainty Analysis:** Full error propagation was performed using Type A and Type B uncertainty methods for all measurements.

4. **Performance Comparison:** Detector responses were analyzed across different configurations to identify consistency issues.

![Efficiency Results](results_plots/efficiency_comparison.png)

*Figure 2: Absolute efficiencies calculated for different detector configurations.*


## 📁 Repository Structure

A high-level overview of the project organization:
```
cosmic-on-air-detector-calibration-analysis/
│
├── Data/
│   └── Raw and processed data files from the experiment.
│       - Safecast detector measurements (.csv)
│       - RadiaCode detector measurements (.txt) 
│       - GMC 500 Plus detector measurements (.csv)
│       - Background radiation measurements
│
├── Codes/
│   └── The core analysis scripts and notebooks.
│       - Python files (.py) for each detector's analysis
│       - Jupyter notebooks (.ipynb) for each detector's analysis  
│       - radiacode_analysis_with_notes.ipynb: Detailed explanations of the RadiaCode analysis
│       - The complete workflow includes: data cleaning, efficiency calculation, and uncertainty propagation.
│
├── Results_Plots/
│   └── Final publication-quality figures (.png) output by the scripts.
│       - Count rate measurements for each detector
│       - Efficiency comparisons across configurations
│
├── Detector_Pictures/
│   └── Images of the detectors used in the experiment.
│       - Safecast bGeigie Zen detector
│       - RadiaCode gamma-ray spectrometer  
│       - GMC 500 Plus Geiger counter
│
└── README.md
```


## 🛠️ Technical Implementation

- **Language:** Python
- **Key Libraries:** `pandas`, `numpy`, `scipy`, `matplotlib`, `plotly`
- **Core Techniques:** Statistical calibration, error propagation, geometric efficiency calculations, data visualization.

## 👨‍💻 Skills Demonstrated

This project showcases **directly transferable data analysis skills**:

### 📊 Data Cleaning & Preprocessing
- Handled raw radiation detector data with noise and background interference
- Performed data validation and quality checks across multiple sensor types
- Created automated processing pipelines for reproducible analysis

### 📈 Statistical Analysis & Modeling
- Applied statistical methods for radiation count rate analysis
- Implemented full uncertainty propagation for scientific measurements
- Conducted efficiency calculations with geometric corrections

### 🔧 Programming & Technical Skills
- **Python Data Stack:** `pandas` for data manipulation, `numpy` for numerical computations, `scipy` for statistical analysis
- **Data Visualization:** Created professional plots with `matplotlib` and interactive charts with `plotly`
- **Experimental Data Analysis:** Developed workflows for processing real-world sensor data

## 👨‍💻 View the Analysis Code

For insight into the analysis process—including data cleaning, efficiency calculations, and uncertainty propagation—see the main analysis notebook:
**[efficiency_calculation.ipynb](codes/efficiency_calculation.ipynb)**

## 📄 License

**Report:** Copyright © 2025 Valen Lebepe. All rights reserved.
This report is provided for viewing purposes only. Redistribution, copying, or commercial use is prohibited without explicit permission.

## 👤 Author

**Valen Lebepe**  
- GitHub: [@ValenLebepe](https://github.com/ValenLebepe)
- LinkedIn: [Valen Lebepe](https://www.linkedin.com/in/valenlebepe)  
- Email: valenlebepe@gmail.com
