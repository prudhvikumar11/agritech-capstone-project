# AgriTech Capstone Project

A data analysis and machine learning capstone project focused on agricultural productivity and planning. The project combines crop production, rainfall, precipitation, fertilizer, irrigation, and FAOSTAT-related data to investigate productivity patterns and support agricultural decision-making.

## Project Objectives

The analysis addresses four business objectives:

1. **Crop productivity and seasonal performance**  
   Identify high-yield crops, seasonal performance, and productivity trends to support agricultural planning.

2. **Irrigation infrastructure and crop performance**  
   Analyze irrigation project distribution, completion progress, and relationships with agricultural performance.

3. **Rainfall and climate variability**  
   Analyze rainfall and precipitation patterns over time to understand variability relevant to agricultural planning.

4. **Fertilizer usage and productivity**  
   Analyze fertilizer consumption trends and relationships with crop yields to understand agricultural input usage and sustainability.

## Analytical Workflow

The notebook follows a structured analytics and machine-learning workflow:

- Dataset loading and initial inspection
- Exploratory Data Analysis (EDA)
- Univariate and bivariate analysis
- Seasonal and crop-level productivity analysis
- Irrigation project analysis
- Rainfall and precipitation trend analysis
- Fertilizer consumption analysis
- Descriptive statistics
- Hypothesis testing
  - Z-test
  - T-test
  - Chi-square test
  - Correlation analysis
- Feature engineering
- Machine learning
  - Linear Regression
  - Logistic Regression
  - K-Nearest Neighbors (KNN)
  - K-Means Clustering
- Model evaluation and interpretation

## Datasets

The notebook uses the following project datasets:

| Dataset | Purpose |
|---|---|
| `crop_production.csv` | Crop area, production, yield, crop and season information |
| `rainfall.csv` | Historical rainfall/yield-related agricultural data |
| `precipitation.csv` | Annual precipitation data |
| `fertilizer.csv` | Fertilizer-use and crop-yield related data |
| `irrigation.csv` | Irrigation project information by state/UT |
| `faostat.xlsx` | FAOSTAT dataset used in the analysis |

The notebook originally referenced these files using local Windows paths. The GitHub-ready notebook uses the repository-relative `data/` directory instead.

> **Data availability:** Only upload datasets to GitHub if their redistribution is permitted. If they are not redistributable, keep the files out of the repository and provide instructions in `data/README.md` for obtaining them.

## Key Analysis Results

The notebook reports the following model results:

### Linear Regression

The regression model achieved:

- **R²: 0.9024**
- **MAE: 0.1610**
- **RMSE: 0.2119**

The analysis uses regression to model the relationship between the engineered agricultural features and the selected productivity target.

### Classification

The notebook also evaluates:

- Logistic Regression
- KNN Classifier

The reported Logistic Regression results include approximately **60% accuracy** and a **weighted F1 score of 0.5867**. The KNN model is evaluated using accuracy and classification metrics after feature scaling and hyperparameter search.

### K-Means Clustering

The notebook groups crop-season observations based on production-related features.

Reported clustering metrics for the selected three-cluster solution:

- **Silhouette Score: 0.6991**
- **Calinski-Harabasz Score: 282.41**
- **Davies-Bouldin Index: 0.4115**

The notebook interprets the three clusters as broadly representing low-, medium-, and high-production patterns.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- SQLAlchemy

## Repository Structure

```text
agritech-capstone-project/
│
├── README.md
├── agritech_capstone_project.ipynb
├── requirements.txt
├── .gitignore
│
└── data/
    ├── README.md
    ├── crop_production.csv
    ├── rainfall.csv
    ├── precipitation.csv
    ├── fertilizer.csv
    ├── irrigation.csv
    └── faostat.xlsx
```

## Getting Started

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd agritech-capstone-project
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

**Windows**

```bash
.venv\Scripts\activate
```

**macOS/Linux**

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the datasets

Place the required datasets under:

```text
data/
```

The filenames should match the names used by the notebook.

### 5. Start Jupyter

```bash
jupyter notebook
```

Open:

```text
agritech_capstone_project.ipynb
```

and run the notebook from top to bottom.

## Notes on Reproducibility

The cleaned notebook removes machine-specific Windows file paths and uses:

```python
DATA_DIR = Path("data")
```

This makes the project portable across machines and suitable for GitHub.

Model training uses fixed random seeds where applicable, including `random_state=42`, to make the analysis more reproducible.

## Project Takeaways

The analysis highlights that agricultural productivity is influenced by multiple dimensions rather than cultivated area alone. The project examines crop and seasonal differences alongside irrigation infrastructure, rainfall/precipitation variability, and fertilizer usage.

The clustering analysis additionally shows that crop-season combinations can exhibit distinct production patterns, meaning the same crop can fall into different production groups depending on its agricultural season.

## Author

**Prudhvi Kumar**

GitHub: https://github.com/prudhvikumar11

LinkedIn: https://www.linkedin.com/in/prudhvi-kumar-k-893975153/
