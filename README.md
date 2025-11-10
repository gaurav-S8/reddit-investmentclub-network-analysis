# Reddit InvestmentClub — Network Analysis  

Understanding user interaction networks in the r/InvestmentClub subreddit using social graph analysis and centrality metrics.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![NetworkX](https://img.shields.io/badge/Library-NetworkX-purple.svg)
![Pandas](https://img.shields.io/badge/Data-Pandas-blue.svg)
![Graph](https://img.shields.io/badge/Analysis-Network%20Science-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
![Notebook](https://img.shields.io/badge/Jupyter-Notebook-yellow.svg)

## 📘 Overview

This project analyzes community interaction patterns in **r/InvestmentClub**, a Reddit community focused on stock market discussions.  
The aim is to examine how users connect, who influences discussion, and how communication structure reflects group behavior.

We build a **directed interaction network** from Reddit conversations and apply **social network analysis** techniques to reveal communication hubs, community structure, and influence dynamics.

## 🔍 Project Goals

- Extract user interaction graphs from Reddit discussions
- Build a directed network where:
  - **Nodes = Reddit users**
  - **Edges = replies/mentions between users**
- Compute centrality metrics to identify key members:
  - Degree Centrality (engagement)
  - Betweenness Centrality (information brokers)
  - Eigenvector Centrality (influence within clusters)
- Visualize interaction structure and communities
- Draw insights about participation dynamics in investing discussions

## 📂 Project Structure
📦 reddit-investmentclub-network-analysis
├── 📁 Data/ # Processed data used for analysis
├── 📁 zips/ # Raw zipped Reddit dataset
├── 📁 plots/ # Network graphs & visualizations
├── 📄 NetworkAnalysis_InvestmentClub.ipynb # Main Jupyter notebook
├── 📄 Reddit_Data_Analysis_Coursework_Report.pdf
├── 📄 .gitignore
└── 📄 README.md

---

## 🛠️ Methods

### ✅ Data Pipeline
1. Load zipped Reddit data  
2. Extract comments / submissions  
3. Filter invalid users (e.g., `[deleted]`, bots)  
4. Build directed edge list:  
   `User A → User B` if **A replies to B**

### ✅ Network Construction
- Graph Type → **Directed Graph (DiGraph)**
- Tools → pandas, NetworkX, matplotlib
- Basic network stats calculated:
  - Node/edge count
  - Diameter & density
  - Connected components

## 📊 Key Visualizations & What They Show

| Visualization | Insight |
|--------------|--------|
**Full User Interaction Graph (with isolated users)** | ~12.9k users visualized; ~4.6k users are isolated → many users post without interacting.  
**Active Interaction Network (isolates removed)** | Dense core emerges → active users form a tightly connected financial discussion hub.  
**Top-200 Users Network** | Hub-and-spoke structure → a few “super-users” dominate discussion (*Zurevu* is most central).  
**Degree Centrality Ranking** | *Zurevu* has ~17× more connections than next user → extreme influence concentration.  
**LCC Attack Simulation** | Removing ~5% top users collapses connectivity → network is dependent on a small elite core.  
**Rich-Club Coefficient Curve** | High-degree users show selective inter-connection at top range → “elite cluster” behavior.  
**Activity Timeline** | Stable long-term activity with a massive spike during market-event period (weeks 460–470).  
**User Role Identification (Z-Score Analysis)** | ~6.5k help-seekers, ~6.2k help-givers, ~150 hybrid users → subreddit functions as a Q&A support hub.  
**Topic Modeling (LDA)** | Focus on stocks, crypto, market trends, recession risk, and well-known financial figures.

---

## 🧠 Key Findings

- Online finance communities show **power-law participation** (few talk, many listen)
- Network is **super-user driven** — small elite controls information flow
- Removing top users **destroys network cohesion**
- Community acts as a **learning + advice hub** (help-seekers ↔ help-givers)
- Discussion reacts strongly to **market events**
- Topics revolve around **investment strategy, macroeconomics, and key stocks**

---

### 🔍 How to Read the Network Graphs

- **Nodes = users**, **Edges = interactions**
- **Larger nodes** = more central / influential
- **Tighter clusters** = sub-groups around topics/interest areas
- **Isolated dots** = users who ask/post but never interact
- **Bridges** = users who connect multiple communities

---

### 📌 Interpretation Example (Top-200 Network)

- Large central node (*Zurevu*) = dominant discussion hub  
- Few medium-sized nodes = secondary influencers  
- Many small nodes around = regular users replying or seeking advice  
- Structure = **hub-and-spoke**, typical in finance communities where knowledge concentrates

> Result: Community trust and knowledge flow depend on a small “core circle” of influential users.

---

## ▶️ How to Run

1. Open `Code.ipynb`
2. Ensure required libraries are installed:

```bash
pip install pandas networkx matplotlib
```
