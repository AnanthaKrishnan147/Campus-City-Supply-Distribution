# Micro-Project 1: Campus City Emergency Supply Distribution

## 📋 Problem Summary
This project tackles a real-time supply chain optimization problem for Campus City Logistics. The objective is to design an optimal supply distribution network that minimizes total annual costs while meeting the daily demands of essential campus facilities. 

This is formulated as a Mixed-Integer Linear Programming (MILP) problem. The model makes binary decisions to select exactly 2 optimal warehouses from a list of candidates and continuous decisions regarding the volume of supplies shipped, all while strictly adhering to capacity limits and a $1,500,000 annual budget.

## 📂 Repository Structure
- `/src`: Contains the Jupyter Notebook (`main.ipynb`) with the executable Python source code and the PuLP optimization model.
- `/data`: Contains the necessary CSV datasets used for the problem (`facilities.csv`, `warehouses.csv`, `demands.csv`, `transportation_costs.csv`, and `geographic_bounds.csv`).
- `Report.pdf`: The final technical report containing the mathematical formulation, methodology, and results analysis.

## ⚙️ Dependencies Required
To execute the computational implementation, you need Python installed along with the following libraries:

```bash
pip install pandas pulp matplotlib networkx scipy