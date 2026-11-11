# Neurons — in vivo electrophysiology analysis

Exploratory repository for spike-train characterization and comparison of putative dorsal raphe nucleus (DRN, serotonin) and ventral tegmental area (VTA, dopamine) neurons.

## Structure

- `data/raw/drn_serotonin_female/` — DRN spike and spike-characteristic CSV exports
- `data/raw/vta_dopamine_female/` — VTA spike and spike-characteristic CSV exports
- `data/processed/` — compiled neuron-feature tables and historic summary export
- `data/unclassified/` — original large text export; contents/format require verification
- `notebooks/` — electrophysiology comparison and exploratory ML
- `archive/scratch/` — unrelated introductory Python notebooks, retained for provenance

## Notebooks

- `notebooks/01_vta_drn_comparison.ipynb`: existing comparison notebook (unchanged)
- `notebooks/02_neuron_classification_ml.ipynb`: exploratory DRN/VTA ML notebook; its CSV paths were updated to the new layout

Run notebooks from the `notebooks/` directory. The current analysis is exploratory, not validated neuron-type identification. Region-based neuron labels are putative and do not substitute for independent cell-type validation. In particular, splitting individual spikes at random can leak neuron identity into train/test data; use a neuron- or animal-grouped split for rigorous evaluation.

## Notes

The original DRN CSVs appeared both at the repository root and in a nested directory with identical Git blob hashes. Only one canonical copy is retained. Source CSV filenames are unchanged. No raw recordings have been intentionally modified. Large notebook outputs and original, unclassified exports are preserved rather than discarded. If you used old hard-coded paths outside the ML notebook, update them to this structure.
