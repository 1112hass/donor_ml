# DonorsChoose Project Risk Model

**Dataset**: [Kaggle KDD Cup 2014](https://www.kaggle.com/c/kdd-cup-2014-predicting-excitement-at-donors-choose/data)

This project supports DonorsChoose.org, a crowdfunding platform for public school teachers in the United States, by predicting which classroom projects are most at risk of not being fully funded before they expire. The platform currently relies on a digital content expert who can manually review only a small fraction of daily submissions, approximately ten percent.

Our objective is to develop a predictive model that ranks projects by their likelihood of going unfunded, thereby helping allocate expert attention where it is most urgently needed.

The analysis is based on data from the DonorsChoose 2014 KDD Cup, which includes structured, semi-structured, and unstructured features such as project costs, subject categories, grade levels, school-level poverty indicators, and essay content written by teachers.

After merging, cleaning, and engineering features, we trained and evaluated three classification models:
- Logistic Regression
- Random Forest
- XGBoost

Among the three, **XGBoost** achieved the strongest performance, with:
- Area Under the ROC Curve (AUC): 0.69
- F1 Score: 0.79

It also demonstrated strong precision among the top ten percent of highest-risk predictions, which corresponds to the platform’s expert review capacity.

Important predictive features included:
- Total project cost
- Resource quantity
- Teacher experience on the platform

We recommend integrating this model into DonorsChoose’s project submission system to automatically identify high-risk proposals for review. This targeted intervention approach can help improve funding success rates, optimize limited human resources, and support more equitable educational opportunities.

## Code

- `MLF_project.ipynb` – The main Jupyter Notebook for data analysis and modeling.

## Datasets

The dataset is too large to push to GitHub. Please download from the following link and place the files in the project root directory:

[Google Drive Dataset Link](https://drive.google.com/drive/folders/1USin0LLD1-w-SvOrU_2CohF_1_BxYk1U?usp=sharing)

Required data files:
- `projects.csv`
- `outcomes.csv`
- `essays.csv`
- `resources.csv`
- `donations.csv`

## Requirements

| Package           | Tested Version |
|-------------------|----------------|
| Python            | 3.9+           |
| numpy             | ≥ 1.24         |
| pandas            | ≥ 2.0          |
| scikit-learn      | ≥ 1.4          |
| xgboost           | ≥ 2.0          |
| imbalanced-learn  | ≥ 0.11         |
| matplotlib        | ≥ 3.8          |
| seaborn           | ≥ 0.13         |
| geopandas         | ≥ 0.14         |

Install all dependencies in one step:

```bash
pip install numpy pandas scikit-learn xgboost imbalanced-learn matplotlib seaborn geopandas

