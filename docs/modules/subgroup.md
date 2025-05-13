# Subgroup identification module

plantiSMASH includes a subgroup identification module that helps predict substrate specificities for enzyme subfamilies in plant biosynthetic gene clusters. Currently, this module supports several key protein families: cellulose synthases, UDP-glucuronosyltransferases (UDPGTs), short-chain dehydrogenases (SDRs), and oxidosqualene cyclases (OSCs).

The workflow combines:

- HMMER to detect domain-containing proteins,

- pplacer to phylogenetically place these proteins onto precomputed reference trees, and

- GraPhlAn to generate interactive and color-coded visualizations.

How it works

1. Domain detection: The target genome is scanned with profile HMMs to detect relevant domains.

2. Phylogenetic placement: Identified protein sequences are placed onto curated reference trees using pplacer.

3. Subgroup inference: If a target protein's neighboring nodes in the tree belong to a consistent known subgroup, it is inferred to belong to that subgroup.

4. HMM matching: Separately, the full-length protein is scored against subgroup-specific HMMs. If the top-scoring subgroup matches the pplacer result, this is marked as high-confidence.

5. Visualization: Color-coded trees are generated with GraPhlAn to display placements and subgroup contexts.

Interpreting results
In the cluster overview, when a subgroup is detected for a gene, a clickable label is shown. Clicking on the detected subgroup name will open an interactive phylogenetic tree showing the target protein and its neighbors, colored by subgroup.

Subgroup predictions that align with known biosynthetic product types are marked with an asterisk *. If no consistent assignment is possible, or if the HMMER and pplacer results disagree, the module presents both results for user inspection.

![Subgroup](../assets/images/subgroup.png)

## Supported subgroups in v2.0

This module enables the subgroup of protein sequences from various families based on the results of `hmmer` scans using domain pHMMs. The families it covers include the Cellulose synthase (CSLs) family (Chung et al., 2020; Jozwiak et al., 2020), UDP-glucuronosyltransferase (UGTs) family (Louveau & Osbourn, 2019), short-chain dehydrogenases/reductases (SDRs) family (Moummou et al., 2012), and oxidosqualene cyclase (OSCs) family (unpublished work).

## References for the Subgroup Module

Chung, S. Y., Seki, H., Fujisawa, Y., Shimoda, Y., Hiraga, S., Nomura, Y., Saito, K., Ishimoto, M., & Muranaka, T. (2020). A cellulose synthase-derived enzyme catalyses 3-O-glucuronosylation in saponin biosynthesis. Nature Communications 2020 11:1, 11(1), 1–11. https://doi.org/10.1038/s41467-020-19399-0


Jozwiak, A., Sonawane, P. D., Panda, S., Garagounis, C., Papadopoulou, K. K., Abebie, B., Massalha, H., Almekias-Siegl, E., Scherf, T., & Aharoni, A. (2020). Plant terpenoid metabolism co-opts a component of the cell wall biosynthesis machinery. Nature Chemical Biology 2020 16:7, 16(7), 740–748. https://doi.org/10.1038/s41589-020-0541-x


Louveau, T., & Osbourn, A. (2019). The Sweet Side of Plant-Specialized Metabolism. Cold Spring Harbor Perspectives in Biology, 11(12), a034744. https://doi.org/10.1101/CSHPERSPECT.A034744


Moummou, H., Kallberg, Y., Tonfack, L. B., Persson, B., & van der Rest, B. (2012). The Plant Short-Chain Dehydrogenase (SDR) superfamily: Genome-wide inventory and diversification patterns. BMC Plant Biology, 12(1), 1–17. https://doi.org/10.1186/1471-2229-12-219/FIGURES/7

## Customization
This module is modular and can be extended to support additional protein families or custom subgroup definitions. For detailed instructions on how to customize the subgroup analysis (e.g. adding new reference trees or HMMs), please refer to the [plantiSMASH Wiki](https://github.com/plantismash/plantismash/wiki). 
