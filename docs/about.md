# About plantiSMASH 

plantiSMASH allows the rapid genome-wide identification, annotation, and analysis of specialized metabolite biosynthetic gene clusters (BGCs) across the plant kingdom. It is a specialized extension of the widely used [antiSMASH](https://antismash.secondarymetabolites.org/#!/start) tool, tailored specifically to target plant genomes.

## News

Version [**2.0-beta**](https://github.com/plantismash/plantismash/tree/dev) of plantiSMASH is live now!  
plantiSMASH is an extension of the widely used tool antiSMASH, now optimized for and made to work on plant genomes.  
plantiSMASH version 2.0-beta features a range of updates and improvements in the areas of gene cluster identification, homology detection, and substrate prediction:

plantiSMASH provides:

- Specific library of pHMM models and completely novel cluster calling logic designed to work on plant genomes
- Specific plant clusterblast database from precalculated plant biosynthetic gene clusters
- Specific training model for gene finding using glimmerHMM
- Homology based metabolic modeling
- Coexpression analysis and html-based visualization on detected biosynthetic gene clusters with the CoExpress module

To top it off, these are the added features of plantiSMASH ver 2.0-beta:

- Updated library of pHMM models and the number of detection rules increased from 6 to 12, including 3 rules being updated.
- Updated plant clusterblast database with precalculated plant biosynthetic gene clusters for 382 NCBI plant genomes.
- Updated specific module for detection of repeats in BURP domains for candidate cyclopeptide BGCs.
- Implemented prediction of substrate specificities of enzyme subfamilies for cellulose synthases, UDP-glucuronosyltransferases, short-chain dehydrogenases, and oxidosqualene cyclases.


## Dependencies 
plantiSMASH is powered by several open-source tools:

- [NCBI BLAST+](http://blast.ncbi.nlm.nih.gov/Blast.cgi?CMD=Web&PAGE_TYPE=BlastDocs&DOC_TYPE=Download)
- [Diamond](http://ab.inf.uni-tuebingen.de/software/diamond/)
- [HMMer 3](http://hmmer.janelia.org/)
- [Muscle 3](http://www.drive5.com/muscle/)
- [GlimmerHMM](https://ccb.jhu.edu/software/glimmerhmm/)
- [CD-HIT](http://weizhongli-lab.org/cd-hit/)
- [PySVG](http://codeboje.de/pysvg/)
- [JQuery SVG](http://keith-wood.name/svg.html)
- [JQuery DataTables](https://datatables.net/)
- [InCHlib](http://www.openscreen.cz/software/inchlib/home/)
- [vis.js](http://visjs.org/)
- [pplacer](https://github.com/matsen/pplacer)
- [GraPhlAn](https://huttenhower.sph.harvard.edu/graphlan/)


## plantiSMASH 2.0 contributors 

plantiSMASH version 2.0 is the product of a collaborative effort between:

- [Bioinformatics Group](http://www.wur.nl/en/Expertise-Services/Chair-groups/Plant-Sciences/Bioinformatics.htm), Wageningen University & Research
- [Department of Metabolic Biology](https://www.jic.ac.uk/staff/anne-osbourn/), John Innes Centre, Norwich
- [The Robert H. Smith Institute of Plant Sciences and Genetics in Agriculture](https://plantscience.agri.huji.ac.il/people/guy-polturak), Hebrew University of Jerusalem
- [DOE Joint Genome Institute](https://jgi.doe.gov/), Lawrence Berkeley National Labs
  
Supported by the Graduate School for Experimental Plant Sciences (EPS) and Vidi Grant VI.Vidi.213.183 from The Netherlands Organization for Scientific Research (NWO).

## plantiSMASH 1.0 contributors 

plantiSMASH version 1.0 was the product of a collaborative effort between:

- [Bioinformatics Group](http://www.wur.nl/en/Expertise-Services/Chair-groups/Plant-Sciences/Bioinformatics.htm), Wageningen University & Research  
- [Department of Informatics Engineering](http://if.unila.ac.id/), Lampung University  
- [Novo Nordisk Foundation Center for Biosustainability](http://www.biosustain.dtu.dk/), Technical University of Denmark  
- [Department of Metabolic Biology](https://www.jic.ac.uk/staff/anne-osbourn/), John Innes Centre, Norwich

Supported by the Graduate School for Experimental Plant Sciences (EPS),  
VENI Grant (#863.15.002) from The Netherlands Organization for Scientific Research (NWO),  
a Novo Nordisk Foundation Grant,  
UK Biotechnological and Biological Sciences Research Council (BBSRC) Institute Strategic Programme Grant  
"Understanding and Exploiting Plant and Microbial Metabolism" (BB/J004561/1),  
the John Innes Foundation,  
the joint Engineering and Physical Sciences Research Council/BBSRC-funded  
OpenPlant Synthetic Biology Research Centre grant BB/L014130/1,  
and a National Institutes of Health Genome to Natural Products Network award U101GM110699.

## How to cite 

If you have found plantiSMASH useful, please cite:

**plantiSMASH: automated identification, annotation and expression analysis of plant biosynthetic gene clusters.**  
Satria A. Kautsar, Hernando G Suarez Duran, Kai Blin, Anne Osbourn & Marnix H. Medema
Nucleic Acids Research, 45(W1), W55-W63. (2017) [https://doi.org/10.1093/nar/gkx305](https://doi.org/10.1093/nar/gkx305)