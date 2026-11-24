# IEEE-IoTJ-2026

Data and demonstration code supporting selected results in Section IV of:

> Jameel Ali, Foivos Ioannis Michelinakis, Giuseppe Caso, Karl-Johan Grinnemo,
> Mohammad Rajiullah, and Tarik Cicic, "Impact of Suboptimal Configurations on
> Energy Efficiency and Latency in Commercial Cellular IoT."

## Contents

- `data/dataset.csv`: Section IV dataset
- `paper_figures_section4.ipynb`: code for generating the included results
- `figures/`: generated figures in PNG and PDF formats
- `tables/`: generated table values
- `validate_release.py`: data validation script

## Data columns

| Column | Unit | Description |
|---|---:|---|
| `record_id` | - | Transaction or episode identifier |
| `campaign_id` | - | Measurement campaign identifier |
| `operator` | - | Anonymised mobile operator |
| `rat` | - | NB-IoT or LTE-M |
| `packet_size_B` | byte | Application payload size |
| `coverage` | - | Normal, Robust, or Extreme coverage |
| `rsrp_dBm` | dBm | Mean RSRP |
| `rtt_s` | s | Round-trip time |
| `connected_duration_s` | s | Connected-state duration |
| `connected_energy_J` | J | Connected-state energy |
| `analysis_scope` | - | Intended analysis scope |

Rows with `analysis_scope = section4_main` are used for the general analysis.
Rows with `analysis_scope = fig9_only` are used only for Fig. 9.

## Generated outputs

Running the notebook generates:

- Table I
- Table II
- Figs. 4-6
- Fig. 8
- Fig. 9

## Run

```bash
pip install -r requirements.txt
python validate_release.py
jupyter notebook paper_figures_section4.ipynb
```

Open the notebook and select **Run All**. Generated files are saved in
`figures/` and `tables/`.

## Citation

Please cite the associated paper. Citation metadata are available in
`CITATION.cff`.
