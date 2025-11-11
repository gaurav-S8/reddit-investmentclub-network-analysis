# Reddit InvestmentClub — Social Network Analysis

Analyzing user interaction patterns and influence dynamics within the **r/InvestmentClub** subreddit.  
This project focuses on **network science and time-series engagement patterns** to understand community behavior and influence structure. A brief topic analysis is included to highlight major conversation themes.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![NetworkX](https://img.shields.io/badge/Library-NetworkX-purple.svg)
![Pandas](https://img.shields.io/badge/Data-Pandas-blue.svg)
![Graph](https://img.shields.io/badge/Analysis-Network%20Science-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
![Notebook](https://img.shields.io/badge/Jupyter-Notebook-yellow.svg)


## Key Highlights

- Built a **directed interaction network** (~12.9K users, 14K+ edges, 10-year data)
- Identified **super-influencers** driving most discussions (power-law behavior)
- Removing the top ~5% users **collapses connectivity** → leadership-dependent network
- Classified **help-seekers vs help-givers vs hybrid users**
- Performed **LDA topic modeling** to uncover investment conversation themes
- Analyzed **temporal posting patterns** & activity spikes aligned with market events

> Result: The community behaves like a **Q&A financial hub** with a small core of dominant contributors who shape discussions and information flow.

## Objectives
- Map user-to-user communication flows
- Identify key influencers and structural hubs
- Measure network robustness & elite clustering behavior
- Understand community behavior over time
- Extract dominant topics driving discussions

## Methodology

| Step | Techniques |
|------|-----------|
Data Collection | Reddit JSON, Pandas preprocessing  
Network Construction | Directed DiGraph (NetworkX)  
Centrality Analysis | Degree, Eigenvector, Betweenness  
Community Structure | Rich-club, Core-periphery behavior  
Robustness Test | Largest Connected Component (node removal)  
User Role Analysis | Activity Z-Score (help-giver vs seeker)  
Topic Modeling | LDA on high-engagement submissions  
Visualization | Matplotlib, NetworkX layouts  

## Key Findings

| Insight | Summary |
|--------|--------|
Influence Concentration | Small elite group dominates conversations (power-law)  
Network Fragility | Top users removal → rapid collapse in connectivity  
User Roles | ~50% help-seekers, ~50% help-givers, ~150 hybrid roles  
Market Sensitivity | Activity spikes around major financial events  
Topic Themes | Stocks, macroeconomics, crypto, EVs, recession fear

## Repository Structure
<pre>
📦 reddit-investmentclub-network-analysis
├── Data/ # Processed data
├── zips/ # Raw JSON data
├── plots/ # Network visualizations
├── NetworkAnalysis_InvestmentClub.ipynb
├── Reddit_Data_Analysis_Coursework_Report.pdf
└── README.md
</pre>

## Tech Stack

| Category | Tools |
|---|---|
Language | Python 3.10+  
Libraries | Pandas, NetworkX, Matplotlib, Scikit-Learn  
Environment | Jupyter Notebook  

## How to Run

```bash
git clone https://github.com/gaurav-S8/reddit-investmentclub-network-analysis.git
cd reddit-investmentclub-network-analysis
pip install -r requirements.txt
jupyter notebook NetworkAnalysis_InvestmentClub.ipynb
