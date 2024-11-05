# data-analysis
A collection of Jupyter notebooks for data analysis, focusing on data quality, anomaly detection, and defining filters across various datasets

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

- Identifying and handling outliers (e.g., identifying and filtering out zeros in specific columns).
- Defining cutoff thresholds for each dataset to flag invalid or extreme values.
- Providing clear filters to clean the data based on the domain-specific characteristics.

Notebooks:
1. **Water Data Analysis**: Identifies invalid zero values in water usage data (e.g., production use water) and applies filters to remove them.
2. **Production Volume Analysis**: Examines the production volume data to determine valid thresholds and remove anomalous entries.
3. **Energy Data Analysis**: Identifies high and low thresholds for energy consumption, filtering out extreme or invalid values.

## Water Data Analysis

The **water data analysis** notebook focuses on the following steps:

- **Detecting Zero Values**: For the year 2023, the dataset contained entries where production use water was reported as 0. These entries were deemed invalid since they contradicted other data suggesting there was production use, and thus those zeros were filtered out.
- **Determining Cutoff Values**: The notebook identifies the highest and lowest cutoff values for valid water usage based on historical data trends, domain knowledge, and statistical analysis.
- **Applying Filters**: After detecting and addressing anomalies like zeros, appropriate filters were applied to clean the dataset.

### Key Analysis Techniques:
