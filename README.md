# Random Forest Regressor for Predicting Generosity

This project uses machine learning to predict generosity scores from the World Happiness Report 2018 dataset. The analysis compares different regression models to understand which factors most strongly influence charitable behavior across countries.

## 📊 Dataset

The project uses the **World Happiness Report 2018 Chapter 2 Online Data** (`WHR2018Chapter2OnlineData.csv`), which contains:

- **1,562 entries** across multiple countries and years
- **19 features** covering economic, social, health, governance, and emotional well-being indicators

## 🎯 Objective

**Predict the "Generosity" score** - the residual measure of generosity beyond what log GDP per capita would predict. This helps identify countries that exhibit above-expected charitable behavior relative to their economic status.

## 🔍 Features Used

The model uses 7 key features to predict generosity:

### Economic & Material

- **Log GDP per capita** - Economic prosperity indicator

### Social & Health

- **Social support** - Perceived social support network
- **Healthy life expectancy at birth** - Health and longevity measure
- **Freedom to make life choices** - Personal autonomy and freedom

### Governance & Emotional

- **Perceptions of corruption** - Trust in institutions
- **Positive affect** - Positive emotions and experiences
- **Negative affect** - Negative emotions and stress

## 🤖 Models & Results

### Linear Regression (Baseline)

- **R² Score**: 0.268
- **MSE**: 0.019
- Simple linear relationship between features and generosity

### Random Forest Regressor (Best Model)

- **R² Score**: 0.613
- **MSE**: 0.010
- **Best Parameters** (via GridSearchCV):
  - `n_estimators`: 200
  - `max_depth`: None
  - `min_samples_split`: 2

## 📈 Feature Importance

The Random Forest model identified these as the most important predictors of generosity:

1. **Freedom to make life choices** (24.4%)
2. **Log GDP per capita** (18.6%)
3. **Positive affect** (15.6%)
4. **Perceptions of corruption** (12.1%)
5. **Healthy life expectancy at birth** (11.9%)
6. **Negative affect** (9.2%)
7. **Social support** (8.3%)

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **scikit-learn** - Machine learning models and evaluation
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization

## 📋 Project Structure

```
RandomForestRegressor/
├── RandomRegressor.ipynb       # Main analysis notebook
├── WHR2018Chapter2OnlineData.csv  # World Happiness Report dataset
├── README.md                   # Project documentation
└── LICENSE                     # MIT license
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### Running the Analysis

1. Clone this repository
2. Install the required dependencies
3. Open `RandomRegressor.ipynb` in Jupyter Notebook
4. Run all cells to reproduce the analysis

## 📊 Key Insights

- **Random Forest significantly outperforms Linear Regression** (R² improvement from 0.27 to 0.61)
- **Freedom and economic factors are strongest predictors** of generosity
- **Emotional well-being (positive affect) plays a crucial role** in charitable behavior
- **Model explains ~61% of variance** in generosity scores, indicating that predicting charitable behavior remains challenging

## 🎯 Applications

This model could help:

- **Philanthropic organizations** identify countries most likely to respond to charitable campaigns
- **Policymakers** understand social and economic levers that influence giving behavior
- **Researchers** study the relationship between material wealth and charitable behavior
- **NGOs** tailor interventions based on cultural and social factors

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

**Rudraksh Chaudhry** - Feel free to reach out for questions or collaborations!
