# project_code
code for the project
## Project overview

This project studies how an Ant Colony Programming (ACP) approach can be used to approximate solutions of scalar ordinary differential equations (ODEs), and compares its performance with standard numerical solvers.

The comparison is carried out using a shared residual-based evaluation protocol. Across the experiments, ACP, Forward Euler, and classical fourth-order Runge–Kutta (RK4) are evaluated on a common grid using the same midpoint residual metric.

## Main components

The code in this repository includes:

- an ACP-style symbolic search method for scalar ODE residual minimisation,
- numerical baseline solvers including Euler and RK4,
- routines for computing the shared residual-based accuracy metric,
- experiment scripts for the four case studies discussed in the dissertation,
- plotting utilities for reproducing the figures.

## Experiments

The dissertation considers four scalar initial value problems:

1. **Closed-form separable ODE**
   - \( y'(t) = (1-y(t))^2, \; y(0)=0 \)
   - exact solution available for reference.

2. **Nonlinear ODE without closed-form reference**
   - \( y'(t) = t - y(t)^3, \; y(0)=0 \)

3. **Oscillatory / rapidly varying ODE**
   - \( y'(t) = \sin(10t) - y(t)^3, \; y(0)=0 \)

4. **Application-motivated second-order reaction kinetics**
   - \( y'(t) = -y(t)^2, \; y(0)=1 \)
   - exact solution available for reference.

