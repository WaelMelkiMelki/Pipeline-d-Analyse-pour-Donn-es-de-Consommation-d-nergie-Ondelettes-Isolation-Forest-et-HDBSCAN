# Pipeline-d-Analyse-pour-Donn-es-de-Consommation-d-nergie-Ondelettes-Isolation-Forest-et-HDBSCAN
# Smart Home Energy Disaggregation and Analysis

This project analyzes smart home energy consumption data to identify and visualize the power usage of individual appliances. It also explores techniques for signal compression using wavelets and anomaly detection using Isolation Forest and HDBSCAN algorithms.

## Project Overview

The primary goals of this project are:

1.  **Identify and Count Equipment Types:** Extract and count the unique types of equipment present in the dataset.
2.  **Visualize Equipment Power Consumption:** Generate time-series plots to visualize the active power consumption for each unique equipment type.
3.  **Signal Compression using Wavelets:** Apply wavelet decomposition (specifically the 'coif5' wavelet) to compress the energy consumption signal of a selected appliance (Microwave) and evaluate the compression effectiveness using metrics like RMSE, MAE, and R². The coefficients of the original signal are also saved for potential further analysis.
4.  **Anomaly Detection:** Implement anomaly detection on the power consumption data of specific appliances (Refrigerator and Microwave) using two different methods:
    *   **Isolation Forest:** A tree-based anomaly detection algorithm.
    *   **HDBSCAN:** A density-based clustering algorithm that can identify noise points as anomalies.

## Dataset

The project uses a CSV file containing smart home energy consumption data. The file path is expected to be:
`/content/drive/MyDrive/P2M/sfmconnect.disaggregationP2M.csv`

The dataset is assumed to contain columns related to equipment names and their corresponding power and energy consumption.

## Requirements

To run this project, you will need the following libraries installed:

*   `pandas`
*   `pywavelets`
*   `numpy`
*   `scikit-learn`
*   `plotly`
*   `hdbscan`

You can install these using pip:
