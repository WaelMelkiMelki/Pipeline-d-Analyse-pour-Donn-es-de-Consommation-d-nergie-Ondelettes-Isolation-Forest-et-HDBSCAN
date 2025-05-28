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
Use code with caution
bash pip install pywavelets pandas matplotlib numpy scikit-learn plotly hdbscan

## How to Run

1.  **Clone the repository:**
Use code with caution
bash git clone

2.  **Open the Jupyter Notebook or Google Colab notebook.**
3.  **Ensure the dataset is accessible:** The notebook expects the dataset at `/content/drive/MyDrive/P2M/sfmconnect.disaggregationP2M.csv`. If your file is located elsewhere, update the `file_path` variable in the code. If using Google Colab, make sure to mount your Google Drive.
Use code with caution
python from google.colab import drive drive.mount('/content/drive')

4.  **Run the cells sequentially.** The notebook is structured to perform the following steps:
    *   Install necessary libraries.
    *   Mount Google Drive (if in Colab).
    *   Load data and identify unique equipment types.
    *   Visualize power consumption for each equipment type.
    *   Perform wavelet compression on the microwave energy signal and save coefficients.
    *   Perform wavelet compression on the refrigerator energy signal.
    *   Perform anomaly detection on the refrigerator power consumption using Isolation Forest.
    *   Perform anomaly detection on the refrigerator power consumption using HDBSCAN.
    *   Perform anomaly detection on the microwave power consumption using HDBSCAN.

## Code Structure

The code is presented as a series of cells within a Jupyter Notebook or Google Colab notebook. Each cell addresses a specific part of the project's analysis pipeline.

*   **Initial Setup:** Library installations and Google Drive mounting.
*   **Equipment Analysis:** Identifying and counting unique equipment types.
*   **Visualization:** Generating time-series plots of power consumption.
*   **Wavelet Compression:** Functions and execution for signal compression and evaluation.
*   **Anomaly Detection:** Implementation of Isolation Forest and HDBSCAN for identifying anomalies in power consumption.

## Results

The notebook will output:

*   The total number of unique equipment types and their names.
*   Interactive Plotly graphs visualizing the power consumption of each appliance.
*   Compression statistics (RMSE, MAE, R², compression ratio) for the wavelet-compressed signals.
*   An interactive Plotly graph comparing the original and reconstructed signals after wavelet compression.
*   Interactive Plotly graphs visualizing the identified anomalies in the power consumption of the Refrigerator and Microwave.

## Future Work

*   Explore other wavelet families and compression ratios.
*   Apply anomaly detection to other equipment types.
*   Implement other anomaly detection algorithms for comparison.
*   Develop a more robust method for automatically identifying equipment types and their corresponding power/energy columns.
*   Analyze the impact of different pre-processing techniques on anomaly detection performance.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for any improvements or bug fixes.

## License

This project is licensed under the [Apache License] - see the LICENSE file for details.
Use code with caution
