# Numerical Computations — Practical Assignments (Fall 2024)

<div align="center">
  <img src="https://cdn.freebiesupply.com/logos/large/2x/sharif-logo-png-transparent.png" alt="Sharif Logo" width="110" height="110"><br/>
  <b>Computer Engineering Department</b> • <b>Numerical Computations</b>
</div>

This repo contains **three Jupyter notebooks** implementing core numerical methods **from scratch** with clear plots and brief analysis.

## Files
- `NC_Practical1.ipynb` — Taylor series, Newton interpolation (vectorized + Horner), cubic splines (natural & clamped)
- `NC_Practical2.ipynb` — ODE IVP solvers: Euler, Heun, Backward Euler, RK4, Adams–Bashforth(2)
- `NC_Practical3.ipynb` — RK4 for a 3D system + Newton–Raphson for a nonlinear system

## Setup
Tested on **Python 3.10+**.
```bash
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -U pip numpy matplotlib sympy jupyterlab
jupyter lab  # or: jupyter notebook
```

## Practical Summaries
### Practical 1 — Approximation & Interpolation
- Taylor expansion for \(f(x)=e^{-x}\sin(5x)\) with tolerance-based convergence.
- Newton interpolation using **vectorized divided differences** and **Horner** evaluation; runtime vs. nodes.
- Cubic splines with **natural/clamped** boundaries; endpoint behavior comparison.

### Practical 2 — ODE Initial-Value Problems
- Compare Euler, Heun, Backward Euler, RK4, AB(2) on \(y'=-2y\), \(y(0)=1\), \(x\in[0,5]\).
- Single overlay plot to contrast accuracy, stability, and cost.

### Practical 3 — Multi‑Dimensional ODEs & Nonlinear Solve
- RK4 for \((x,y,z)\) with several \((\text{max\_iter}, h)\) settings → time‑series of \(x(t),y(t),z(t)\).
- Newton–Raphson on
  \(\{x^2+y^2-4=0,\ e^x+y-1=0\}\) with iteration traces for different initial guesses.

## Reproducibility
Only `numpy`, `matplotlib`, and (in Practical 1) `sympy` for symbolic derivatives. Results are deterministic.

## License
Pick any license (e.g., MIT).

---
**Quick start**
```bash
pip install -U numpy matplotlib sympy jupyterlab
jupyter lab
```
