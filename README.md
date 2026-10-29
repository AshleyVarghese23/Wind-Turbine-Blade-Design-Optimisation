# Wind Turbine Blade Design Optimisation

## Overview
This project explores wind turbine blade design optimisation using Python-based numerical modelling, simulation, and optimisation techniques.

## Objectives
- Develop a baseline wind turbine blade model.
- Evaluate aerodynamic performance under defined operating conditions.
- Optimise selected blade design parameters.
- Compare the baseline and optimised designs using quantitative metrics.

## Technology Stack
- Python
- NumPy
- SciPy
- Pandas
- Matplotlib
- Jupyter
- AeroSandbox
- NeuralFoil
- pymoo

## Repository Structure
- `src/`: Python source code
- `notebooks/`: Experiments and analysis
- `results/`: Numerical outputs
- `figures/`: Plots and visualisations

## Project Status
Initial setup complete. Modelling, simulation, and optimisation will be developed incrementally.

### Airfoil Polar Generation

Aerodynamic lift and drag coefficients for the NACA 4412 airfoil were generated using AeroSandbox and NeuralFoil at a Reynolds number of 500,000. The angle of attack was swept from -10° to 20° in 0.25° increments. Lift-to-drag ratio was calculated to identify the angle of maximum predicted aerodynamic efficiency.

The resulting polar data is saved in `results/naca4412_polar.csv`, and the corresponding plots are saved in `figures/naca4412_polars.png`. Linear interpolation is used to retrieve lift and drag coefficients at intermediate angles for subsequent BEM calculations.

**Limitations:** A single Reynolds number is used as a simplifying assumption. Actual Reynolds number varies along a rotating blade because local relative velocity and chord length vary with blade radius. NeuralFoil predictions are model-based estimates and should not be treated as experimental measurements.