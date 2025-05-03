# DonorsChoose Project Risk Model

This project helps identify which classroom projects on DonorsChoose are least likely to get funded, so that a content expert can review them and improve their chances.
Dataset: https://www.kaggle.com/c/kdd-cup-2014-predicting-excitement-at-donors-choose/data 

---

## Files

- `MLF_project.ipynb` – The main Jupyter Notebook for data analysis and modeling.
- `projects.csv`, `outcomes.csv`, `essays.csv`, `resources.csv`, `donations.csv` – Input datasets.
- `at_risk_projects.csv` – Output file listing the bottom 10% of projects least likely to be funded.
- `README.md` – This file with instructions and explanation.

---

## Steps for running the project

### Step 1: Clone or Download

Go to your GitHub repo and either:

- Click **Code > Download ZIP**, or  
- Run this in your terminal:

```bash
git clone https://github.com/1112hass/your-repo-name.git
cd your-repo-name
```

### Step 2: Install Python Packages

Make sure Python 3.x is installed, then install required libraries:

```bash
pip install pandas numpy matplotlib seaborn geopandas scikit-learn textblob
python -m textblob.download_corpora
```

### Step 3: Launch Notebook

```bash
jupyter notebook
```

Open `MLF_project.ipynb` and run all cells.

---

## What This Does

- Loads and merges project, essay, donation, and resource data
- Adds sentiment and text features from project essays
- Visualizes geographic and numeric data
- Trains a model to predict funding success
- Outputs a CSV with at-risk projects needing expert review

