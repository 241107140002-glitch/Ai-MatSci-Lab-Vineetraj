# AI in Material Science — Module 1

This repository contains the Jupyter notebooks for **Module 1** of the *AI in Material Science* course. The module introduces the core Python data-science stack (pandas, NumPy, Matplotlib, Seaborn) applied to materials data, and takes the first steps toward connecting to the Materials Project API.

## Contents

| Notebook | Topic | Description |
|---|---|---|
| `Module_1_S01.ipynb` | Intro to pandas | Builds a small dictionary of material properties (Fe, Al, Ti — atomic number, density, melting point, crystal structure, bandgap), converts it into a pandas DataFrame, and explores it with `.head()`, `.info()`, `.dtypes`, `.shape`, and `.describe()`. |
| `Module_1_S02.ipynb` | Intro to Matplotlib | Heavily commented walkthrough of `matplotlib.pyplot`, plotting **bandgap energy vs. atomic number** for Group 14 elements (C, Si, Ge, Sn, Pb) with labeled points, custom styling, and a grid. |
| `Module_1_S03.ipynb` | HW1 — Quiz + Plotting | Answers a conceptual quiz question (Python list vs. NumPy array) and plots **density vs. atomic number** for Period 4 transition metals (Ti, V, Cr, Mn, Fe) as a line chart. |
| `Module_1_S04.ipynb` | HW1 — Option 2 | Bar chart comparing **thermal conductivity** of common engineering metals (Al, Cu, Ag, Au). |
| `Module_1_S05.ipynb` | Multi-material dataset | Constructs a 15-entry dataset spanning three material classes (Metal, Ceramic, Polymer) across 8 properties (density, elastic modulus, bandgap, thermal conductivity, melting temperature, cost) and demonstrates filtering the DataFrame by class. |
| `Module_1_S06.ipynb` | Data preprocessing | Covers unit conversion (Kelvin → Celsius), one-hot encoding of the `Class` column with `pd.get_dummies`, and a custom function to filter materials by density. |
| `Module_1_S07.ipynb` | Materials Project API setup | Imports `MPRester` from `mp_api.client`, sets up `python-dotenv` to load an API key from a `.env` file for authenticating with the Materials Project database. |
| `Module_1_S08.ipynb` | Environment setup | Continues the Materials Project setup, installs and imports `seaborn` alongside pandas/matplotlib/dotenv, confirming the full environment is ready for subsequent analysis. |

## Learning Progression

1. **Foundations (S01–S02):** Learn pandas DataFrame basics and Matplotlib plotting fundamentals.
2. **Applied Homework (S03–S04):** Practice visualizing real materials data (density, thermal conductivity) with line and bar charts.
3. **Working with Larger Datasets (S05–S06):** Scale up to a multi-class materials dataset; learn data cleaning techniques (unit conversion, encoding, filtering).
4. **External Data Access (S07–S08):** Set up the Materials Project API client and full plotting/analysis environment (pandas, matplotlib, seaborn) in preparation for pulling real-world materials data in later modules.

## Requirements

- Python 3.10+
- `pandas`
- `matplotlib`
- `seaborn`
- `python-dotenv`
- `mp_api` (Materials Project API client)

Install with:
```bash
pip install pandas matplotlib seaborn python-dotenv mp-api
```

## Notes

- Some notebooks (S07, S08) require a **Materials Project API key** stored in a `.env` file (e.g., `MP_API_KEY=your_key_here`) and loaded via `load_dotenv()`.
- S06 contains a leftover shell/git command cell (`git add / commit / push`) that will raise a `SyntaxError` if run as Python code — it should be run in a terminal instead, not in the notebook.
