🐝 Artificial Intelligence Analysis of Pollinator Population Trends in the UK

This project investigates whether machine learning can be used to analyse and predict pollinator population trends in the United Kingdom.

The project combines UK biodiversity datasets, a custom Genetic Algorithm (GA) for temporal window and feature selection, and Support Vector Regression (SVR) to model wild bee occupancy trends.

🎯 Project Overview

Pollinating insects play an important role in biodiversity and agriculture, but monitoring population changes across long periods can be challenging.

This project developed an AI-driven proof of concept using wild bee occupancy as a biodiversity indicator and investigated whether other insect population indicators could be used as predictors of wild bee trends.

The analysis was designed around potential use by environmental and agricultural stakeholders, including DEFRA and biodiversity monitoring initiatives.

🧠 Approach

The project followed an end-to-end machine learning workflow:

1. Data Integration
    * Combined multiple biodiversity datasets using outer joins to maximise temporal coverage.
    * Standardised columns and numerical formats.
    * Resolved structural inconsistencies and invalid entries.
2. Data Preprocessing
    * Chronological sorting and aggregation.
    * Pivot transformations.
    * Numerical coercion and cleaning.
    * Linear interpolation for missing observations.
3. Genetic Algorithm
    * Developed a custom GA search process to optimise the temporal window and perform feature selection.
    * The algorithm prioritised data completeness and consistency.
    * Identified 1976–2024 as the selected temporal window.
    * Selected:
        * Butterfly Smoothed Index
        * Butterfly Unsmoothed Index
4. Machine Learning
    * Implemented Support Vector Regression (SVR) using an RBF kernel.
    * Applied feature scaling.
    * Used GridSearchCV for hyperparameter optimisation.
    * Evaluated performance against unseen test data.

📊 Results

The strongest solution combined the Genetic Algorithm with a tuned SVR model.

Metric	Result
R²	0.8974
MAPE	1.98%
Selected period	1976–2024

The model explained a substantial proportion of variation in the held-out data while maintaining a low percentage prediction error.

Actual vs Predicted Values

Residual Analysis

The results suggest that butterfly population indicators may provide useful surrogate information when modelling wild bee population trends.

🛠️ Technologies & Techniques

* Python
* Pandas
* NumPy
* Scikit-learn
* Support Vector Regression (SVR)
* Radial Basis Function (RBF) Kernel
* Genetic Algorithms
* Feature Selection
* GridSearchCV
* Feature Scaling
* Data Cleaning & Transformation
* Matplotlib
* Jupyter Notebook

📁 Repository Structure

uk-pollinator-ai-analysis/
│
├── aai.ipynb
├── data/
├── actual_vs_predicted_comparison.png
├── residual_plot_comparison.png
├── README.md
└── .gitignore

🌱 Future Improvements

Further work could extend the model by incorporating additional ecological drivers, including:

* Pesticide exposure
* Climate variability
* Habitat and land-use change
* Invasive species
* Additional pollinator indicators

The project could also be extended through real-time environmental data integration and Explainable AI (XAI) methods to improve model transparency for environmental decision-making.

⚠️ Limitations

This project is a proof of concept based on historical biodiversity indicators. The relationships identified by the model should not be interpreted as evidence that changes in butterfly populations cause changes in wild bee populations.

Additional ecological and environmental variables would be required to improve the model’s ecological validity and generalisability.

⸻
