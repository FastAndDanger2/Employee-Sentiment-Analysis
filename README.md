# Employee Sentiment Analysis  
Author: Ojas Sarada

This repository contains a complete analysis pipeline to assess employee engagement and sentiment using natural language processing, exploratory data analysis, and statistical modeling. The project was completed as part of an internal evaluation and is intended to demonstrate clarity of thought, reproducibility, and effective communication of insights.

## Project Overview

The goal of this project is to analyze anonymized employee messages to understand sentiment trends, identify individuals at risk of disengagement, and build a model to forecast overall mood shifts. The core objectives are:

- Sentiment labeling: Classify each message as Positive, Negative, or Neutral
- Exploratory data analysis (EDA): Visualize distributions and trends
- Monthly sentiment scoring: Aggregate sentiment per employee per month
- Employee ranking: Highlight top and bottom performers
- Flight risk detection: Flag employees showing signs of disengagement
- Predictive modeling: Use linear regression to explain sentiment scores using behavioral data

---

## Folder Structure

employee-sentiment-analysis/
├── data/ # Raw and processed data files
│ ├── test.csv
│ ├── labeled_test.csv
│ └── flight_risks.csv
├── models/ # Trained model artifacts
│ └── sentiment_trend_model.pkl
├── notebooks/ # Primary analysis notebook
│ └── analysis.ipynb
├── scripts/ # Optional Python utilities
│ └── utils.py
├── visualizations/ # All saved plots and charts
│ ├── sentiment_distribution.png
│ ├── message_length_hist.png
│ ├── sentiment_vs_length.png
│ ├── employee_ranking_table.png
│ └── regression_plot.png
├── .env.example # Environment variable template (optional)
├── README.md # This file
├── report.docx # Formal report with findings
└── requirements.txt # Python package dependencies

## Setup Instructions
To run this project locally:

**Clone the repository**
git clone https://github.com/yourusername/employee-sentiment-analysis.git
cd employee-sentiment-analysis

# Create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate  # macOS/Linux
# OR
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env

# Launch Jupyter and run the notebook
jupyter notebook notebooks/analysis.ipynb


Results Summary
Top 3 Positive Employees (Sample Output):

alice@corp.com
raj@corp.com
john@corp.com

Top 3 Negative Employees (Sample Output):

mike@corp.com
zoe@corp.com
carla@corp.com

Employees Flagged as Flight Risks:

mike@corp.com
deepa@corp.com
carla@corp.com

Model Performance (Linear Regression):

R² Score: 0.72
Mean Squared Error: 3.35

The model indicates that message frequency and average length are meaningful predictors of overall sentiment scores.

Methodology
Sentiment Analysis: VADER sentiment scoring with thresholds for Positive (≥ 0.05), Negative (≤ -0.05), and Neutral (otherwise)

EDA: Histograms, boxplots, and count distributions to uncover patterns

Scoring: Sentiment converted to numeric scores (+1, 0, -1), aggregated monthly

Ranking: Employees sorted by sentiment score per month

Flight Risk: Employees with ≥ 4 negative messages in any 30-day rolling window

Modeling: Linear regression using message count and average length as features

Notes
This project uses only publicly available libraries (NLTK, pandas, matplotlib, seaborn, sklearn).

No external APIs or sensitive data are used.

All results and visuals are reproducible from the provided notebook.

License
This project was completed as part of an internal evaluation. It is not intended for public distribution. Please do not share or reuse without permission.
