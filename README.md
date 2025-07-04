

# Machine Predictive Maintenance

A data-driven framework for forecasting machine failures using Random Forest classifiers. This project walks through data preprocessing, exploratory analysis, model training, hyperparameter tuning, and deployment-ready prediction scripts, along with accompanying Power BI dashboards and a formal project report.

---

## Repository Structure

```
machine-predictive-maintenance/
├── data/                  # Raw and processed datasets
│   ├── predictive_maintenance/          # Original Kaggle CSVs
│   └── predictive_maintenance1/         # Cleaned and feature-engineered data
│
├── notebook/              # Jupyter notebooks
│   └── Machine Predictive Maintenance Classification.ipynb
│
├── reports/               # PDF and Markdown reports
│   ├── IEEE Format DS Final Report.pdf
│   └── Machine Predictive Maintenance Classification Report.pdf
│
├── power_bi/              # Power BI dashboard files
│   └── final.pbix
│
├── requirements.txt       # Python dependencies
├── README.md              # This file
└── .gitignore             # Files and folders to ignore
```

---

## Overview

Industrial downtime is costly. By analyzing sensor readings—air and process temperature, rotational speed, torque, and tool wear—this project trains a Random Forest model to:

1. **Classify** whether a machine will fail (`Target` = 0/1).
2. **Predict** failure type (e.g. Heat Dissipation, Tool Wear, Overstrain).

Key steps include data cleaning, visualization (histograms, heatmaps, boxplots, violin and bubble charts), model training & evaluation (accuracy, precision, recall, F1-score), feature-importance analysis, and hyperparameter tuning with `GridSearchCV`.

---

##  Getting Started

### Prerequisites

* Python 3.8+
* pip

### Installation

1. **Clone the repo**

   ```bash
   git clone https://github.com/your-username/machine-predictive-maintenance.git
   cd machine-predictive-maintenance
   ```

2. **Create & activate a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate    # Linux/macOS
   venv\Scripts\activate       # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

1. **Prepare the data**

   * Place original Kaggle CSV(s) in `data/predictive_maintenance/`.
   * Run the preprocessing cells in the Jupyter notebook to generate `data/predictive_maintenance1/`.

2. **Explore & visualize**

   * Open `notebook/Machine Predictive Maintenance Classification.ipynb`.
   * Execute cells to reproduce EDA plots (histograms, pie charts, heatmaps, box & violin plots, bubble charts).

3. **Train & evaluate the model**

   * Run the model training section to fit a `RandomForestClassifier`.
   * View evaluation metrics and feature importances.

4. **Hyperparameter tuning**

   * Use the `GridSearchCV` section in the notebook to find the best `n_estimators` and `max_depth`.

5. **Predict on new data**

   * Modify the example in “Predictive Analysis” to input your own sensor readings.
   * The notebook outputs predicted failure label and probability for each failure type.

6. **Power BI Dashboards**

   * Open the `final.pbix` files in `power_bi/` to interactively explore key metrics and feature contributions.

7. **Read the formal report**

   * Detailed methodology, literature review, and conclusions are in `reports/`.

---

## Folder Details

* **data/raw**: Original Kaggle dataset
* **data/processed**: Cleaned, with nulls removed, categorical encoding, train/test splits
* **notebook**: All analysis, modeling and visualization code
* **reports**:

  * IEEE-formatted final report
  * Project report with executive summary and appendices
* **power\_bi**: Interactive dashboards for non-technical stakeholders

---

##  Contributing

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m "Add X feature"`)
4. Push to your branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

---

##  Author

* **Hammad Anwar**
