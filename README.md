# Scalable Machine Learning Model for Anomaly Detection in Ethereum Transactions

This project implements a scalable machine learning pipeline for detecting anomalous transactions on the Ethereum blockchain using Python. It leverages various anomaly detection algorithms and data processing techniques to identify potentially fraudulent or unusual activities from blockchain transaction data.

---

## Overview

The project focuses on building an effective and scalable anomaly detection system using transaction features extracted from Ethereum blockchain data. The workflow includes:

- Data collection and cleaning of Ethereum transaction datasets
- Feature engineering and selection to identify important transaction characteristics
- Pre-processing and normalization of features for model input
- Training and evaluation of multiple anomaly detection models including:
  - Isolation Forest
  - One-Class SVM
  - Minimum Covariance Determinant (Elliptic Envelope)
- Comparing model performance using accuracy metrics
- Marking transactions predicted as anomalies for further analysis

---

## Features

- **Multiple anomaly detection algorithms:** Isolation Forest, One-Class SVM, and Elliptic Envelope.
- **Robust feature engineering:** Statistics on transaction timings, values, contract activity, ERC20 token transfers, and more.
- **Data scaling and normalization:** Using standard scalers and MinMax scaling for better model convergence.
- **Train-test split:** 75% training and 25% testing data split with reproducible random state.
- **Performance evaluation:** Accuracy metrics and reports to assess anomaly detectors.
- **Visualization:** Use of matplotlib for plotting learning curves and results (optional).

---

## Dependencies

- Python 3.6+
- pandas
- numpy
- scikit-learn
- xgboost
- matplotlib



Install dependencies via pip:

pip install pandas numpy scikit-learn xgboost matplotlib


---

## Usage

1. **Prepare data:** Ensure Ethereum transaction CSV files are available as used in the project (`rD6thSEMProject.csv` and others).

2. **Run the notebook/script:** Execute the main Python notebook/script which performs the following steps:
   - Data loading and preprocessing
   - Feature selection and scaling
   - Model training and testing
   - Anomaly detection result analysis

3. **Analyze output:** Review accuracy scores for different methods and examine marked anomalies.

---

## File Structure

- `paste.txt` - Python code notebook/script with full data loading, preprocessing, model training, and evaluation pipeline.
- `paste-2.txt` - Dataset snippets or additional code used for transaction data handling and model testing.

---

## Model Details

- **Isolation Forest:** Achieved highest accuracy (~99%) in detecting anomalies.
- **One-Class SVM:** Another tested method with slightly lower accuracy (~97%).
- **Elliptic Envelope:** Statistical method tested with high robustness (~98.7%) but warnings on covariance matrix rank.

---

## Notes

- The dataset includes features like transaction hash, block number, timestamps, sender and receiver addresses, transaction values, fees, and historical token prices.
- Labels include flags indicating known anomalies (-1).
- Some warnings related to matrix calculations in Elliptic Envelope implementation.
- Scaling methods applied prior to model training to normalize feature ranges.

---

## Future Improvements

- Integration of more advanced feature extraction.
- Implementation of real-time detection pipelines.
- Use of deep learning or ensemble methods for anomaly detection.
- Visualization dashboard for flagged transactions.
- Automated alerting or reporting system for suspicious activities.

---

## Acknowledgments

This project was developed as part of an academic or research coursework on scalable machine learning applications, focusing on blockchain analytics and cybersecurity.

---

Feel free to contact for questions or collaboration ideas!

