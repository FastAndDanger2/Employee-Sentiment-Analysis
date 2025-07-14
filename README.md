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
