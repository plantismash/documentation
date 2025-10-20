# plantiSMASH database

The plantiSMASH database contains a set of precalculated results for selected species. These are updated every plantiSMASH version. See the [Changelog](../changelog/index.md) section. 

See the overview of results for plantiSMASH 2.0 database [View the PDF](../assets/images/BGCcount_tree_v2.pdf). The full overview of the results is availbe on the webserver at [plantiSMASH 2.0 database](https://plantismash.bioinformatics.nl/precalc/v2/). 

This directory contains **precalculated plantiSMASH database** accessible at:  
🔗 [https://plantismash.bioinformatics.nl/precalc/v2](https://plantismash.bioinformatics.nl/precalc/v2)

---

## 📁 Directory Structure

```bash
precalc/
├── v1/
├── v2-beta1/
├── v2-beta4/
└── v2/
```

---

## Details on plantiSMASH database versioning and status 

| Precalc Folder | plantiSMASH version used to generate the output | clusterBLAST Database used | Public Release Date | Nr. of genomes | Notes | Status (Public or Archived) | 
|----------------|---------------------|------------------------|--------------|--------------|-------------|--------|
| `v1/` | 1.0 | clusterBLAST database hosted on GitHub plantiSMASH 1.0 release [https://github.com/plantismash/plantismash/releases/tag/1.0](https://github.com/plantismash/plantismash/releases/tag/1.0) | DATE | 49 | Coexpress module results available in Arabidopsis thaliana [https://plantismash.bioinformatics.nl/precalc/v1/Arabidopsis_thaliana/](https://plantismash.bioinformatics.nl/precalc/v1/Arabidopsis_thaliana/) | Public in the plantiSMASH database [https://plantismash.bioinformatics.nl/precalc/v1](https://plantismash.bioinformatics.nl/precalc/v1) | 
| `v2-beta1/` | 2.0 beta 1 | clusterBLAST available at [10.5281/zenodo.16927685](https://zenodo.org/records/16927685) | DATE | 49 | NOTES | Public in the plantiSMASH database [https://plantismash.bioinformatics.nl/precalc/v2-beta1](https://plantismash.bioinformatics.nl/precalc/v2-beta1) |
| `v2-beta4/` | 2.0 beta 4 | clusterBLAST available at [10.5281/zenodo.17178066](https://zenodo.org/records/17178066) | DATE | 387 | NOTES | Public in the plantiSMASH database [https://plantismash.bioinformatics.nl/precalc/v2-beta4](https://plantismash.bioinformatics.nl/precalc/v2-beta4) |
| `v2/` | 2.0 | clusterBLAST available at [10.5281/zenodo.17396002](https://zenodo.org/records/17396002) | Public stable release | 430 | TFBS module results available in Arabidopsis thaliana for 1*10-4 p-value  and 500 bp window scanning size. | Public in the plantiSMASH database [https://plantismash.bioinformatics.nl/precalc/v2](https://plantismash.bioinformatics.nl/precalc/v2)  | 

---

## ⚙️ Usage

When running *plantiSMASH* locally, you can specify the ClusterBlast database path with the corresponding version you wish to reproduce:

```bash
run_antismash.py input.gbk --clusterblast --clusterblast-database /path/to/precalc/clusterblastdb/
```


## 📄 License and Citation

See [How to cite plantiSMASH](https://plantismash.github.io/documentation/about/#how-to-cite). 