# Reproducing the Main Manuscript Figures

Each main-text figure in the published manuscript has a dedicated Jupyter notebook
in [`pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/`](https://github.com/surbut/aladynoulli2/tree/main/pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean)
(stripped of large output cells, kept lean for git tracking; full
exploration-version notebooks are retained in the parent
`main_paper_figures/` directory for the authors' reference).
The notebooks run top-to-bottom against the released Zenodo data archive
([DOI 10.5281/zenodo.20187989](https://doi.org/10.5281/zenodo.20187989)).

| Figure | Topic | Notebook | Rendered output |
|---|---|---|---|
| **Figure 1** | Model overview (architecture schematic + theta/phi/lambda relationships) | [`Figure1_Model_Overview.ipynb`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/Figure1_Model_Overview.ipynb) | `paper_figs/Fig1.pdf` |
| **Figure 2** | Population-level disease signature patterns and temporal evolution | [`Figure2_Population_Level_Patterns.ipynb`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/Figure2_Population_Level_Patterns.ipynb) | `paper_figs/fig2/fig2.pdf` |
| **Figure 3** | Individual-specific trajectories (Panels A, B) and heterogeneity within disease subtypes (Panel C) | Panels A + B: [`Figure3_Individual_Trajectories.ipynb`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/Figure3_Individual_Trajectories.ipynb)<br/>**Panel C (line-filled heterogeneity plots for MI / Breast / MDD): [`R3_Q8_Heterogeneity_MainPaper_Method.html`](reviewer_responses/notebooks/R3/R3_Q8_Heterogeneity_MainPaper_Method.html)** (already rendered on this site) | `paper_figs/fig3/fig3.pdf` (assembled), `paper_figs/fig3/line_filled_*.pdf` (Panel C panels) |
| **Figure 4** | Genetic architecture: GWAS lead variants, RVAS hits, PRS heatmaps per disease subtype | [`Figure4_Genetic_Validation.ipynb`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/Figure4_Genetic_Validation.ipynb) | `paper_figs/fig4/fig4.pdf` |
| **Figure 5** | Multi-disease risk prediction performance vs PCE / PREVENT / GAIL / QRISK3 / Cox (centered model — as in shipped manuscript) | [`Figure5_Predictive_Performance.ipynb`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/Figure5_Predictive_Performance.ipynb)<br/>(reparam variant lives under Reparam Results on this site: [`Figure5_REPARAM.html`](reparam/Figure5_REPARAM.html)) | `paper_figs/fig5/fig5.pdf` |

## Shared utility libraries

The notebooks import helper functions from:

- [`pyScripts/fig3_utils.py`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/fig3_utils.py) — Figure 3 trajectory / heterogeneity helpers
- [`pyScripts/fig4_utils.py`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/fig4_utils.py) — Figure 4 AUC / ROC / calibration helpers
- [`pyScripts/fig5utils.py`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/fig5utils.py) — Figure 5 prediction-evaluation helpers (`evaluate_static_auc`, `evaluate_dynamic_auc`, etc.)

## Required inputs

Each notebook loads trained checkpoints and population data from the Zenodo
deposit:

- **Model checkpoints** (UKB pooled + per-batch): `aladynoulli2-main_zenodo.zip → checkpoints/`
- **Numerical data files** (signature loadings, lead-SNP tables, performance metrics, RVAS results): `SuppDataFiles_for_zenodo.zip`
- **PheCode-ICD mapping** (public): `phewascatalog.org/phecodes_icd10cm`

Individual-level UK Biobank, MGB, and All of Us data are not redistributable;
the notebooks can be re-run by approved researchers using their own data access
following the procedures described in the manuscript Methods.

## Suggested workflow to regenerate any figure

```bash
# 1. Clone repo and pull released code archive
git clone https://github.com/surbut/aladynoulli2
cd aladynoulli2
# OR: download the Zenodo v1.0 snapshot
# wget https://zenodo.org/records/20187989/files/aladynoulli2-main_zenodo.zip

# 2. Set up environment (Python 3.12+ with PyTorch, NumPy, Pandas, Matplotlib, Seaborn, scikit-learn)
python3 -m venv aladyn_env
source aladyn_env/bin/activate
pip install torch numpy pandas matplotlib seaborn scikit-learn jupyter

# 3. Open the relevant notebook and run top-to-bottom
jupyter notebook pyScripts/dec_6_revision/new_notebooks/main_paper_figures_clean/Figure2_Population_Level_Patterns.ipynb
```

## Caveats / notes

- The figures were rendered against the centered (production) model
  (`pyScripts_forPublish/clust_huge_amp_vectorized.py`); the reparam variant
  (`pyScripts_forPublish/clust_huge_amp_vectorized_reparam.py`) was the source
  for Figure 5 panels showing the centered-vs-reparam comparison.
- Figure 1 (model overview schematic) is partially hand-assembled in Adobe
  Illustrator; the notebook produces the component plots used in panels B–D.
- Extended Data figures use the same notebook → caption convention. See the
  Methods section of the manuscript for the full ED-figure pipeline.
