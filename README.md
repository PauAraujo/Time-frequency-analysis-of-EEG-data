## Time-resolved Frequency Analysis of EEG Traces
This repository contains the code and data for a project that performed a time-resolved frequency analysis on EEG traces. The objective was to identify spectral features and shifts in EEG power across certain frequency bands, specifically the low gamma band (30-60 Hz), in response to linguistic stimuli.

## Dataset
The data used in this project is a partial analysis of the RITA dataset, published by [Roncaglia-Denissen et al](https://journals.sagepub.com/doi/10.1177/0267658314554497) in 2015, featuring EEG traces from Turkish individuals in the early stages of learning German. The EEG data were collected using an electrode cap with 65 electrodes in the 10-20 system at a sampling rate of 500 Hz.

## Structure
The EEG data for both conditions are structured as 3D NumPy arrays with the following dimensions:

- 0th dimension: Trial repetitions
- 1st dimension: Number of channels
- 2nd dimension: Number of samples in a trial (276 samples for the baseline condition and 751 samples for the evoked period)
  
## Methodology
The project unfolds in two key sections:

1) Exploratory data analysis of the EEG traces to understand the available data.
2) Time-frequency analysis using time-frequency representations (TFRs) for both conditions.

The Fast Fourier Transform (FFT) is used as part of the time-frequency analysis. FFT is a powerful tool that allows us to decompose a signal into its constituent frequencies. In this project, FFT is used to convert the EEG time-series data from the time domain to the frequency domain, making it possible to analyze the power of the EEG signal across different frequency bands.

This analysis focuses on the relative differences within each participant to offset any uncontrolled between-subject effects that might occur due to individual variations. 
