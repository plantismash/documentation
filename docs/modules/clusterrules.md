# BGC detection and cluster rules 

In its rule-based BGC detection mode, plantiSMASH first runs a set of BGC-related HMM profiles on the input data and then uses manually curated rules to identify the BGCs.

The currently used rules can be found at [GitHub](https://github.com/plantismash/plantismash/tree/master/antismash/generic_modules/hmm_detection), and a summary is available [here](../glossary.md)

For how to customise the rules see the [plantiSMASH Developer Wiki](https://github.com/plantismash/plantismash/wiki).

## 1. How do rules find BGCs?
### 1.1 Identify domains of proteins
PlantiSMASH detects protein domains (HMMs) by running hmmerscan. The HMMs files, `cluster_rules.txt`, `hmmdetails.txt`, and `filterhmmdetails.txt` for plants are in `plant`. The `hmmdetails.txt` controls which HMMs will be used (4th column) and the bitscore cutoff (3rd column) to filter hmmerscan results. Usually the bitscore cutoff is `-1` equal to no filter. 

The results are recorded in the output .gbk files. To only show the HMMs with highest bitscore from matches on same proteins sequence range, add them in `filterhmmdetails.txt`. For example, the same domain range match HMM UDPGT and UDPGT_2 , but the output will only show the one with highest bitscore.

Note: Another module by using the command `--full-hmmer` will use Pfam-A.hmm to identify any kind of domains. But the results only recorded in the output .gbk files and did not used in other module.

### 1.2. Clustering the neighboring genes with identified domains HMMs matches
This involves the `essential` and `Cutoff` of a rule in `cluster_rules.txt`.
A rule is usually formed as follows:
```bash
Name	        Rule	                             Cutoff (in kb)	Extension (in kb)
Product type	minimum(3,[required],[core_list])	5	           1
```

The `core_list` is a list of HMMs names of domains determining product type, such as `Chal _ stic _ synt _ C/Chal _ stic _ synt _ N` for the rule `polyketide`. Here the two HMMs names are joined by `/`, representing the saved cluster contains at least one of them. If joined by `,` , the cluster containing both domains will be saved.

In `required`, each HMMs name is joined by `,` , representing the saved cluster contains at least one of them. The `required` almost is the list of HMMs record in `hmmdetails.txt` because the clustering starts from the gene with a HMM (in the list) match. Then check the HMM matches of neighboring genes whether in the `required`. If a neighboring gene with the match belongs to the `required`, then add this gene and check the neighbors of it and so on until no new gene adding in the cluster. 

The span of left and right “neighborhood” of a gene on the conift or on the chromosome is calculated dynamically by function `get_dynamic_cutoff_multiplier`.

Simply, `left span = right span = Cutoff*(the span of the nearest ten genes)/10`

In idea situation and `Cutoff = 5`, the neighboring genes are the nearest ten genes. But if one of the nearest is way far away then it will be in the ‘neighborhood’. You can increase the cutoff to consider more neighbor genes. When cutoff = 10, then the neighboring genes must include the nearest 10 genes.

### 1.3. Filter the clusters
The domains composition of the cluster contains at least two different domains (`--min-domain-number  2`  is default) and meets `core_list`.

The cluster contains at least three genes with `required` HMMs matches (set by the number behind `minimum(`) and they sharing the similarity below 50% (`--cdh-cutoff 0.5` is default). The similarity is calculated by CD-HIT. Maybe meet the error of memory, the default is `--cdh-memory  2000`.

### 1.4. output
The cluster also contain genes in the `Extension` of the both ends biosynthetic genes. The cluster type is same to the name of rule found and saved it. 
