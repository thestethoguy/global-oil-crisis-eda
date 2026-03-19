# 🛢️ Global Economic Impact Analysis: 2026 Oil Crisis

**Author:** Aman Aaryan
**Degree:** B.Tech in Information Technology

## 📋 Project Overview
This project involves a comprehensive Exploratory Data Analysis (EDA) and predictive modeling pipeline to assess the macroeconomic shockwaves caused by the 2026 geopolitical conflict and the subsequent closure of the Strait of Hormuz. The analysis investigates the vulnerability of global supply chains and the resulting domestic inflation risks.

## 🏗️ Data Science Pipeline Architecture

```mermaid
flowchart TD
    %% Custom Styling
    classDef dataset fill:#e1f5fe,stroke:#01579b,stroke-width:2px,color:#000
    classDef processing fill:#fff3e0,stroke:#e65100,stroke-width:2px,color:#000
    classDef modeling fill:#f3e5f5,stroke:#4a148c,stroke-width:2px,color:#000
    classDef insight fill:#e8f5e9,stroke:#1b5e20,stroke-width:2px,color:#000

    %% Pipeline Nodes
    subgraph Data [1. Data Ingestion]
        A[(crude_oil_daily.csv)]:::dataset
        B[(country_impact.csv)]:::dataset
        C[(petrol_prices_comparison.csv)]:::dataset
    end

    subgraph Preprocessing [2. Preprocessing & Engineering]
        D[Handle Missing Values]:::processing
        E[DateTime Parsing]:::processing
        F[Relational Merging 'JOIN']:::processing
    end

    subgraph Analysis [3. Exploratory Data Analysis]
        G{Time-Series Volatility}:::processing
        H{Bivariate Scatter Mapping}:::processing
    end

    subgraph ML [4. Predictive Modeling]
        I((Linear Regression)):::modeling
        J((Logistic Regression)):::modeling
        K[Predict: GDP Impact %]:::modeling
        L[Classify: Risk Tiers]:::modeling
    end

    subgraph Output [5. Executive Deliverables]
        M[Jupyter Notebook]:::insight
        N[Exported PDF / HTML]:::insight
        O(((Final Business Insights))):::insight
    end

    %% Routing
    A & B & C --> D
    D --> E --> F
    F --> G & H
    G & H --> I & J
    I --> K
    J --> L
    K & L --> M & N --> O



## 🛠️ Tech Stack & Methodologies
* **Language:** Python 3
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
* **Methodologies:**
  * Data Cleaning & DateTime preprocessing for time-series evaluation.
  * Relational Data Merging to map domestic fuel surges against stock market declines.
  * **Linear Regression:** Predicting continuous GDP percentage impacts based on import dependency metrics (evaluated via RMSE and R-Squared).
  * **Logistic Regression:** Classifying categorical inflation risk tiers (evaluated via Precision, Recall, and Confusion Matrices).

## 🚀 Key Insights
1. Identified a massive structural break in global Brent and WTI crude benchmarks aligning exactly with the conflict escalation timeline.
2. Demonstrated mathematically that South Asian nations with high oil import dependencies suffered the sharpest GDP contractions.
3. Proven strong inverse correlation between sudden domestic fuel price hikes and national stock market stability.

## 📂 File Structure
* `EDA_Project.ipynb`: The main Jupyter Notebook containing all chronological code, visualizations, and markdown explanations.
* `EDA_Project.pdf`: A clean, exported document of the final analysis for easy reading.
* `*.csv`: The underlying datasets utilized for the analysis.
