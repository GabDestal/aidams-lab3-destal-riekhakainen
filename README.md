# aidams-lab3-destal-riekhakainen

Lab 3: bottom-up steel emissions for China with uncertainty quantification (bootstrap, Monte Carlo simulation, scenarios).

- `lab3.ipynb`: the completed notebook, already run with all outputs visible
- `data/Plant-level_data_Global_Iron_and_Steel_Tracker_June_2026_V1.xlsx`: Global Energy Monitor, Global Iron and Steel Tracker (June 2026 release, CC BY 4.0)

## Run the notebook

Use Python 3.10 or newer. From the repository folder, install the dependencies:

```
pip install pandas numpy scipy matplotlib openpyxl jupyterlab
```

Then start Jupyter and run everything from the top:

```
jupyter lab lab3.ipynb
```

In Jupyter, use **Kernel → Restart Kernel and Run All Cells**. A full run takes about a minute. Random draws use fixed seeds, so the results match the saved outputs.

## Data

The setup cell reads the workbook from `data/`. To use another copy or release of the tracker, set the `GIST_PATH` environment variable to its path before starting Jupyter:

```
# PowerShell
$env:GIST_PATH = "C:\path\to\Plant-level-data-Global-Iron-and-Steel-Tracker-September-2025-V1.xlsx"
# bash
export GIST_PATH=/path/to/Plant-level-data-Global-Iron-and-Steel-Tracker-September-2025-V1.xlsx
```

The lab was written for the September 2025 release; this repository uses the June 2026 release, whose column names (`GEM plant ID`, `Country/area`, `Parent (English)`) are mapped back to the lab's names in the setup cell. Numbers therefore differ slightly from those quoted in the lab text.
