### 1. Setup Conda environment

```shell
conda env create -f environment.yml
conda activate scai

git clone https://github.com/praanjalmishra/ECG_scai.git
cd ECG_scai
```

### 2. Hierarchy of the Data Strucure


```bash
/ecg_data

├── device_01
│   ├── user_001
│   │   ├── ecg_day_1.csv
│   │   ├── hr_day_1.csv
│   │   └── ...day_30.cse
│   ├── user_002
│   │   ├── ecg_day_1.csv
│   │   ├── hr_day_2.csv
│   │   └── ...day_30.csv
│   └── ...
├── device_02
│   ├── user_001
│   │   ├── ecg_day_1.csv
│   │   ├── hr_day_1.csv
│   │   └── ...day_30.csv
│   ├── user_002
│   │   ├── ecg_day_1.csv
│   │   ├── hr_day_2.csv
│   │   └── ...day_30.csv
│   └── ...


```

### 3. ECG Analysis Tool

`ECG_Analysis.ipynb` contains a Python class `ECGAnalysis` designed for analyzing ECG data. The class provides various functionalities: for loading ECG data, filtering it, detecting peaks, computing heart rate, analyzing waveform intervals (PR, QRS, QT), and calculating heart rate variability (HRV).


## Features
- **Data Loading**: Load ECG data from CSV files stored in a specified directory structure.
- **Signal Processing**: Filter ECG signals using a Butterworth bandpass filter.
- **Peak Detection**: Identify peaks in the filtered ECG signal.
- **Heart Rate Computation**: Calculate average heart rate from detected peaks.
- **Waveform Analysis**: Detect and analyze various wave peaks (P, Q, R, S, T).
- **Interval Calculation**: Compute PR, QRS, and QT intervals from detected peaks.
- **Visualization**: Plot various aspects of the ECG signal and detected features.

### 4. HR and RR analysis

`HR_RR_Analysis.ipynb` contains a Python class `HealthDataLoader` designed for loading and analyzing health data including Heart Rate (HR) and Respiratory Rate (RR).

## Features
- **Data Loading**: Load HR and RR data from CSV files based on specified device, user, and days.
- **Data Preprocessing**: Convert date columns, handle missing values, and replace zeros with computed means.
- **Data Analysis**: Analyze trends in HR and RR over time, including daily averages and variations by hour.
- **Correlation Analysis**: Calculate correlations between HR and RR for daytime and nighttime periods.
- **Clustering**: Perform KMeans clustering on HR and RR data to identify patterns and visualize clusters.


