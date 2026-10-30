# Multi-Class Cyber Attack Classification

This project implements a multi-class machine learning model in Python to classify different types of network cyber attacks (`attack_type`) based on traffic features and behavioral statistics.

## Dataset
- **File:** `7-cyber_attack_data.csv`[cite: 2]
- **Features:** Packet rates, payload sizes, connection durations, TCP flag counts, interarrival times, failed login attempts, unusual port activity scores, session entropy, and response delays[cite: 2].
- **Target Variable:** `attack_type` (Multi-class classification: 0, 1, and 2)[cite: 2].

## Workflow & Methodology
1. **Data Preprocessing:** Loaded the dataset using `pandas`, checked data structures, missing values, and descriptive statistics[cite: 2].
2. **Train-Test Split:** Split the dataset into training and testing sets (70% train, 30% test) using stratified/random sampling[cite: 2].
3. **Baseline Model:** Trained a multi-class **Logistic Regression** model and assessed performance via accuracy, classification reports, and confusion matrices[cite: 2].
4. **Hyperparameter Tuning:** Optimized model performance using **GridSearchCV** combined with `StratifiedKFold` cross-validation across various solvers, penalties, and regularization strengths (`C`)[cite: 2].
5. **Multi-Class Strategies:** Explored advanced classification techniques including **One-vs-One (OvO)** and **One-vs-Rest (OvR)** classifiers to compare multi-class handling[cite: 2].

## Technologies & Libraries Used
- **Python**[cite: 2]
- **Pandas & NumPy** (Data processing and matrix operations)[cite: 2]
- **Matplotlib & Seaborn** (Data visualization)[cite: 2]
- **Scikit-Learn** (Classification models, metrics, GridSearchCV, and OvO/OvR wrappers)[cite: 2]

## Results
- The baseline and tuned Logistic Regression models achieved an accuracy of ~**79%**, while the One-vs-One strategy yielded approximately **80%** accuracy on the test dataset[cite: 2].
