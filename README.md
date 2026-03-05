# Micro-Project 1: Campus City Emergency Supply Distribution

## 📋 Problem Summary
This project tackles a real-time supply chain optimization problem for Campus City Logistics. The objective is to design an optimal supply distribution network that minimizes total annual costs while meeting the daily demands of essential campus facilities. 

This is formulated as a Mixed-Integer Linear Programming (MILP) problem. The model makes binary decisions to select optimal warehouses from a list of candidates and continuous decisions regarding the volume of supplies shipped, strictly adhering to the business constraints outlined below.

## 📊 Data Parameters & Constraints

### Transportation Costs (`transportation_costs.csv`)
- **Data Source:** Pre-calculated matrix using actual distances.
- **Cost Range:** $3.68 - $5.03 per unit between selected locations.
- **Calculation:** Based on real geographic coordinates using the Haversine formula.

### Financial Constraints
- **Annual Budget:** $1,500,000.
- **Operational Period:** 365 days (all operational metrics are strictly annualized).
- **Construction Cost:** Amortized over 10 years to calculate the true annual fixed cost.

### Physical & Business Constraints
- **Warehouse Selection:** The network must select exactly 2 warehouses to ensure redundancy.
- **Demand Satisfaction:** Each facility must receive exactly its required annual supply (daily demand × 365).
- **Capacity Limits:** Total shipments from any open warehouse cannot exceed its annual limit (daily capacity × 365).
- **Budget Limit:** The combined annual fixed and transportation costs must be ≤ $1,500,000.
- **Non-negativity:** All shipment quantities must be ≥ 0.

## 📂 Repository Structure
- `/src`: Contains the Jupyter Notebook (`main.ipynb`) with the executable Python source code and the PuLP optimization model.
- `/data`: Contains the necessary CSV datasets used for the problem (`facilities.csv`, `warehouses.csv`, `demands.csv`, `transportation_costs.csv`, and `geographic_bounds.csv`).
- `Report.pdf`: The final technical report containing the mathematical formulation, methodology, and results analysis.

## ⚙️ Dependencies Required
To execute the computational implementation, you need Python installed along with the following libraries:

`pip install pandas pulp matplotlib networkx scipy`
