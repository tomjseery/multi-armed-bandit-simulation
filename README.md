# Multi-Armed Bandit Simulation

A Jupyter notebook that models a stationary ten-armed bandit and compares online action-selection strategies over repeated experiments. Each simulated arcade machine returns normally distributed rewards around a hidden true value, leaving the agent to balance exploration and exploitation.

## Implemented experiment

- Ten arms with fixed expected rewards
- Incremental action-value estimates
- Epsilon-greedy agents with `ε = 0`, `0.01` and `0.1`
- Upper Confidence Bound (UCB) selection with `c = 2`
- 500 episodes of 1,000 steps per agent
- Per-arm reward histories and per-step reward logs
- Violin plots and average-reward comparisons
- Reporting of each agent's estimated best action

The notebook also contains early scaffolding for optimistic-initial-value and gradient-bandit agents. Those classes are unfinished and are not part of the executed comparison.

## Requirements

- Python 3
- Jupyter Notebook or JupyterLab
- NumPy
- PyTorch
- Matplotlib
- Seaborn

One way to create an isolated environment is:

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyter numpy torch matplotlib seaborn
jupyter notebook N_Armed_Bandit_Problem_Arcade_Machine.ipynb
```

Run the notebook from top to bottom to construct the environment, execute every agent and regenerate the visualisations. No random seed is fixed, so exact reward curves vary between runs.

## Structure

The project is intentionally notebook-based: the environment, agents, experiment loop, plots and recorded outputs are all contained in `N_Armed_Bandit_Problem_Arcade_Machine.ipynb`.

## Status

This is an exploratory reinforcement-learning exercise, not a packaged library. The epsilon-greedy and UCB paths form the completed experiment; the additional agent classes are retained as future-work scaffolding.
