# DonorsChoose Project Risk Model

This project supports [DonorsChoose.org](https://www.donorschoose.org/), a crowdfunding platform for public school teachers in the United States. The objective is to predict which classroom projects are at risk of not being fully funded before they expire, helping the platform prioritize expert review on the most vulnerable proposals.

Currently, DonorsChoose relies on a digital content expert who can manually review only about 10% of daily project submissions. Our model assists in identifying and ranking projects most likely to go unfunded.

## Dataset

The data used comes from the [Kaggle KDD Cup 2014](https://www.kaggle.com/c/kdd-cup-2014-predicting-excitement-at-donors-choose/data). It includes the following CSV files:

- `projects.csv`
- `outcomes.csv`
- `essays.csv`
- `resources.csv`
- `donations.csv`

> Note: The dataset is too large to upload to GitHub. Please download it from [this Google Drive folder](https://drive.google.com/drive/folders/1USin0LLD1-w-SvOrU_2CohF_1_BxYk1U?usp=sharing) and place all five files in the root directory of the project.

## Model Summary

Three classification models were trained and evaluated:

- Logistic Regression
- Random Forest
- XGBoost

**XGBoost** demonstrated the strongest performance:

- ROC AUC: 0.69
- F1 Score: 0.79

It also showed high precision when identifying the top 10% of projects at highest risk, aligning well with the expert review capacity.

### Key Features

- Total project cost
- Quantity of requested resources
- Teacher experience on the platform

## Requirements

Install dependencies using:

```bash
pip install numpy pandas scikit-learn xgboost imbalanced-learn matplotlib seaborn geopandas
