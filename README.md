# Data Analysis for Cutoff Values in Water, Production Volume, and Energy Datasets

This repository contains Jupyter notebooks that analyze water usage, production volume, and energy data to determine the highest and lowest cutoff values, identify outliers, and apply filters to improve data quality. The analysis focuses on detecting specific data issues such as erroneous zero values and other anomalies, with the goal of ensuring that each dataset accurately reflects valid measurements. The notebooks document the steps for each dataset and define filters for data cleaning.

## Table of Contents
1. [Overview](#overview)
2. [Water Data Analysis](#water-data-analysis)
3. [Production Volume Analysis](#production-volume-analysis)
4. [Energy Data Analysis](#energy-data-analysis)
5. [Usage](#usage)
6. [Contributing](#contributing)
7. [License](#license)
8. [Acknowledgments](#acknowledgments)

## Overview

This repository contains separate Jupyter notebooks dedicated to analyzing and cleaning datasets for three domains: water usage, production volume, and energy consumption. The goal of each analysis is to identify the highest and lowest cutoff values, detect anomalies such as zeros or other outliers, and apply appropriate filters to improve the quality of the data.

Each notebook follows a similar approach but is focused on a different dataset. The analysis involves:

- Identifying and handling outliers.
- Defining cutoff thresholds for each dataset to flag invalid or extreme values.
- Providing clear filters to clean the data based on the domain-specific characteristics.

Notebooks:
1. **Water Data Analysis**: Identifies invalid zero values in water usage data (e.g., production use water) and applies filters to remove them.
2. **Production Volume Analysis**: Examines the production volume data to determine valid thresholds.
3. **Energy Data Analysis**: Identifies high and low thresholds for energy consumption, filtering out extreme or invalid values.

## Water Data Analysis

The **water data analysis** notebook focuses on the following steps:

- **Detecting Zero Values**: For the year 2023, the dataset contained entries where production use water was reported as 0. These entries were deemed invalid since they contradicted other data suggesting there was production use (['watproduse'] == 'Yes'), and thus those zeros were filtered out.  2023 produced more zeros than prior years becuase of the addition of watsourcetrackoptall.  Prior to 2023 when watsourcetrackopt = 'no', all values were null, 2023 and beyond watsourcetrackopt = 'no' or watsourcetrackoptall = 'no' will produce a zero instead of NULL.

- **Determining Cutoff Values**: The notebook identifies the highest and lowest cutoff values for valid water usage based on historical data trends, domain knowledge, and statistical analysis.
- **Applying Filters**: After detecting and addressing anomalies like zeros, appropriate filters were applied to clean the dataset.

### Key Analysis Techniques:
- Zeros were flagged and removed if the dataset indicated water usage should have been greater than zero.
- Cutoff thresholds for valid water usage were established using scatter plot outlier analysis.

## Production Volume Analysis

The **production volume analysis** notebook follows a similar approach to the water analysis, focusing on identifying:

- **Anomalies and Cutoff Values**: Identifies potential anomalies in the production volume data (e.g., values that fall outside expected production ranges).
- **Zero or Null Values**: Analyzes production volumes that are reported as zero or null and evaluates whether they should be removed or flagged.
- **Filter Application**: Defines a filter based on the determined cutoffs and applies it to clean the data, ensuring that only valid production volume data is retained.

### Key Analysis Techniques:
- Statistical analysis to define the valid range for production volume data.
- Filtering out rows where production volume is reported as zero when it is not plausible.

## Energy Data Analysis

The **energy data analysis** notebook focuses on:

- **Identifying Extreme Values**: Examines the energy dataset for unusually high or low values that may be outliers.
- **Defining Valid Cutoff Ranges**: Establishes valid ranges for energy consumption based on historical data and domain expertise.
- **Filtering Invalid Data**: Similar to the water and production volume datasets, this notebook filters out values that fall outside the acceptable range.

### Key Analysis Techniques:
- Anomaly detection for extreme values in energy consumption.
- Statistical methods to calculate the highest and lowest acceptable values for energy data.

## Usage

To run the analysis for any of the datasets, follow these steps:

### Prerequisites

- Python 3.x
- Jupyter Notebook or JupyterLab
- Required Python libraries (listed below)

### Installation

1. Clone the repository:
   `git clone https://github.com/yourusername/data-analysis.git`

2. Navigate to the project directory:
   `cd data-analysis`

3. Install dependencies:
   `pip install -r requirements.txt`

4. Launch Jupyter Notebook:
   `jupyter notebook`

5. Open and run the desired notebook for water, production volume, or energy analysis to explore and filter the data.

Each notebook contains detailed steps, explanations, and the filters applied to clean the data.

## Contributing

We welcome contributions to improve the analysis or suggest improvements. If you'd like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request to merge your changes into the main repository.

Please ensure that any new code adheres to the existing structure and is well-documented.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the authors of [Pandas](https://pandas.pydata.org/) for providing the tools for data manipulation and analysis.
- [Matplotlib](https://matplotlib.org/) and [Seaborn](https://seaborn.pydata.org/) for their excellent visualization libraries that helped with identifying data patterns.
