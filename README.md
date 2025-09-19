# Torres Strait Coral Reef Stress Analysis

A comprehensive analysis of Great Barrier Reef coral stress monitoring data for the Torres Strait region, using data from NOAA's Coral Reef Watch program.

## Overview

This project provides a professional Jupyter notebook that analyzes 40 years (1985-2025) of sea surface temperature (SST) and coral stress data from the Torres Strait region of the Great Barrier Reef. The analysis creates NOAA-style visualizations highlighting periods of significant coral stress events.

## Features

- **Comprehensive Data Analysis**: Processes daily SST measurements spanning 1985-2025
- **Professional Visualization**: Creates publication-quality charts matching NOAA's styling standards
- **Stress Event Highlighting**: Identifies and visualizes coral bleaching warnings and alert-level events
- **Climatological Context**: Includes long-term monthly temperature averages for comparison
- **Statistical Analysis**: Provides detailed statistics on temperature patterns and stress events

## Data Source

The analysis uses data from **NOAA's Coral Reef Watch** program:

- **Dataset**: Torres Strait Virtual Station Data
- **URL**: https://coralreefwatch.noaa.gov/product/vs/data/torres_strait.txt
- **Provider**: National Oceanic and Atmospheric Administration (NOAA)
- **Program**: Coral Reef Watch
- **Coverage**: Daily measurements from January 1985 to September 2025
- **Parameters**:
  - Sea Surface Temperature (Min, Max, 90th percentile)
  - Sea Surface Temperature Anomalies
  - Degree Heating Weeks (DHW)
  - Bleaching Alert Area indicators

### Data Description

The Torres Strait dataset contains the following key measurements:

| Parameter | Description |
|-----------|-------------|
| `SST_MIN` | Daily minimum sea surface temperature (°C) |
| `SST_MAX` | Daily maximum sea surface temperature (°C) |
| `SST@90th_HS` | Sea surface temperature at 90th percentile hotspot (°C) |
| `SSTA@90th_HS` | Sea surface temperature anomaly at 90th percentile (°C) |
| `DHW_from_90th_HS>1` | Degree Heating Weeks from 90th percentile threshold |
| `BAA_7day_max` | 7-day maximum Bleaching Alert Area |

## Installation & Usage

### Prerequisites

```bash
pip install pandas numpy matplotlib requests
```

### Running the Analysis

1. Clone this repository:
```bash
git clone https://github.com/lwsinclair/gbr-stress.git
cd gbr-stress
```

2. Open the Jupyter notebook:
```bash
jupyter notebook torres_strait_analysis.ipynb
```

3. Run all cells to:
   - Download the latest data from NOAA
   - Process and analyze the dataset
   - Generate the visualization
   - Display summary statistics

## Key Results

The analysis reveals:

- **40 years of continuous monitoring** from 1985-2025
- **Temperature trends** and seasonal patterns in the Torres Strait
- **Coral stress events** including bleaching warnings and alert-level conditions
- **Climatological baseline** for temperature comparisons
- **Statistical summaries** of stress event frequency and intensity

## Visualization

The main output is a comprehensive time series chart featuring:

- **SST Time Series**: Daily 90th percentile sea surface temperatures
- **Temperature Range**: Min-max daily temperature envelope
- **Climatology**: Monthly average temperatures for reference
- **Stress Periods**: Color-coded background highlighting for:
  - 🟠 **Bleaching Warning** (SSTA > 1°C)
  - 🔴 **Alert Level 2** (DHW ≥ 8°C-weeks)
- **DHW Timeline**: Degree Heating Weeks on secondary axis
- **Reference Lines**: Bleaching threshold temperatures

## Scientific Context

### Coral Bleaching Thresholds

The analysis uses established coral bleaching thresholds:

- **Bleaching Warning**: Sea surface temperature anomaly > 1°C above long-term average
- **Alert Level 1**: Degree Heating Weeks ≥ 4°C-weeks
- **Alert Level 2**: Degree Heating Weeks ≥ 8°C-weeks (severe bleaching likely)

### Torres Strait Significance

The Torres Strait represents a critical region for coral reef monitoring as it:

- Connects the Great Barrier Reef to Indo-Pacific coral systems
- Experiences significant thermal stress events
- Serves as an early warning indicator for reef-wide bleaching events
- Contains important cultural and ecological values

## Data Quality & Limitations

- **Temporal Coverage**: Daily data from 1985-present with minimal gaps
- **Spatial Resolution**: 5km satellite-derived measurements
- **Validation**: Data undergoes NOAA quality control procedures
- **Limitations**: Satellite measurements may differ from in-situ temperatures

## Contributing

Contributions are welcome! Please feel free to:

- Report issues or bugs
- Suggest improvements to the analysis
- Add additional visualization features
- Extend the analysis to other reef regions

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **NOAA Coral Reef Watch** for providing the monitoring data
- **NOAA Satellite and Information Service** for satellite SST measurements
- **Great Barrier Reef Marine Park Authority** for regional context
- The scientific community working on coral reef conservation

## References

1. NOAA Coral Reef Watch. Torres Strait Virtual Station Data. https://coralreefwatch.noaa.gov/
2. Liu, G., et al. (2014). Reef-scale thermal stress monitoring of coral ecosystems: new 5-km global products from NOAA Coral Reef Watch. Remote Sensing, 6(11), 11579-11606.
3. Eakin, C. M., et al. (2010). Caribbean corals in crisis: record thermal stress, bleaching, and mortality in 2005. PloS one, 5(11), e13969.

## Contact

For questions about this analysis, please open an issue on this repository.

---

*Generated using NOAA Coral Reef Watch data. This analysis is provided for educational and research purposes.*