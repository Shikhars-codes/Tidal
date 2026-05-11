# TidalSense Study — Analysis

Analysis of a 30-day clinical study of the N-Tidal breathing-test handset
across 10 GP practices, 20 handsets and 25 administrators (~8.7k tests).

## Contents

```
data/raw/        software_table.csv, hardware_telemetry_table.csv
notebooks/
  EDA.ipynb        data quality and exploratory plots
  analysis.ipynb   operational report for clinical / product leadership
README.md
requirements.txt
```

## Setup

```bash
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/EDA.ipynb` first, then `notebooks/analysis.ipynb`. Both
notebooks are self-contained — helper functions are defined in the first
cell. Charts use Plotly.

## What's in each notebook

- **`EDA.ipynb`** — schema, missing-value check, daily/weekday/hourly volume,
  outcome and error distributions, per-handset error ranking, per-handset
  telemetry, firmware rollout timeline, boot-frequency comparison, correlation
  matrix.
- **`analysis.ipynb`** — the deliverable. Executive summary, headline KPIs,
  daily activity, per-practice performance, then **9 findings** each in
  *what we found → likely cause → recommended action* format with supporting
  charts, plus a prioritised recommendation table for management.
