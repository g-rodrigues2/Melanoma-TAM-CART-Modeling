# Melanoma Dynamics Involving CAR T-cells and tumor-associated macrophages

This notebook contains the analytical computations, numerical simulations, and sensitivity analyses associated with an ordinary differential equation (ODE) model describing the interaction among tumor cells, tumor-associated macrophages (TAMs), and CAR T-cells in cutaneous melanoma.

You can see the codes on this [Repository](https://g-rodrigues2.github.io/Melanoma-Dynamics-Repository/).

The model is used to investigate qualitative and quantitative aspects of the system dynamics, including equilibrium behavior, stability changes, phase portraits, treatment-response profiles, and parameter sensitivity.

These materials were used in my PhD thesis and are also related to the published article "A mathematical model to the melanoma dynamics involving CAR T-cells," published in Computational and Applied Mathematics.

Article link:
https://link.springer.com/article/10.1007/s40314-024-03060-3

## Model overview

The system is composed of three state variables:

- T(t): tumor cell population
- M(t): tumor-associated macrophage population
- C(t): CAR T-cell population

The governing ODE system is based on logistic-type tumor growth, macrophage recruitment/proliferation, and CAR T-cell activation and decay, with additional interaction terms accounting for immunosuppressive and cytotoxic effects.

## Main goals of this notebook

This notebook is intended to:

- reproduce the numerical simulations presented in the study;
- generate the figures associated with equilibrium and stability analyses;
- explore the effects of key parameters on tumor dynamics;
- investigate transition thresholds and qualitative changes in the solutions;
- perform global sensitivity analysis using FAST/eFAST methods.

## Contents

The notebook includes code for:

- simulation of the full T-M-C dynamical system;
- computation of coexistence equilibria and associated thresholds;
- graphical analysis of functions related to existence and stability conditions;
- phase portraits and time-course simulations under different parameter regimes;
- numerical exploration of transition values such as critical parameter thresholds;
- sensitivity analysis at the final time and along time using FAST;
- export of figures and sensitivity outputs for later use.

## Requirements

The notebook uses Python and the following main libraries:

- numpy
- scipy
- matplotlib
- pandas
- sympy
- SALib

Install them with:

pip install numpy scipy matplotlib pandas sympy SALib

## Folder structure

Before running the notebook, it is recommended to create the following directories:

figures/
sensitivity_results/

Generated outputs are typically saved in these folders, including:

- .pdf and .png figure files;
- .csv files with sensitivity indices;
- .npz files containing saved model outputs and time-dependent sensitivity results.

## How to use

Run the notebook sequentially from top to bottom.

A few sections are lightweight and produce figures directly, while others are more computationally expensive, especially:

- dense time integrations;
- parameter sweeps over large grids;
- FAST sensitivity analysis with many samples.

For the sensitivity-analysis sections, it is recommended to run the heavy computation cells only once and save the outputs, then use the plotting cells separately afterward.

## Notes

- Some simulations use very fine temporal grids and may take longer to run.
- Some figure-generation cells assume that the folders figures/ and sensitivity_results/ already exist.
- The notebook is structured to support both analytical interpretation and figure reproduction.
- Parameter values are chosen according to the model formulation and literature-informed or estimated values used in the study.

## Output

The notebook can generate figures such as:

- time profiles of tumor, macrophage, and CAR T-cell populations;
- phase portraits;
- threshold and bifurcation-like diagrams;
- equilibrium classification plots;
- stacked and bar plots for sensitivity indices.

These outputs are suitable for manuscript, thesis, or supplementary-material preparation.

## Reproducibility

To improve reproducibility, the notebook fixes seeds where appropriate in the sensitivity-analysis workflow. Still, execution time may vary depending on the machine and on the numerical tolerances adopted in the ODE solver.

## Author

Guilherme Rodrigues

## Reference

If you use or adapt this notebook, please cite the corresponding thesis chapter, article, or project from which this model was derived.
