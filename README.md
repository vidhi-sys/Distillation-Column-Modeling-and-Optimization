# Distillation-Column-Modeling-and-Optimization
This project focuses on modeling and optimizing a distillation column process using machine learning techniques. The goal is to predict key output variables—distillate purity (xD) and reboiler duty (QR)—based on input operating conditions

<img width="3570" height="1466" alt="parity_plots" src="https://github.com/user-attachments/assets/6b3f1f90-e7c8-4103-9757-3589d55790c8" />

🎯 Objectives
Develop accurate surrogate models for predicting distillate purity (xD) and reboiler duty (QR)

Compare multiple machine learning algorithms

Identify optimal operating conditions for distillation columns

Provide a comprehensive analysis framework for distillation optimization

📁 Project Structure
'''
AI_Distillation_Surrogate_Model/
├── final_code.py              # Main implementation script
├── requirements.txt           # Python dependencies
├── README.md                  # This file
└── AI_Distillation_Surrogate_Results/
    ├── distill_data.csv       # Generated dataset
    ├── data_columns.txt       # Dataset description
    ├── best_hyperparameters.json  # Optimized model parameters
    ├── validation_results.csv # Validation performance metrics
    ├── test_results.csv       # Test performance metrics
    ├── results_summary.csv    # Summary of results
    ├── optimization_results.csv # Optimal operating conditions
    ├── input_output_relationships.png  # Effect of R on outputs
    ├── correlation_heatmap.png         # Correlation matrix
    ├── parity_plots.png       # Actual vs predicted values
    ├── residual_distributions.png     # Error distributions
    └── taylor_diagrams.png    # Taylor diagrams for model evaluation
    '''
🛠️ Installation & Setup
Prerequisites
Python 3.8+

pip package manager

Installation
Clone or download the project files

Install required dependencies:

bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
🚀 Usage
Execute the main script to run the complete analysis:

bash
python final_code.py
The script will:

Generate synthetic distillation data

Train and evaluate multiple ML models

Create visualizations and performance metrics

Identify optimal operating conditions

Save all results to the output directory

📊 Input Parameters
Parameter	Range	Description
Reflux Ratio (R)	0.8-5.2	Ratio of liquid returned to column
Feed Composition (xF)	0.2-0.95	Ethanol mole fraction in feed
Feed Flow Rate (F)	70-130 kmol/h	Input flow rate
Number of Stages (N)	20	Theoretical separation stages
🎯 Output Targets
Target	Range	Description
Distillate Purity (xD)	0.2-0.956	Ethanol purity in distillate
Reboiler Duty (QR)	200-1800 kW	Energy consumption in reboiler
🤖 Machine Learning Models
Polynomial Regression: Baseline model with polynomial features

XGBoost: Advanced gradient boosting algorithm

Bagging Regressor: Ensemble method with multiple estimators

📈 Performance Summary
Best Model (XGBoost) Performance:
Distillate purity prediction: R² = 0.968, RMSE = 0.009

Reboiler duty prediction: R² = 0.842, RMSE = 62.3 kW

Validation Performance:
Model	xD R²	QR R²	xD RMSE	QR RMSE
Polynomial	0.892	0.956	0.018	45.2
XGBoost	0.973	0.865	0.008	58.1
Bagging	0.961	0.854	0.009	59.8
🔍 Optimization Results
Identified optimal configurations for different purity targets:

R	xF	F	xD	QR (kW)
2.5	0.70	100	0.88	780.0
3.2	0.75	100	0.91	950.0
4.0	0.80	100	0.93	1150.0
5.0	0.85	100	0.95	1400.0
6.0	0.90	100	0.96	1650.0
⏱️ Expected Runtime
Initial execution: 2-3 minutes

Complete analysis: 5-7 minutes

Output: 15+ files including data, plots, and results

✅ Verification
Successful execution is confirmed by:

Terminal message: "ANALYSIS COMPLETE"

AI_Distillation_Surrogate_Results folder creation

Complete set of output files (CSV, PNG, JSON)

📚 References
Chen, T., & Guestrin, C. (2016). XGBoost: A scalable tree boosting system

Scikit-learn: Machine Learning in Python, Pedregosa et al., JMLR 12, pp. 2825-2830, 2011

Geron, A. (2019). Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow

👨‍💻 Author
Vidhi Udasi
VIT Bhopal University, Batch: 2023
Autumn Internship Candidate

📄 License
This project is created for educational and research purposes as part of a screening task for an AI/ML internship position.



