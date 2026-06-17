# Reviewer Response Analyses

This directory contains all interactive analyses addressing reviewer questions and concerns.

## 📁 Structure

```
reviewer_responses/
├── README.md                      # This file - navigation hub
├── notebooks/
│   ├── R1/                        # Referee #1 analyses
│   ├── R2/                        # Referee #2 analyses
│   ├── R3/                        # Referee #3 analyses
│   ├── framework/                 # Framework overview
│   ├── archive/                   # Archived/removed notebooks
│   └── results/                   # Reviewer-specific results
├── preprocessing/                 # Data preprocessing utilities
│   ├── preprocessing_utils.py     # Standalone preprocessing functions
│   ├── create_preprocessing_files.html  # Interactive preprocessing notebook
│   └── WORKFLOW.md                # Complete workflow documentation
└── SIMPLE_EXAMPLE.py              # Simple example of preprocessing functions
```

## 🎯 How to Use

1. Click on any question below to navigate to its dedicated analysis notebook
2. Each notebook is self-contained and can be run independently
3. All notebooks use the same data paths and setup

## 🔧 Technical Notes

- **Results**: Stored in `notebooks/results/` (within notebooks directory)
- **Source Code**: Shared code is in `pyScripts_forPublish/` (not duplicated here)
- **Paths**: Notebooks use absolute paths for reliability
- **Data**: All notebooks are self-contained and can be run independently

---

## Referee #1: Human Genetics, Disease Risk

| Question | Notebook | Status |
|----------|----------|--------|
| **Q1**: Selection bias / socioeconomic bias | [`notebooks/R1/R1_Q1_Selection_Bias.html`](notebooks/R1/R1_Q1_Selection_Bias.html) | ✅ Complete |
| **Q3**: Clinical/biological meaningfulness | [`notebooks/R1/R1_Q3_Clinical_Meaning.html`](notebooks/R1/R1_Q3_Clinical_Meaning.html) | ✅ Complete |
| **Q3**: ICD vs PheCode aggregation | [`notebooks/R1/R1_Q3_ICD_vs_PheCode_Comparison.html`](notebooks/R1/R1_Q3_ICD_vs_PheCode_Comparison.html) | ✅ Complete |
| **Q7**: Heritability estimates | [`notebooks/R1/R1_Q7_Heritability.html`](notebooks/R1/R1_Q7_Heritability.html) | ✅ Complete |
| **Q9**: AUC vs clinical risk scores | [`notebooks/R1/R1_Q9_AUC_Comparisons.html`](notebooks/R1/R1_Q9_AUC_Comparisons.html) | ✅ Complete |
| **Q10**: Age-specific discrimination | [`notebooks/R1/R1_Q10_Age_Specific.html`](notebooks/R1/R1_Q10_Age_Specific.html) | ✅ Complete |
| **Additional**: Biological plausibility (CHIP) | [`notebooks/R1/R1_Biological_Plausibility_CHIP.html`](notebooks/R1/R1_Biological_Plausibility_CHIP.html) | ✅ Complete |
| **Additional**: Clinical utility (dynamic risk) | [`notebooks/R1/R1_Clinical_Utility_Dynamic_Risk_Updating.html`](notebooks/R1/R1_Clinical_Utility_Dynamic_Risk_Updating.html) | ✅ Complete |
| **Additional**: Genetic validation (GWAS) | [`notebooks/R1/R1_Genetic_Validation_GWAS.html`](notebooks/R1/R1_Genetic_Validation_GWAS.html) | ✅ Complete |
| **Additional**: Genetic validation (Gene-based RVAS) | [`notebooks/R1/R1_Genetic_Validation_Gene_Based_RVAS.html`](notebooks/R1/R1_Genetic_Validation_Gene_Based_RVAS.html) | ✅ Complete |
| **Additional**: Multi-disease patterns | [`notebooks/R1/R1_Multi_Disease_Patterns_Competing_Risks.html`](notebooks/R1/R1_Multi_Disease_Patterns_Competing_Risks.html) | ✅ Complete |
| **Additional**: Robustness (LOO validation) | [`notebooks/R1/R1_Robustness_LOO_Validation.html`](notebooks/R1/R1_Robustness_LOO_Validation.html) | ✅ Complete |

## Referee #2: EHRs

| Concern | Notebook | Status |
|---------|----------|--------|
| Temporal accuracy / leakage | [`notebooks/R2/R2_Temporal_Leakage.html`](notebooks/R2/R2_Temporal_Leakage.html) | ✅ Complete |
| Model validity / learning | [`notebooks/R2/R2_R3_Model_Validity_Learning.html`](notebooks/R2/R2_R3_Model_Validity_Learning.html) | ✅ Complete |
| **Washout approaches comparison** | [`notebooks/R2/R2_Washout_Comparisons.html`](notebooks/R2/R2_Washout_Comparisons.html) | ✅ Complete |
| **Delphi Phecode mapping comparison** | [`notebooks/R2/R2_Delphi_Phecode_Mapping.html`](notebooks/R2/R2_Delphi_Phecode_Mapping.html) | ✅ Complete |

## Referee #3: Statistical Genetics, PRS

| Question | Notebook | Status |
|----------|----------|--------|
| **Q3**: Avoiding reverse causation (washout analysis) | [`notebooks/R3/R3_AvoidingReverseCausation.html`](notebooks/R3/R3_AvoidingReverseCausation.html) | ✅ Complete |
| **Q4**: Decreasing_Hazards | [`notebooks/R3/R3_Q4_Decreasing_Hazards_Censoring_Bias.html`](notebooks/R3/R3_Q4_Decreasing_Hazards_Censoring_Bias.html) | ✅ Complete |
| **Q8**: Heterogeneity analysis (main paper method) | [`notebooks/R3/R3_Q8_Heterogeneity_MainPaper_Method.html`](notebooks/R3/R3_Q8_Heterogeneity_MainPaper_Method.html) | ✅ Complete |
| **Q8**: Heterogeneity analysis (continued) | [`notebooks/R3/R3_Q8_Heterogeneity_Continued.html`](notebooks/R3/R3_Q8_Heterogeneity_Continued.html) | ✅ Complete |
| **Population Stratification**: Continuous ancestry effects | [`notebooks/R3/R3_Population_Stratification_Ancestry.html`](notebooks/R3/R3_Population_Stratification_Ancestry.html) | ✅ Complete |
| **Additional**: Linear vs Nonlinear mixing | [`notebooks/R3/R3_Linear_vs_NonLinear_Mixing.html`](notebooks/R3/R3_Linear_vs_NonLinear_Mixing.html) | ✅ Complete |
| **Additional**: Cross-cohort similarity | [`notebooks/R3/R3_Cross_Cohort_Similarity.html`](notebooks/R3/R3_Cross_Cohort_Similarity.html) | ✅ Complete |

---

## Framework Overview

| Notebook | Description |
|----------|-------------|

---

## Preprocessing & Workflow

**Addresses reviewer questions about data preprocessing and the complete analysis workflow.**

| Resource | Description |
|----------|-------------|
| [`preprocessing/WORKFLOW.md`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/reviewer_responses/preprocessing/WORKFLOW.md) | **Complete end-to-end workflow documentation** - Step-by-step guide from preprocessing → batch training → master checkpoint → prediction |
| [`preprocessing/create_preprocessing_files.html`](preprocessing/create_preprocessing_files.html) | Interactive notebook for data preprocessing with visualizations (smoothed prevalence, clustering, signature references) |
| [`preprocessing/enhanced_simulation_showcase_v2.html`](preprocessing/enhanced_simulation_showcase_v2.html) | Enhanced simulation framework with comprehensive parameter recovery analysis, training progress tracking, and calibration validation |
| [`preprocessing/preprocessing_utils.py`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/reviewer_responses/preprocessing/preprocessing_utils.py) | Standalone preprocessing functions (`compute_smoothed_prevalence_at_risk`, `create_initial_clusters_and_psi`, `create_reference_trajectories`) |
| [`preprocessing/SIMPLE_EXAMPLE.py`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/reviewer_responses/preprocessing/SIMPLE_EXAMPLE.py) | Minimal copy-paste example demonstrating how to use the preprocessing functions |

**Workflow Overview:**
1. **Preprocessing**: Create smoothed prevalence, initial clusters, and reference trajectories
2. **Batch Training**: Run `run_aladyn_batch_vector_e_censor_nolor` with E matrix *using complete patient history* (no LR regularization on gamma)
3. **Master Checkpoint**: Generate master checkpoint (phi and psi)
4. **Prediction**: Run `run_aladyn_predict_with_master_vector_cenosrE` (automatically loads `E_enrollment_full.pt`) meaning it's trained with only enrollment data.

See [`preprocessing/WORKFLOW.md`](https://github.com/surbut/aladynoulli2/blob/main/pyScripts/dec_6_revision/new_notebooks/reviewer_responses/preprocessing/WORKFLOW.md) for detailed instructions.

---

## Quick Navigation

### ✅ All Completed Analyses

**Referee #1:**
- Selection bias (IPW): [`notebooks/R1/R1_Q1_Selection_Bias.html`](notebooks/R1/R1_Q1_Selection_Bias.html)
- Clinical meaning (FH): [`notebooks/R1/R1_Q3_Clinical_Meaning.html`](notebooks/R1/R1_Q3_Clinical_Meaning.html)
- ICD vs PheCode aggregation: [`notebooks/R1/R1_Q3_ICD_vs_PheCode_Comparison.html`](notebooks/R1/R1_Q3_ICD_vs_PheCode_Comparison.html)
- Heritability: [`notebooks/R1/R1_Q7_Heritability.html`](notebooks/R1/R1_Q7_Heritability.html)
- AUC comparisons: [`notebooks/R1/R1_Q9_AUC_Comparisons.html`](notebooks/R1/R1_Q9_AUC_Comparisons.html)
- Age-specific discrimination: [`notebooks/R1/R1_Q10_Age_Specific.html`](notebooks/R1/R1_Q10_Age_Specific.html)
- Biological plausibility (CHIP): [`notebooks/R1/R1_Biological_Plausibility_CHIP.html`](notebooks/R1/R1_Biological_Plausibility_CHIP.html)
- Clinical utility (dynamic risk): [`notebooks/R1/R1_Clinical_Utility_Dynamic_Risk_Updating.html`](notebooks/R1/R1_Clinical_Utility_Dynamic_Risk_Updating.html)
- Genetic validation (GWAS): [`notebooks/R1/R1_Genetic_Validation_GWAS.html`](notebooks/R1/R1_Genetic_Validation_GWAS.html) - **Identifies 10 novel loci for Signature 5 not found in individual trait GWAS**
- Genetic validation (Gene-based RVAS): [`notebooks/R1/R1_Genetic_Validation_Gene_Based_RVAS.html`](notebooks/R1/R1_Genetic_Validation_Gene_Based_RVAS.html)
- Multi-disease patterns: [`notebooks/R1/R1_Multi_Disease_Patterns_Competing_Risks.html`](notebooks/R1/R1_Multi_Disease_Patterns_Competing_Risks.html)
- Robustness (LOO validation): [`notebooks/R1/R1_Robustness_LOO_Validation.html`](notebooks/R1/R1_Robustness_LOO_Validation.html)

**Referee #2:**
- Temporal leakage: [`notebooks/R2/R2_Temporal_Leakage.html`](notebooks/R2/R2_Temporal_Leakage.html)
- Model validity / learning: [`notebooks/R2/R2_R3_Model_Validity_Learning.html`](notebooks/R2/R2_R3_Model_Validity_Learning.html)
- Washout approaches comparison: [`notebooks/R2/R2_Washout_Comparisons.html`](notebooks/R2/R2_Washout_Comparisons.html)
- Delphi Phecode mapping comparison: [`notebooks/R2/R2_Delphi_Phecode_Mapping.html`](notebooks/R2/R2_Delphi_Phecode_Mapping.html)

**Referee #3:**
- Avoiding reverse causation (washout analysis): [`notebooks/R3/R3_AvoidingReverseCausation.html`](notebooks/R3/R3_AvoidingReverseCausation.html)
- Heterogeneity analysis (main paper method): [`notebooks/R3/R3_Q8_Heterogeneity_MainPaper_Method.html`](notebooks/R3/R3_Q8_Heterogeneity_MainPaper_Method.html)
- Heterogeneity analysis (continued): [`notebooks/R3/R3_Q8_Heterogeneity_Continued.html`](notebooks/R3/R3_Q8_Heterogeneity_Continued.html)
- Population stratification: [`notebooks/R3/R3_Population_Stratification_Ancestry.html`](notebooks/R3/R3_Population_Stratification_Ancestry.html)
- Linear vs Nonlinear mixing: [`notebooks/R3/R3_Linear_vs_NonLinear_Mixing.html`](notebooks/R3/R3_Linear_vs_NonLinear_Mixing.html)
- Cross-cohort similarity: [`notebooks/R3/R3_Cross_Cohort_Similarity.html`](notebooks/R3/R3_Cross_Cohort_Similarity.html)

**Framework:**

✅ All complete
