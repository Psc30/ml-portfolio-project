# 🌌 Exoplanet Classification Project

## Project Overview

In this project, I used a real-world dataset of confirmed exoplanets to build a classification model that predicts the **type of exoplanet** based on planetary and stellar attributes such as mass, radius, orbital characteristics, and distance from Earth. 

After performing data cleaning and exploratory data analysis (EDA), I completed feature engineering to prepare the data for building classification models. The goal of this project is to identify which physical features are most influential in the classification task, offering insights into the diversity of planets beyond our solar system.

## Objective
To build and evaluate a machine learning model using real-world data.

## Project Steps
- [x] Data exploration and cleaning
- [x] Feature selection/engineering
- [ ] Model selection and training
- [ ] Model evaluation
- [ ] Results and conclusion

## Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib/Seaborn (for visualization)
- Jupyter Notebook

## 📊 Dataset
The dataset comes from a publicly available exoplanet catalog and contains physical and orbital properties of exoplanets. Each row represents one exoplanet.

| Feature Name        | Description                                                        |
| ------------------- | ------------------------------------------------------------------ |
| `name`              | Name of the exoplanet by NASA                                      |
| `distance`          | Distance from Earth (in light years)                               |
| `stellar_magnitude` | Brightness of the host star                                        |
| `planet_type`       | Type of planet (e.g., Gas Giant) **← target variable**             |
| `discovery_year`    | Year the planet was discovered                                     |
| `mass_multiplier`   | Mass of the planet relative to Jupiter                             |
| `mass_wrt`          | Reference unit for mass (always "Jupiter")                         |
| `radius_multiplier` | Radius of the planet relative to Jupiter                           |
| `radius_wrt`        | Reference unit for radius (always "Jupiter")                       |
| `orbital_radius`    | Distance of planet from its star (in AU)                           |
| `orbital_period`    | Time it takes the planet to complete one orbit (in years)          |
| `eccentricity`      | Eccentricity of the orbit (0 = circular, closer to 1 = elliptical) |
| `detection_method`  | Detection method (e.g., Radial Velocity)                           |

## 🧼 Data Cleaning
- Dropped constant columns: mass_wrt, radius_wrt
- Removed duplicate records

## 📈 Exploratory Data Analysis (EDA)
- Visualized feature distributions
- Generated correlation heatmaps
- Explored relationships between mass, radius, orbital features, and planet type

## 🔧 Feature Engineering
- Performed train/test split using stratified sampling based on `planet_type`
- Label encoded the target variable `planet_type`
- One-hot encoded the `detection_method` feature
- Imputed missing values in numerical columns using median strategy
- Ensured train/test feature alignment and consistent preprocessing

## 🔜 Next Steps
- Train and evaluate classification models
- Summarize key findings, insights, and feature importances
- Update this README with final conclusions and model performance once the project is complete
