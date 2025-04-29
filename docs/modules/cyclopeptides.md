# Cyclopeptide BGC detection 

This module supports the detection of cyclopeptide BGCs in the presence of a BURP domain and repeat sequences. 

The Cyclopeptide detection module identifies biosynthetic gene clusters (BGCs) associated with cyclopeptide production in plants.
Detection is based on two main criteria:

- The presence of a BURP domain (a characteristic biosynthetic domain).

- The presence of internal amino acid repeats within coding sequences, suggesting the existence of cyclopeptide precursor peptides.

Once a candidate BGC is identified, the module performs the following steps:

1. Repeat Detection: Using a repeat-finding algorithm, the module scans the coding sequences (CDSs) inside the cluster for repeated amino acid motifs.

2. Pattern Matching: Detected repeats are matched against known cyclopeptide-related patterns where available, or reported as new motifs.

3. Filtering Logic: Only clusters containing both a BURP domain and at least one repeat with appropriate features are retained.

4. Result Summary: For each coding sequence with detected repeats, the module reports:

   - The identified repeat patterns.

   - The number of repeat instances.

   - The location and sequence coverage.

A visual highlight of the repeats inside the amino acid sequence.

The output includes a detailed view showing the repeat locations, pattern matches, and highlighted sequences.

![Cyclopeptide repeat](../assets/images/cyclopeptide_repeat.png)



