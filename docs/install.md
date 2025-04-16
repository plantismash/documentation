### Download plantiSMASH Standalone

Stand-alone versions of plantiSMASH are available through **[our GitHub page](https://github.com/plantismash/plantismash)**.

#### Current Release

The current standalone release is **[plantiSMASH 2.0-beta](https://github.com/plantismash/plantismash/tree/dev)** (*December 16th, 2024*).

---

## Installation Options

There are two ways to install plantiSMASH:

1. **Downloading the standalone release** – Suitable for users who want to install plantiSMASH from a zip package and ensure dependencies are installed separately.
2. **Cloning from GitHub** – Recommended for users who want the latest development version and prefer managing dependencies in a virtual Conda environment.

---

### Option 1: Downloading the standalone release

1. Download the latest plantiSMASH standalone release from our GitHub repo:  
   [https://github.com/plantismash/plantismash/releases](https://github.com/plantismash/plantismash/releases)

2. Ensure you have the following dependencies installed (tested versions in parentheses):  


      - [Glimmer](https://ccb.jhu.edu/software/glimmer/) (3.02)  
      - [GlimmerHMM](https://ccb.jhu.edu/software/glimmerhmm/) (3.0.4)  
      - [HMMER3](http://hmmer.janelia.org/) (3.3.2)  
      - [HMMER2](ftp://ftp.sanger.ac.uk/pub/1000genomes/ftp/technical/working/20110111_hmmer-2.3.2.tar.gz) (version 2.3.2 tested). plantiSMASH requires hmmpfam2, a legacy tool from HMMER 2. This binary is no longer included in HMMER 3.x and must be installed manuallyappend a 2 to all hmmer2 executables to avoid conflict with hmmer3 executable names, like hmmalign -> hmmalign2 
      - [FastTree](http://www.microbesonline.org/fasttree/) (2.1.8)  
      - [DIAMOND](https://github.com/bbuchfink/diamond) (2.0.15)  
      - [MUSCLE](http://www.drive5.com/muscle/) (3.8.31)  
      - [Prodigal](https://github.com/hyattpd/Prodigal) (2.6.3)  
      - [NCBI Blast+](https://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/) (2.12.0)  
      - [CD-HIT](http://weizhongli-lab.org/cd-hit/) (4.8.1)  
      - [LibXML2](http://xmlsoft.org/) (2.10.3)  
      - [pplacer](https://matsen.fhcrc.org/pplacer/)  
      - [NCBI Datasets CLI](https://www.ncbi.nlm.nih.gov/datasets/) (16.40.1)  
      - [Unzip](https://linux.die.net/man/1/unzip)  
      - [Helperlibs](https://github.com/helperlibs) (0.2.1)  
      - [Biopython](https://biopython.org/) (1.76)  


3. Once all dependencies are installed, plantiSMASH should be ready to use.


---

### Option 2: Cloning from GitHub 

Using Windows? Click here for the full [Windows Setup Guide](windows-linux-setup.md).

1. Clone the latest version from GitHub:

      ```bash
      git clone -b dev https://github.com/plantismash/plantismash.git
      cd plantismash
      ```  
   
2. If not installed already, conda/mamba can be installed by following these instructions:

      ```bash
      # install miniforge
      curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
      bash Miniforge3-$(uname)-$(uname -m).sh
      # follow instructions and let it run `conda init`

      # set default channels
      source ~/.bashrc
      conda config --set auto_activate_base false
      source ~/.bashrc
      conda config --add channels bioconda
      conda config --add channels conda-forge
      conda config --set channel_priority strict  
      ```


2. Create and activate a Conda environment using the provided `environment.yml` file

      ```bash
      conda env create -f environment.yml
      conda activate plantismash
      ```

3. Download the required databases:

      ```bash
      python download_databases.py
      ```

4. Verify the installation 

      ```bash
      python run_antismash.py -h
      ```

---