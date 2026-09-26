# Brain aging cell-cell communication analyses

Three analysis notebooks from a human brain aging project using FastCCC. The notebooks cover donor-level cell-cell communication in two prefrontal cortex (PFC) datasets and one hippocampal dataset. Saved outputs have been removed from this public copy; the analysis code is otherwise taken from the versions previously uploaded to `MaLab-scGenomics/BrainAging`.

| Notebook | Scope |
| --- | --- |
| [`FastCCC_pfc70_cpdbv5_mainline_v2-test (1)-备份.ipynb`](notebooks/FastCCC_pfc70_cpdbv5_mainline_v2-test%20%281%29-%E5%A4%87%E4%BB%BD.ipynb) | Multi-cohort PFC analysis of 70 donors: per-donor FastCCC, age trends, ligand-receptor drivers, and network metrics. |
| [`FastCCC_pfc_jeffries_cpdbv5_donor_age_mainline-备份.ipynb`](notebooks/FastCCC_pfc_jeffries_cpdbv5_donor_age_mainline-%E5%A4%87%E4%BB%BD.ipynb) | Independent PFC donor-age analysis with CellPhoneDB v5 annotations. |
| [`FastCCC_hippocampus_GSE286609_group_latent_time-1.ipynb`](notebooks/FastCCC_hippocampus_GSE286609_group_latent_time-1.ipynb) | Hippocampal diagnosis-group comparisons and neurogenic latent-time analysis. |

## Running the notebooks

These are research notebooks, not a turnkey pipeline. They require the corresponding `.h5ad` inputs, donor metadata, and FastCCC interaction databases. The path/configuration cell near the top of each notebook contains paths from the original Linux analysis server; update those paths before running elsewhere. The notebooks use Python with FastCCC, Scanpy, pandas, NumPy, SciPy, Matplotlib, seaborn, and, in some sections, NetworkX, gseapy, and matplotlib-venn. The PFC analyses use CellPhoneDB v5 annotation files; the hippocampal notebook points to a CellChat database. Check each notebook's configuration before selecting a database.

The 70-donor PFC notebook additionally imports four project-specific modules from the server home directory: `ccc_models`, `ccc_cpdb`, `ccc_network`, and `ccc_viz`. Those modules are not included here, so that notebook cannot be run end-to-end from this repository alone. Input datasets and database files are also not included. The notebooks were checked for valid JSON and Python syntax; they have not been rerun in this repository.

## Data and provenance

The hippocampal notebook identifies the source study as GEO accession `GSE268609`. Its filename uses `GSE286609`, while its configured input path uses `GSE268609`; verify the accession and local input file before reuse. For the PFC datasets, see the dataset and metadata descriptions in the corresponding notebooks. No raw donor-level expression data are published in this repository.
