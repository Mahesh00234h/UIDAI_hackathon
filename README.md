# Aadhaar Enrolment & Update Load Forecasting

## Predictive Modeling with Lifecycle-Based Governance Framework

### Overview

This project builds a comprehensive predictive modeling framework to forecast future Aadhaar enrolment and update loads at state and district levels. It aims to identify regions at risk of biometric failure or update backlogs and provide actionable governance insights.

The analysis treats Aadhaar as a three-stage lifecycle:
1.  **Enrolment**: Initial registration.
2.  **Demographic Updates**: Changes in personal data.
3.  **Biometric Updates**: Fingerprint/iris re-enrolment.

By analyzing these stages, the system captures stress patterns, capacity issues, and risks unique to UIDAI operations.

### Key Features

*   **Explainable Predictive Models**: Uses Linear Regression, Random Forest, and Gradient Boosting to forecast loads, ensuring all decisions are traceable to specific features.
*   **Risk Scoring**: Quantifies biometric failure and update backlog risks per region.
*   **Future Demand Forecasts**: Predicts enrolment and update volumes.
*   **Governance Dashboard**: specific metrics for state and district-level planning.
*   **Lifecycle Stress Index**: A composite indicator to identify systemic issues.

### Project Structure

```
├── aadhaar_predictive_analysis.ipynb   # Main Jupyter Notebook containing the analysis code
├── api_data_aadhar_biometric/          # Biometric update data (CSV files)
├── api_data_aadhar_demographic/        # Demographic update data (CSV files)
├── api_data_aadhar_enrolment/          # Enrolment data (CSV files)
├── predictions/                        # Output directory for generated reports and CSVs
│   ├── README.md                       # Analysis results summary
│   ├── QUICK_START.md                  # Executive summary
│   ├── district_predictions_*.csv      # Detailed predictions per district
│   ├── state_governance_dashboard.csv  # State-level aggregated metrics
│   ├── top_50_priority_regions.csv     # Ranked list of high-risk regions
│   └── ...
```

### Getting Started

#### Prerequisites

*   Python 3.12 or higher
*   Jupyter Notebook or JupyterLab

#### Installation

1.  Clone this repository.
2.  Install the required Python packages. You can typically do this with pip:

    ```bash
    pip install pandas numpy scikit-learn statsmodels matplotlib seaborn
    ```

### Usage

1.  Open the `aadhaar_predictive_analysis.ipynb` notebook.
2.  Ensure the data directories (`api_data_aadhar_*`) are present and contain the relevant CSV files.
3.  Run all cells in the notebook.
4.  The script will process the data, train the models, and generate predictions.
5.  Check the `predictions/` directory for the output files.

### Outputs

The analysis generates several CSV files in the `predictions/` folder:

*   **`district_predictions_and_risk_scores.csv`**: Complete predictions and risk scores for all districts.
*   **`state_governance_dashboard.csv`**: Aggregated metrics for state-level decision making.
*   **`top_50_priority_regions.csv`**: Regions ranked by governance priority score, highlighting those needing immediate intervention.
*   **`feature_importance_analysis.csv`**: Ranking of factors driving the predictions.
*   **`model_performance_metrics.csv`**: Technical validation metrics (R², RMSE, etc.).

For a detailed explanation of the methodology and results, please refer to [DOCUMENTATION.md](DOCUMENTATION.md).
