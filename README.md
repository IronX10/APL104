Displacement-controlled Loading Analysis
Report and Problem Statement
Report on Analysis of Stress Distribution
Problem Statement
Overview
This project analyzes displacement-controlled loading of materials using data-driven approaches. The workflow involves three main steps:

Polynomial Regression: Generate polynomial equations for displacement components (u_x and u_y) using polynomial.py.
Optimization: Calculate Lamé constants (λ and μ) and minimize the cost function using lameconstant.py.
Stress Visualization: Plot stress variation (σ_xx, σ_yy, σ_xy) for the material using distribution.py.
File Descriptions
polynomial.py

Purpose: Perform polynomial regression on displacement data to model u_x and u_y.
Key Outputs:
Polynomial equations for u_x and u_y.
Prediction vs. Actual plots for displacement components.
lameconstant.py

Purpose: Optimize Lamé constants (λ and μ) based on Navier’s equations and boundary constraints.
Key Outputs:
Optimized Lamé constants.
Cost function value for training and test datasets.
distribution.py

Purpose: Visualize stress variations (σ_xx, σ_yy, σ_xy) across the material.
Key Outputs:
Scatter plots for stress components at various points.
main.py

Purpose: Integrates the workflow for all five datasets in the data/ directory.
Steps:
Call polynomial_obtain to compute u_x and u_y.
Optimize Lamé constants using lame_constants.
Plot stress distributions for each dataset.
How to Run
Ensure Dependencies Are Installed:

pip install -r requirements.txt
Place Data in the data/ Directory:

Each subfolder (e.g., 1, 2, ...) should contain:

displacement_data.csv
reaction_data.csv
Run the Main Script:

python main.py
Outputs
Polynomial Regression:

Equations for u_x and u_y.
Prediction vs. Actual plots.
Lamé Constants Optimization:

Optimized values of λ and μ.
Stress Distribution:

Scatter plots for σ_xx, σ_yy, and σ_xy.
