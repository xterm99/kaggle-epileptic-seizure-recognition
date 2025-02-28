# kaggle-epileptic-seizure-recognition
Abstract del trabajo

## Problem Context
Epilepsy is a neurological disorder characterized by recurrent seizures resulting from abnormal, excessive neuronal activity in the brain. These seizures manifest due to synchronized electrical discharges within neuronal networks, disrupting normal brain function.

Electroencephalography (EEG) is a fundamental tool in diagnosing and studying epilepsy. It records the brain's electrical activity via electrodes placed on the scalp, capturing waveforms that reflect the underlying neuronal dynamics. In healthy individuals, EEG signals display organized patterns with characteristic waveforms corresponding to different brain states, such as alpha (8–12 Hz) and beta (12–30 Hz) rhythms. However, in individuals with epilepsy, EEG signals exhibit distinctive abnormalities, including sharp spikes, spike-and-wave complexes, and high-frequency oscillations, indicative of disorganized neuronal activity.

<figure style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/cb247b9c-3309-47ac-8707-639b69792cb3" alt="EEG Patterns" width="500">
  <figcaption style="font-size: 0.85em; font-style: italic; display: block; margin-top: 5px;">
    Figure 1: Typical EEG patterns in an epileptic seizure.
  </figcaption>
</figure>


Accurate identification of these epileptiform patterns is crucial for effective diagnosis and management of epilepsy. However, manual interpretation of EEG recordings is time-consuming and prone to subjective bias. This underscores the need for automated, reliable methods to detect and classify epileptic seizures. This project addresses this need by implementing pattern recognition techniques for epileptic seizure detection, aiming to enhance diagnostic precision and inform therapeutic strategies.

## Dataset

The dataset used in this study is sourced from [Kaggle](https://www.kaggle.com/datasets/harunshimanto/epileptic-seizure-recognition) and is originally derived from the UCI Machine Learning Repository.

### Data Structure
The dataset consists of EEG recordings from **500 individuals**, each with a **23.6-second** brain activity recording sampled into **4097 data points**. Each data point represents the EEG signal at a specific time.

To enhance usability, the original data was segmented into **1-second chunks**, each containing **178 time points**. This resulted in a total of **11,500 samples (500 individuals × 23 segments per individual)**. The dataset is formatted as a CSV file where:

- **Columns 1-178** contain EEG signal values.
- **Column 179** (`y`) represents the class label.

### Class Labels
The dataset is originally multi-class, with labels representing different brain states:

- **1** – Seizure activity (epileptic seizure).
- **2** – EEG recorded from the brain region affected by a tumor.
- **3** – EEG recorded from a healthy brain region in a tumor-affected patient.
- **4** – EEG recorded with eyes closed.
- **5** – EEG recorded with eyes open.

For seizure detection tasks, this dataset is often used for **binary classification**, where **class 1 (seizure activity) is distinguished from all other classes**.

For more details, refer to the [Kaggle dataset page](https://www.kaggle.com/datasets/harunshimanto/epileptic-seizure-recognition).

## Organization of this Repository

This repository is structured into a series of notebooks, each focusing on a key stage of the epileptic seizure detection pipeline. The organization is as follows:

- **`0_Initial_Analysis_and_Preprocessing`**: This notebook provides a superficial exploratory data analysis (EDA), checking missing values, class imbalance and visualizing of EEGs.

- **`1_Feature_Engineering`**: This section extracts meaningful features from the EEG signals to enhance model performance, including time and frequency domain features, and other relevant signal processing techniques.

- **`2_Dimensionality_Reduction`**: Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA) are applied to reduce the feature space while preserving essential information.

- **`3_Feature_Selection`**: Unlike dimensionality reduction, which transforms the feature space, this step focuses on selecting the most relevant features for seizure classification. Various feature selection techniques are explored to improve model efficiency and interpretability.

- **`4_Models_and_Evaluation`**: This notebook implements different classifiers, evaluates their performance using appropriate metrics, and compares various approaches to identify the most effective models and feature sets.


## Conclusions

## Bibliography

https://www.kaggle.com/datasets/harunshimanto/epileptic-seizure-recognition
