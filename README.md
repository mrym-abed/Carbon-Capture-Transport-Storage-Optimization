# Carbon Capture, Transport and Storage – Optimization

**Optimization of Complex Decisions**  
CentraleSupélec – Université Paris-Saclay  
Academic Year: 2026–2027

## 1. Project Overview

This academic group project investigates the optimal deployment of a Carbon Capture, Transport and Storage (CCTS) infrastructure over a 25-year planning horizon.

The objective is to minimize the total infrastructure and transportation costs while satisfying progressively tightening CO₂ emissions constraints.

The problem is formulated as a **Mixed-Integer Linear Programming (MILP)** model and solved using mathematical optimization techniques.

## 2. Problem Description

The optimization problem considers:

- CO₂ capture installations at industrial emission sites
- Transportation through trucks, railways, and pipelines
- Pipeline construction decisions and capacity planning
- Availability of CO₂ storage facilities
- Network flow conservation
- Annual CO₂ emissions reduction requirements

The optimization jointly determines infrastructure investment decisions, transportation flows, and deployment timing.

## 3. Mathematical Formulation

The project uses a Mixed-Integer Linear Programming (MILP) formulation.

The objective function minimizes total costs, including:

- Transportation operating costs
- Annualized pipeline investment costs

The mathematical model includes constraints related to:

- Capture installation decisions
- CO₂ flow conservation
- Pipeline construction and capacity
- Storage availability
- Transportation network restrictions
- Annual emissions limits

## 4. Implementation and Optimization

The computational implementation was developed in Python using mathematical optimization tools, including Gurobi.

Three problem instances were investigated:

- Small instance
- Medium instance
- Large instance

The baseline experiments use a 25-year planning horizon, a 90% capture efficiency, and an assumed 50% reduction in annual net emissions by the final year.

The 50% target is a modeling assumption, not a value explicitly provided in the input instance files.

## 5. Project Structure and Methodology

The project consists of four main components.

**Q1 – Mathematical Modeling**

Development of the MILP formulation, including decision variables, objective function, and constraints.

**Q2 – Computational Implementation and Numerical Optimization**

Implementation and numerical solution of the MILP model for the Small, Medium, and Large instances.

The computational analysis includes feasibility verification, optimization performance, solution costs, and optimality gaps.

**Q3 – Sensitivity Analysis**

Investigation of how pipeline investment costs and storage-site availability affect infrastructure decisions and total costs.

**Q4 – Cost–Emissions Trade-off Analysis**

Exploration of the trade-off between infrastructure costs and CO₂ emissions reductions using different emissions targets.

## 6. Computational Results

The baseline numerical experiments produced the following results:

| Instance | Reported Cost (Model Units) | Optimality Status |
|---|---:|---|
| Small | 18,405.35 | Globally optimal |
| Medium | 616,447.62 | Feasible solution |
| Large | 685,530.97 | Feasible solution after LP polishing |

The Small instance was solved to global optimality within numerical tolerances.

For the Medium and Large instances, the solver returned feasible solutions within the computational time limits, but global optimality was not established.

## 7. Sensitivity and Trade-off Analysis

Sensitivity experiments investigated the influence of:

- Pipeline distance-dependent investment charges
- Storage-site opening dates
- Emissions reduction targets

The results demonstrate how infrastructure costs, transportation technologies, and deployment decisions depend on the underlying economic and environmental assumptions.

For larger instances, the reported cost–emissions trade-offs are based on feasible computational solutions and should not be interpreted as globally certified Pareto-optimal results.

## 8. My Contributions

This project was completed as part of a university group assignment.

My primary contribution was the **Python coding and computational implementation of Question 2 (Q2)**, focusing on the numerical optimization of the baseline MILP model for the three problem instances.

My work focused on translating the optimization formulation into a computational workflow and obtaining numerical solutions using optimization software.

The complete project also incorporates the other components developed through the group's collaborative work.

## 9. Project Files

The repository includes:

- `CCTS_Final_Report.pdf` – Final technical report covering the mathematical formulation, experiments, results, and conclusions.
- `CCTS_Q1_Q4_Final Code Notebook.zip` – Complete Jupyter Notebook implementation and the three input instance files.

The notebook contains the Q1–Q4 computational workflow and saved numerical outputs.

## 10. Requirements and Execution

**Programming language:** Python

**Main tools and libraries:**
- Gurobi (`gurobipy`)
- NumPy
- Pandas
- SciPy
- Matplotlib
- Jupyter Notebook / IPython

To reproduce the computational experiments:

1. Download and extract the project ZIP archive.
2. Keep the three input instance files in the `data/` directory alongside the notebook.
3. Open `CCTS_Q1_Q4_Experiments.ipynb` in a compatible Jupyter environment.
4. Install the required Python packages and configure a suitable Gurobi license.
5. Review the `RUN_Q2`, `RUN_Q3`, and `RUN_Q4` execution switches.
6. Execute the relevant notebook cells in order.

The full experiments can be computationally demanding. Their outputs are saved in the provided notebook for inspection.

## 11. Academic Context

**Course:** Optimization of Complex Decisions  
**Project type:** Academic Group Project  
**Academic year:** 2026–2027
