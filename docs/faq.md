Frequently Asked Questions
--------------------------

### Can I run plantiSMASH locally as a stand-alone program?

Yes. A stand-alone version of plantiSMASH is available from the [download page](install.md).

### Why doesn't plantiSMASH detect my gene cluster?

Some gene clusters, such as cofactor biosynthesis gene clusters are not identified by plantiSMASH, as they are categorized as primary metabolism instead of secondary metabolism. If you are aware of a true secondary metabolite biosynthesis gene cluster that escapes detection by plantiSMASH, please contact us, and we will add the models necessary to detect it.

### Why are several genes upstream and downstream of gene clusters included, even though they do not seem to be part of the gene cluster?

In designing plantiSMASH, we tried to be very conservative in cutting gene cluster borders, leaving this to the expert eye of the user, as it is better to include extra genes than to leave out key genes.

### Why is my BGC not detected in full?

The BGC did not meet the cutoff as set by the cluster rules file set for the public webserver. The user can specify a different cutoff when running the program as a stand-alone program by manually editing the cluster rules file available on the GitHub repository. If you run into such an issue, contact us or open a ticket on GitHub.

### Can I also submit an unannotated genome sequence in FASTA format?

No. To enable us to operate the plantiSMASH web server with the resources available, users are expected to upload annotated Genbank-formatted or fasta files with gene/CDS annotations (i.e. fasta = gff3). Please first run your assembly on gene finding tools of your preference, such as [AUGUSTUS](https://bioinf.uni-greifswald.de/augustus/) or [MAKER](https://www.yandell-lab.org/software/maker.html) before submitting it into plantiSMASH.

### What is the privacy policy of plantiSMASH?

If you have any concerns about the sensitivity of your data, please use the [stand-alone version of our tool](install.md). While the site is kept as safe and secure as possible, the plantiSMASH public web service is provided as-is and with no warranty against data breaches or maintainer misconduct.

plantiSMASH collects information provided by you and may transfer it to third parties in the process of detecting BGCs. Job results are not password-protected, but they are stored at a randomly generated URL which cannot be easily found by third parties. Output files are removed periodically and without notice, but plantiSMASH maintains a record of the parameters used to submit jobs indefinitely. plantiSMASH, its affiliates, and maintainers reserve the right to use the data submitted to plantiSMASH in accordance with EU regulations.
