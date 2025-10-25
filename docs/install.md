# Download plantiSMASH Standalone

Stand-alone releases are available on  
**[GitHub Releases](https://github.com/plantismash/plantismash/releases)** and **[PyPI](https://pypi.org/project/plantismash/)**.

## Current Release
**Latest tag:**  
[![GitHub Release](https://img.shields.io/github/v/release/plantismash/plantismash?include_prereleases&sort=semver&display_name=tag&logo=github)](https://github.com/plantismash/plantismash/releases/latest)
[![PyPI](https://img.shields.io/pypi/v/plantismash?logo=pypi&label=PyPI)](https://pypi.org/project/plantismash/)

---

## Installation Options

There are two supported ways to install plantiSMASH:

1. **Recommended: Clone from GitHub and install via Conda** – creates a full reproducible environment with all external tools and the latest stable code.  
2. **Alternative: Install the Python package only (from PyPI)** – for developers or integration use; external dependencies must be installed manually.



---

## Option 1 — Recommended full installation (GitHub + Conda)

This option gives you a fully functional **standalone version** of plantiSMASH.

> 💡 **Windows users:** If you don’t already have a Linux environment,  
> follow our [Windows setup guide](windows-linux-setup.md) to install **WSL (Windows Subsystem for Linux)**.  
> This lets you run plantiSMASH natively inside Ubuntu on Windows before proceeding with the steps below.

1. Clone the latest release from Github 

      ```bash
      git clone https://github.com/plantismash/plantismash.git
      # navigate to that directory 
      cd plantismash
      ```

2. Create the Conda environment

      <details>
      <summary><b>🧩 Don’t have Conda or Mamba installed yet? Click to expand setup instructions.</b></summary>

      To create a reproducible plantiSMASH environment, you’ll need a Conda-based package manager such as **[Miniforge (recommended)](https://github.com/conda-forge/miniforge)** or **Mambaforge**.

      Follow these steps to install it on Linux (or inside WSL on Windows):

      ```bash
      # 1. Download and install Miniforge
      curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
      bash Miniforge3-$(uname)-$(uname -m).sh

      # 2. Initialize Conda
      source ~/.bashrc
      conda init bash

      # 3. Set default configuration
      conda config --set auto_activate_base false
      conda config --add channels bioconda
      conda config --add channels conda-forge
      conda config --set channel_priority strict
      ```
      💡 You only need to do this once — future plantiSMASH environments will reuse this configuration.
      </details>

      ```bash

      # Using mamba (recommended)
      mamba env create -f environment.yml
      conda activate plantismash

      ``` 

3. Verify your installation: 

      ```bash 

      # check Python entry points
      plantismash --help
      plantismash_download_databases --help

      ``` 

4. Download the required databases 

      ```bash 
      # default location is created automatically (uses appdirs)
      plantismash_download_databases
      ``` 

      Tip: to test on an example genome, you can fetch A. thaliana with the NCBI Datasets CLI and run plantiSMASH:

      ```bash 
      mkdir -p test_datasets/Arabidopsis_thaliana && cd $_

      datasets download genome accession GCF_000001735.4 --include gbff

      unzip -o ncbi_dataset.zip

      plantismash --taxon plants --limit -1 --outputfolder result/ \
      ncbi_dataset/data/GCF_000001735.4/genomic.gbff

      ``` 

## Option 2 - Python package only (advanced users)

1. Download the latest plantiSMASH standalone release from our GitHub page 

      [![GitHub Release](https://img.shields.io/github/v/release/plantismash/plantismash?include_prereleases&sort=semver&display_name=tag&logo=github)](https://github.com/plantismash/plantismash/releases/latest)

2. Ensure you have the following dependencies installed (**tested versions in parentheses**):  

      - [Glimmer](https://ccb.jhu.edu/software/glimmer/) (3.02)  
      - [GlimmerHMM](https://ccb.jhu.edu/software/glimmerhmm/) (3.0.4)  
      - [HMMER 3](http://hmmer.janelia.org/) (3.3.2)  
      - [HMMER 2](ftp://ftp.sanger.ac.uk/pub/1000genomes/ftp/technical/working/20110111_hmmer-2.3.2.tar.gz) (2.3.2) — **plantiSMASH requires `hmmpfam2`**, a legacy binary not included in HMMER 3.x.  
      Append a “2” to all HMMER 2 executables (e.g. `hmmalign` → `hmmalign2`) to avoid conflicts with HMMER 3 names.  
      - [FastTree](http://www.microbesonline.org/fasttree/) (2.1.11)  
      - [DIAMOND](https://github.com/bbuchfink/diamond) (2.0.15)  
      - [MUSCLE](http://www.drive5.com/muscle/) (3.8.31)  
      - [Prodigal](https://github.com/hyattpd/Prodigal) (2.6.3)  
      - [NCBI BLAST+](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/) (2.12.0)  
      - [CD-HIT](http://weizhongli-lab.org/cd-hit/) (4.8.1)  
      - [LibXML2](http://xmlsoft.org/) (2.10.3)  
      - [pplacer](https://matsen.fhcrc.org/pplacer/) (1.1.alpha17)  
      - [NCBI Datasets CLI](https://www.ncbi.nlm.nih.gov/datasets/) (18.9.0)  
      - [Unzip](https://linux.die.net/man/1/unzip) (6.0)  
      - [Helperlibs](https://github.com/helperlibs) (0.2.1)  
      - [Biopython](https://biopython.org/) (1.76)  

3. Once all dependencies are installed and available on your `PATH`, install the Python package:

      ``` bash 
      pip install plantismash

      ``` 

4. Verify the installation: 
      ```bash 
      plantismash --help
      plantismash_download_databases --help
      ``` 

      ⚠️ This installs only the Python code, not the external binaries.
      To run full analyses, the required tools (HMMER, BLAST, DIAMOND, etc.) must be available on your `PATH`.

## Notes and FAQs 

	•	Why Python 3.8?
This release currently targets `Python >=3.8,<3.9` for compatibility with some dependencies. Use the provided environment.

	•	HMMER2 note
plantiSMASH requires `hmmpfam2` from legacy HMMER 2 in addition to HMMER 3. The line
`bioconda/label/cf201901::hmmer2` installs the legacy binaries under distinct names to avoid conflicts.

	•	PyPI vs Conda
PyPI provides the Python package only. All native/CLI tools are installed via Conda in environment.yml.

	•	Reproducibility
The `environment.yml` pins versions of external tools; PyPI pins Python libs in `pyproject.toml`. This combination reproduces the tested setup.