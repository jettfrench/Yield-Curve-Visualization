# yield-curve-analysis

notebook to load yield data, plot curves, compute spreads, run simple shocks, and sketch a rough forward ladder

## requirements
- python
- pandas, numpy, matplotlib

## files
- `yield_curve_analysis_plus.ipynb` — main notebook
- `sample_yield_curves.csv` — example data (rates in percent)
- outputs (created when running export cell): `spreads_out.csv`, `forwards_out.csv`

## data format
- csv columns: `date, tenor, years, rate`
  - `date`: ISO date (e.g., 2025-11-01)
  - `tenor`: label (e.g., 3M, 2Y, 10Y)
  - `years`: numeric maturity in years (e.g., 0.25, 2, 10)
  - `rate`: yield in percent (e.g., 4.90)

## usage
- open the notebook and set `CSV_PATH` if needed
- run cells top to bottom
- optional: run the export cell to write `spreads_out.csv` and `forwards_out.csv`

## features
- clean matplotlib plots for each curve date
- spreads: 2s10s and 3m10y (basis points)
- shocks: parallel, steepen, flatten (demo on most recent curve)
- rough 1y forward ladder (toy method, not a full bootstrap)
