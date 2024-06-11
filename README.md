# Anomaly-based Intrusion Detection System for Water Treatment Plant

This repository contains the implementation of an anomaly-based intrusion detection system (IDS) designed to detect cyber-attacks on water treatment plants, specifically the Secure Water Treatment (SWaT) testbed. The IDS utilizes the Random Forest algorithm, which demonstrated superior performance in accurately detecting anomalies while minimizing false positives.

## Overview

Water treatment plants are critical cyber-physical systems vulnerable to cyber-attacks that can manipulate settings and operations, potentially leading to water contamination or disruption of the treatment process. This IDS aims to identify deviations from normal system behavior by analyzing sensor readings and system logs collected during both normal operation and simulated cyber-attack scenarios.

## Dataset

The dataset used for training and evaluating the IDS is obtained from the SWaT testbed, which simulates a real water treatment plant environment. The dataset contains sensor readings and system logs collected during normal operation and under simulated cyber-attacks.

Link for dataset: https://drive.google.com/drive/folders/1zkPNPgZ0fIneML21KlLnnkOBuL8X7qK7

## Methodology

Several machine learning algorithms were explored for the anomaly-based IDS, including:

- **Isolation Forest**: Achieved an accuracy of 0.9422 and a precision of 0.51 for detecting anomalies (attacks), with a relatively high number of false positives (934 out of 178,370 normal instances).
- **Random Forest**: Achieved an accuracy of 0.9999 and a precision of 1.0 for detecting anomalies (attacks), with only 5 false positives out of 178,370 normal instances, indicating a very low false positive rate.
- **Local Outlier Factor (LOF)**: Achieved an accuracy of 0.9342 and a precision of 0.12 for detecting anomalies, with a high number of false positives (1,717 out of 178,370 normal instances).
- **One-Class Support Vector Machine (SVM)**: Achieved an accuracy of 0.9392 and a precision of 0.36 for detecting anomalies, with 1,226 false positives out of 178,370 normal instances.

The Random Forest algorithm demonstrated the best performance and was chosen for the final IDS implementation.

## Results

The Random Forest algorithm achieved an accuracy of 0.9999 and a precision of 1.0 for detecting anomalies (attacks). The confusion matrix revealed only 5 false positives out of 178,370 normal instances, indicating a very low false positive rate, which is crucial for critical infrastructure systems to avoid operational disruptions.

