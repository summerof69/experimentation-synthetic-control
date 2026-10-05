# Synthetic Control and Synthetic DiD: hands-on notebook

Code companion for the blog series on measuring campaign impact with **Synthetic Control (SCM)** and **Synthetic Difference-in-Differences (SDID)**.

All data is simulated or made up. Sales are weekly, in Rs lakh.

## What is in this repo

| File | What it is |
|---|---|
| `scm_sdid_notebook.ipynb` | Main notebook. Run top to bottom to see every number and chart from the posts |
| `scm_sdid_demo.py` | The same methods as a plain Python script |
| `requirements.txt` | Python packages needed |

## Run it

**In Google Colab:** open the notebook from GitHub (Colab: File, Open notebook, GitHub tab), then Runtime, Run all. No installs needed.

**Locally:**

```bash
pip install -r requirements.txt
jupyter notebook scm_sdid_notebook.ipynb
# or run the script
python scm_sdid_demo.py
```

## What the notebook covers

1. The Pune free-delivery example by hand: before vs. after, one control city, Synthetic Control
2. Validation: RMSPE and the RMSPE ratio
3. A 25-donor simulation and the placebo test (p = rank / (donors + 1))
4. Synthetic DiD, including a test city bigger than every donor, where Synthetic Control fails
5. Side-by-side summary of all methods

## Blog series

[Experimentation - Synthetic Control and Synthetic DiD](http://harendrasahu.com/blog/1-synthetic-control-core-idea)

- To be Added

## Use your own data

Replace the simulated data with a table of one column per city and one row per week, put the launch week in `n_pre`, and call `synthetic_control(...)` and `synthetic_did(...)`.

## References

- Abadie, Diamond and Hainmueller (2010), Synthetic Control Methods for Comparative Case Studies
- Arkhangelsky, Athey, Hirshberg, Imbens and Wager (2021), Synthetic Difference-in-Differences
