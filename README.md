# treg_aging

---

## System requirements

### Hardware and operating system

| Component | Specification |
|---|---|
| Operating system | macOS 27.2.1 |
| Processor | Apple M3 Ultra |
| Memory | 256 GB RAM |

The analysis was run with 256 GB RAM.

### Software

**R 4.5.2**

| Package | Version |
|---|---|
| Seurat | 5.3.1 |
| sctransform | 0.4.3 |
| harmony | 2.0.5 |
| clusrank | 1.0-4 |
| CellChat | 2.2 |
| Rphenograph | 0.99.1 |
| clustree | 0.5.1 |
| slingshot | 2.18 |
| tradeSeq | 1.24 |
| mgcv | 1.9-4 |

**Python 3.9**

| Package | Version |
|---|---|
| anndata | 0.10 |
| h5py | 3.14 |
| NumPy | 1.26 |
| pandas | 2.3 |
| SciPy | 1.13 |
| Matplotlib | 3.9 |

**Imaging**

| Tool | Version |
|---|---|
| napari | 0.4.19 |
| napari-cosmx | 0.4.17.4 |
| affinder | 0.5.0 |
| napari_alignment_tools | 0.0.1 |

---

## Installation

Clone the repository:

```bash
git clone https://github.com/[user]/[repo].git
cd [repo]
```

Install the R packages:

```r
install.packages(c("Seurat", "sctransform", "harmony", "clusrank", "clustree",
                   "mgcv", "remotes", "BiocManager"))
BiocManager::install(c("slingshot", "tradeSeq"))
remotes::install_github("jinworks/CellChat")
remotes::install_github("JinmiaoChenLab/Rphenograph")
```

Install the Python packages:

```bash
python3.9 -m venv .venv
source .venv/bin/activate
pip install anndata==0.10.* h5py==3.14.* numpy==1.26.* pandas==2.3.* \
            scipy==1.13.* matplotlib==3.9.*
```

Install napari and the alignment plugins:

```bash
pip install "napari[all]==0.4.19" napari-cosmx affinder napari_alignment_tools
```
