# Electricity price forecasting for the Day-Ahead Market

This repository contains the code developed for my Diploma Thesis titled  **Electricity price forecasting for the Day-Ahead Market (DAM)** where we specifically focus on the **Greek Electricity Market (HEnEx)**.


The work focuses on short-tem electricity price forecasting using a combination of statistical, machine learning models and deep learning architectures.
Later on we emphasize the importance of two specific hyperparameters the training size and the look-back window and we provide an initial dynamic approach for the selection of the specific configuration for each day of 2024.


## Methodology Review 
The overall methodology of this thesis is shown in the following figure:

<img width="1681" height="1715" alt="overall_methodology_schema (1)" src="https://github.com/user-attachments/assets/2f45ca15-54e5-4937-9cff-1fa0e0634b97" />

The pipeline for the creation of the architectures included model selection out of:

- **Regression & ensemble models**
  - Random Forest
  - Gradient Boosting
  - XGBoost / LightGBM
- **Deep Learning models**
  - Long Short-Term Memory (LSTM)
  - Temporal Fusion Transformer (TFT)

and we continue with:

- Extensive **feature engineering**
- **Hyperparameter tuning**
- Two **multi-output forecasting strategies**:
  - Single-step autoregressive forecasting
  - Direct multi-step forecasting
- Incorporation of **same-day exogenous variables** 

Following the creation and evaluation of the forecasting models, we continued with the creation of the dynamic hyperparameter selection approach. We employed **regression  and classifier models**  and fine tuned the architectures with hyperparameter tuning and feature engineering.

## Data

The dataset was extracted from the **Day-Ahead Market data** section of the **Hellenic Energy Exchange (HEnEx)** 
https://www.enexgroup.gr/el/markets-publications-el-day-ahead-market

## Repository Structure

The repository is organized is model specific folders as well as a seperate folder that includes the data extraction notebooks.

## Full report

The full report of the thesis can be found in thesis_loukiapavlana_final.pdf in English, with an extensive Greek summary.
