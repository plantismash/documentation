Frequently Asked Questions
--------------------------

### Can I run antiSMASH locally as a stand-alone program?

Yes. A stand-alone version of plantiSMASH is available from the [download page](install.md).

### Why doesn't plantiSMASH detect my gene cluster?

Some gene clusters, such as cofactor biosynthesis gene clusters are not identified by plantiSMASH, as they are categorized as primary metabolism instead of secondary metabolism. If you are aware of a true secondary metabolite biosynthesis gene cluster that escapes detection by antiSMASH, please contact us, and we will add the models necessary to detect it.

### Why are several genes upstream and downstream of gene clusters included, even though they do not seem to be part of the gene cluster?

In designing plantiSMASH, we tried to be very conservative in cutting gene cluster borders, leaving this to the expert eye of the user, as it is better to show some extra genes than to leave out key genes.

### Why is my BGC not detected in full?

The user can specify a different cutoff when running the program as a stand-alone program, by manually editing the cluster rules file, avaialble on the gitHub repository. If you run into such an issue, contact us or open a ticket on GitHub.

### Can I also submit an unannotated genome sequence in FASTA format?

To enable us to operate the plantiSMASH webserver with the resources available, users are expected to upload annotated Genbank-formatted or fasta files with gene/CDS annotations (i.e. fasta = gff3). Please first run your assembly on gene finding tools of your preference, such as [AUGUSTUS](https://bioinf.uni-greifswald.de/augustus/) or [MAKER](https://www.yandell-lab.org/software/maker.html) before submitting it into plantiSMASH.

### What is the privacy policy of plantiSMASH concerning my sequence data?

We keep this site and the data that it analyses as safe and secure as possible. The randomly generated URL ensures that your data cannot easily be found by third parties. Your output files will be periodically deleted from our server. However, sending your data to the web site is at your own risk. If you are concerned about the sensitivity of your data, please use the stand-alone version of our tool.
