# Mean Arterial Pressure Forecasting in ICU

This project evaluates machine learning architectures for forecasting **Mean Arterial Pressure (MAP)** in ICU patients, mapping a 12-hour physiological history to a 6-hour predictive horizon.

## **Core Focus**
Beyond model benchmarking, this project focuses on **domain-specific feature engineering** and **specialized data preprocessing**:
* **Clinical Feature Engineering:** Prioritizing high-impact signals like **GCS Motor Response** (neurological/ischemic indicator) and **PEEP** (respiratory context) to enhance physiological relevance.
* **Advanced Preprocessing:** Implementing a **hybrid scaling strategy** (StandardScaler for vitals and Min-Max for medications) to preserve clinical logic and prevent feature bias.
* **Data Transformation:** Converting raw EHR sequences into dynamic sliding-window tensors and utilizing semantic embeddings for categorical variables.
* **Forecasting Model Benchmarking:** Benchmarks three models, **Amazon Chronos-2**, **Multi-Horizon LSTM**, and **Temporal Fusion Transformer (TFT)**, using both univariate (MAP only) and multivariate (including exogenous variables) forecasting.

## **Main Report**
For the full analysis of the methodology, clinical logic, and comparative performance, see:
* [**final-map-prediction-report.ipynb**](./final-map-prediction-report.ipynb)

## **Model Implementations**
* **Amazon Chronos-2:** Zero-shot Transformer-based foundation model baseline.
* **Multi-Horizon LSTM:** Custom recurrent network with direct-output forecasting.
* **Temporal Fusion Transformer (TFT):** Attention-based model with built-in feature importance (VSN).

## **Data Source**
Derived from the **MIMIC-IV Clinical Database Demo (v2.2)**, available on [Kaggle](https://www.kaggle.com/datasets/montassarba/mimic-iv-clinical-database-demo-2-2).

> For full background, methodology, and evaluation details, please refer to the report final-map-prediction-report-no-code.html.
