# ForecastPowerBench

**Benchmarking Performance, Energy, and Scaling Behavior of Time-Series Foundation Model Inference**

Forecasting accuracy alone does not determine whether a time-series foundation model (TSFM) is suitable for deployment. ForecastPowerBench is a workload-aware benchmark that measures how **context length**, **forecast horizon**, and **batch size** affect TSFM **throughput**, **memory**, **power**, and **Energy per Forecast (EPF)** across hardware platforms. It combines these measurements with GIFT-Eval accuracy scores to study accuracy–efficiency trade-offs.

- **Models:** 10 TSFMs: Chronos-2, FlowState, Kairos, Moirai-2, Sundial, TempoPFN, TiRex, TimesFM 2.5, Toto, TTM-R3
- **Hardware:** NVIDIA H100, RTX 5090, RTX A6000, Jetson AGX Orin
- **Workloads:** 7 context lengths × 9 forecast horizons, plus batch sizes from 1 to 4,096

**Code:** <https://anonymous.4open.science/r/ForecastPowerbench-C810>

## This repository

This repository is the project website: an interactive results explorer, an efficiency map, and the paper's figures.

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

Measurement data is stored in `data/results/`, and every file must be listed in `data/results-index.json`. See [`JSON_DATA_LAYOUT.md`](JSON_DATA_LAYOUT.md) for the schema.
