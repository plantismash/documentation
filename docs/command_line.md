Command Line Use
----------------

The plantiSMASH command line tool comes with a built-in help system. Use
`python run_antismash.py -h` to display help for the most common options, or `python run_antismash.py --help-showall` to get a description of all possible options.


### 1. Run a test dataset 

### 1.1. Run PlantiSMASH on a NCBI reference genome (genebank format) to test
```bash
mkdir -p test_datasets/Arabidopsis_thaliana
cd test_datasets/Arabidopsis_thaliana
datasets download genome accession GCF_000001735.4 --include gbff
unzip ncbi_dataset.zip
python ../../run_antismash.py --clusterblast --knownclusterblast --verbose --debug --limit -1 --taxon plants --outputfolder result/ ncbi_dataset/data/GCF_000001735.4/genomic.gbff
# --clusterblast --knownclusterblast are optional
```
### 1.2. Run PlantiSMASH on a genome with gff3 + fasta
```bash
python run_antismash.py --verbose --debug --limit -1 --taxon plants --outputfolder result/ --use_phase --gff3 path/to/gff3/file path/to/fasta/file
# Please check the error message. The genome names in the gff3 file may differ from those in the fasta file, causing an error.
```
## Note
It is recommended to change the output folder or delete it every time you run PlantiSMASH. Because when using the same output folder, files from the previous run may be partially preserved (only rewriting files with the same names).


### Customising output
Output directories and custom names for output can be specified, instead of using the input filename by default
(see the `--output` family of arguments).
