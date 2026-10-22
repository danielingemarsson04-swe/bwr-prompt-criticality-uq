# Assignment 2: Prompt criticality – how uncertain is the answer?

**Author:** <Your name>

**Program function:** Simulates a BWR control rod drop to prompt criticality (first second after the event) and quantifies the uncertainty of peak power and maximum fuel temperature rise, using (1) one-parameter-at-a-time sensitivity analysis and (2) Monte Carlo sampling of all parameters at once.

## File content

- `README.md` – What it does, how to run it and where to find results
- `main.py` – The program you run (Task 1, Task 2 and plots)
- `reactor_model.py` – The physics model (power, k, void and fuel temperature as functions of time)
- `CODE_DOCUMENTATION.md` – Assumptions, data sources (steam tables at 70 bar), equations
- `requirements.txt` – Python packages used
- `report/` – Final report (PDF) including code appendix and self-evaluation
- `figures/`, `results/` – Output from the simulation

## How to run

1. Open the folder containing `main.py` and `reactor_model.py`
2. Install the required libraries: `pip install -r requirements.txt`
3. Run `python main.py`

## Results

Results from the simulation are saved in `results/` and `figures/`:

- **Nominal case:** time curves of power, multiplication factor, void and fuel temperature, together with Pmax and ΔTmax
- **Task 1:** table and bar chart of the change (%) in Pmax and ΔTmax for each of the five parameters (±1σ), a ranking of the parameters, and the total uncertainty combined in quadrature
- **Task 2:** at least 500 Monte Carlo runs with uncertainty bands (68 % and 95 %) for all time curves, histograms of Pmax and ΔTmax with summary statistics, and a convergence plot of the mean and standard deviation of Pmax versus number of runs
- **Task 3:** comparison of the two methods, and discussion of linearity and parameter independence

## Uncertain parameters

| Parameter | Nominal value | Uncertainty (1σ) |
| --- | --- | --- |
| Excess reactivity ρ | 2000 pcm | 15 % |
| Prompt neutron lifetime l | 1.0×10⁻⁴ s | 15 % |
| Fuel temperature coefficient ∂k/∂Tf | −4 pcm/K | 15 % |
| Void coefficient ∂k/∂α | −100 pcm/% void | 20 % |
| Heat transfer coefficient Uw | 14.3 W/(cm·K) | 25 % |

## Notes

<Known limitations, simplifications or things you did not have time to finish.>
