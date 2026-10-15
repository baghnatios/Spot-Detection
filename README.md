# Spot Detection

Multicycle fluorescence spot detection and barcode analysis for C8/D8 wells. This checkout tracks `baghnatios/Spot-Detection` on `main`.

## Notebook order

1. `notebooks/0304_v11_mac_edited.ipynb`: detector candidates, candidate union, features and QA/crop provenance.
2. `notebooks/05_truth_matching_side_table_bound_fullwell_compatible_all_caches_offaware_patched.ipynb`: bind candidate tables to annotated truth and generate supervised splits.
3. `notebooks/06_model_training_fixed.ipynb`: train/calibrate model families and produce model cards, predictions and evaluation reports.
4. `notebooks/07_fullwell_inference (1).ipynb`: apply saved models and generate full-well predictions and visualizations.

Launch Jupyter from the checkout or `notebooks/`. Notebook 03/04 can alternatively use `SPOT_REPO_ROOT`. Set each notebook's configuration/data-root override to the actual microscopy dataset location. Raw microscopy TIFFs are external and are not included here. Published `tables/`, `annotations/` and `artifacts/` are experiment evidence; their run IDs record provenance.

Scientific Python and optional model dependencies are imported in setup cells. This repository does not yet provide a fully pinned environment. A successful clone or path check does not demonstrate end-to-end reproduction of model results. Review setup cells before installing dependencies and running training.

The separate `../Local Notebook/spot_detection_pipeline_v3(1).ipynb` is an older Google Colab/Drive pipeline retained as a distinct source snapshot. It is not a replacement for the staged published pipeline above. Its Colab mount paths are intentional platform-specific code.
