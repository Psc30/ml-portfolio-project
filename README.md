# 🌌 Exoplanet Classification Project

## 🚀 Project Overview

This project uses real-world data from confirmed exoplanets to build a machine learning model that predicts the **type of exoplanet** based on planetary and stellar features such as mass, radius, orbital parameters, and distance from Earth.

After completing data cleaning and exploratory data analysis (EDA), I engineered features and trained classification models to identify the most informative attributes for predicting exoplanet types. The ultimate goal is to understand which physical characteristics are most influential in distinguishing different classes of exoplanets, offering insights into planetary diversity beyond our solar system.

## 🎯 Objective
To build and evaluate machine learning models that classify exoplanets using astronomical data.

## 🧠 Key Project Steps
- [x] Data exploration and cleaning
- [x] Feature selection and engineering
- [x] Model selection and training
- [x] Model evaluation and tuning
- [x] fnal results and conclusion

## 🧰 Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib & Seaborn (for visualization)
- Jupyter Notebook

## 📊 Dataset
The dataset comes from a publicly available exoplanet catalog and includes physical and orbital properties for confirmed exoplanets. Each row represents one exoplanet.

| Feature Name        | Description                                                        |
| ------------------- | ------------------------------------------------------------------ |
| `name`              | Name of the exoplanet (by NASA)                                    |
| `distance`          | Distance from Earth (in light years)                               |
| `stellar_magnitude` | Brightness of the host star                                        |
| `planet_type`       | Type of planet (e.g., Gas Giant) **← target variable**             |
| `discovery_year`    | Year the planet was discovered                                     |
| `mass_multiplier`   | Mass of the planet relative to Jupiter                             |
| `mass_wrt`          | Reference unit for mass ("Jupiter")                                |
| `radius_multiplier` | Radius of the planet relative to Jupiter                           |
| `radius_wrt`        | Reference unit for radius ("Jupiter")                              |
| `orbital_radius`    | Distance of planet from its star (in AU)                           |
| `orbital_period`    | Time it takes the planet to complete one orbit (in years)          |
| `eccentricity`      | Eccentricity of the orbit (0 = circular, closer to 1 = elliptical) |
| `detection_method`  | Detection method (e.g., Radial Velocity)                           |

## 🧼 Data Cleaning
- Dropped constant columns: `mass_wrt`, `radius_wrt`
- Removed duplicate records

## 📈 Exploratory Data Analysis (EDA)
- Visualized feature distributions
- Generated correlation heatmaps
- Explored relationships between mass, radius, orbital features, and planet type

## 🔧 Feature Engineering
- Performed train/test split using stratified sampling based on `planet_type`
- Encoded the target label and categorical features
- Imputed missing values in numerical columns using median strategy
- Ensured train/test feature alignment and consistent preprocessing

## 🤖 Model Training & Evaluation
- Compared **Logistic Regression** and **Random Forest models**
- Random Forest outperformed with:
    - **CV Accuracy**: ~95.2%  
    - **Test Accuracy**: 95%
    - Strong performance across all classes, validated via classification report and confusion matrix
- Applied `RandomizedSearchCV` to tune hyperparameters
- Interpreted model results using a normalized confusion matrix

## 🔍 Results & Takeaways
- Random Forest delivered strong results across all metrics and outperformed baseline models
- Some misclassification occurred between **Super Earth**, **Neptune-like**, and **Terrestrial** classes — likely due to feature overlap
- The project demonstrated a full ML workflow from raw data to optimized model
- Additional variables (e.g., planetary density, composition) could further enhance accuracy

## 🔮 Future Work
- Incorporate additional exoplanet data (e.g., from Kepler, TESS)
- Experiment with advanced models like XGBoost or LightGBM
- Conduct feature importance analysis or dimensionality reduction (PCA, UMAP)
- Deploy the model via API or interactive dashboard for real-time predictions