# Structural-Erasure-Toolkit

Code, metrics, and documentation for:
**“Retrieval Lost to Time: A Typology of Structural Erasure in Intellectual and Political Memory”**
Evlondo Cooper, 2025

---

## Overview

The **Structural Erasure Toolkit** operationalizes the framework introduced in the paper *Retrieval Lost to Time*.
It measures how ideas and contributors appear, disappear, or shift within collective memory systems.

The notebook implements the **Retrieval Integrity Index (RII)**, a composite measure that quantifies how stably and accurately a subject is represented over time. RII is built from four normalized components:

| Symbol | Meaning                              | Interpretation                                           |
| :----: | :----------------------------------- | :------------------------------------------------------- |
|  **P** | Presence rate (visibility)           | Frequency of mentions within a corpus                    |
|  **C** | Coverage ratio (breadth)             | Fraction of verified contributions receiving recognition |
|  **S** | Substitution share (credit accuracy) | Portion of mentions that are misattributed               |
|  **V** | Volatility label (stability)         | Frequency of reclassification or credit change           |

Each component corresponds to one or more of the paper’s five **modes of erasure**: **Silencing, Reclassification, Compression, Substitution,** and **Tactical Forgetting**.
Together they allow quantitative inspection of structural bias, recovery patterns, and retrieval integrity across time.

---

## Repository Structure

```
├── data/
│   └── samples/                        # Example CSV and JSON inputs
├── notebooks/
│   └── Structural_Erasure_Toolkit_v1.0.ipynb   # Main interactive notebook
├── environment.yml                     # Reproducible Conda environment
├── LICENSE                             # MIT License
└── README.md                           # This file
```

---

## Dependencies

**Required**

* Python 3.10 or later
* NumPy
* Pandas
* Matplotlib
* ipywidgets
* Jupyter Notebook

**Installation**

Using Conda (recommended):

```
conda env create -f environment.yml
conda activate erasure-env
```

Using pip (alternative):

```
pip install numpy pandas matplotlib jupyter ipywidgets
```

---

## Running the Notebook

Open:

```
notebooks/Structural_Erasure_Toolkit_v1.0.ipynb
```

### Quick Start (3 Minutes)

1. **Run the next cell** (“Environment Check”) or select **Kernel → Restart & Run All**.
2. **Try a sample:** click **Run Sample → Generate RII** to view the complete workflow.
3. **Use your own data:** upload a **JSON** or **CSV** file, then click **Analyze**.

You will receive validated inputs, an RII score with 95 percent bootstrap confidence intervals, an explainer chart, and an exportable Markdown or PDF report.

---

## Upload and Validation

Use the widget interface to upload one JSON file *or* two CSVs:

* `presence.csv` must include `corpus_total_items`, `mentions_total`, and `misattributed_mentions`.
  *(Optional: `t`, `mentions` for timeline data.)*
* `classification.csv` must include `distinct_recognized_contributions`, `verified_contributions`, `reclassification_events`, and `time_intervals`.

If any required fields are missing or misnamed, the interface will display descriptive error messages.
Once validation passes, click **Analyze** to generate results.

---

## Output

The toolkit generates:

* A **Retrieval Integrity Index (RII)** summary table
* 95% bootstrap confidence intervals
* Visualization of recognition and volatility trends
* A Markdown report (`RII_Report.md`) with legend, methods note, and limitations
* Optional PDF export if `nbconvert` is available

All processing occurs locally; no uploaded text leaves the user’s environment.

---

## Educational and Ethical Notes

* **Ethical Disclaimer:** Metrics represent informational patterns, not moral value or intent.
  Results depend on corpus quality, coding consistency, and interpretive transparency.
* **Reflexivity (Wikipedia workflow):** Wikipedia is part of the retrieval process; its structural and editorial biases are included in what is being measured.
* **Final Note:** All data are partial records of attention; interpretation remains a human responsibility.

---

## Citation

If you use this repository, please cite:

Cooper, E. (2025). *Retrieval Lost to Time: A Typology of Structural Erasure in Intellectual and Political Memory.* Zenodo. [https://doi.org/10.5281/zenodo.XXXXXXX](https://doi.org/10.5281/zenodo.XXXXXXX)

Cooper, E. (2025). *Structural Erasure Toolkit (v1.0): Quantifying Retrieval Integrity Across Collective Memory Systems.* Zenodo. [https://doi.org/10.5281/zenodo.XXXXXXX](https://doi.org/10.5281/zenodo.XXXXXXX)

---

## License

This repository is released under the **MIT License**.

---
