# Cluster types 

plantiSMASH uses some abbreviations internally and in outputs to refer to the different
types of secondary metabolite clusters detected.

Cluster rules and associated HMM profiles are available in the [plantiSMASH GitHub repository](https://github.com/plantismash/plantismash/). 

## Current Types

| Putative cluster type | Characterized by the presence of | Added | Last updated | Detection Rule Updates |
|-------|-------------|---------|---------|----------------------|
| **alkaloid** | Bet_v_1, Cu_amine_oxid, Str_synth, BBE, Orn_DAP_Arg_deC, Pyridoxal_deC enzymes. | 1.0 | 2.0 | **Added:** BBE, Orn_DAP_Arg_deC, Pyridoxal_deC |
| **lignan** | Dirigent enzyme. | 1.0 | 2.0 | No changes |
| **saccharide** | Glycosyl transferases (1,2,28), UDPGT, Glyco_hydro, Cellulose_synt enzymes. | 1.0 | 2.0 | **Added:** Glyco_hydro_1, Cellulose_synt |
| **terpene** | Terpene_synth, Prenyltrans, SQHop_cyclase, PRISE enzymes. | 1.0 | 2.0 | No changes |
| **polyketide** | AMP-binding and Chal_sti_synt enzymes. | 1.0 | 2.0 | **Now allows multiple detection rules:** AMP-binding + Thr_dehydrat_C OR AMP-binding + Chal_sti_synt_C/N |
| **fatty acid** | AMP-binding, Transferase. | 1.0 | 2.0 | **Added alternative detection rules:** FA_desaturase, FA_desaturase_2, FA_hydroxylase, CER1-like_C |
| **mate** | MatE enzymes. | 1.0 | 2.0 | No changes |
| **sesterpene** | Terpene_synth_C, polyprenyl_synt. | 1.0 | 2.0 | No changes |
| **strictosidine-like** | Str_synth, Pyridoxal_deC enzymes. | 1.0 | 2.0 | No changes |
| **phenolamide** | Transferase, Pyridoxal_deC enzymes or Transferase, Orn_DAP_Arg_deC, Orn_Arg_deC_N enzymes. | 1.0 | 2.0 | **Added alternative detection rules:** Orn_DAP_Arg_deC, Orn_Arg_deC_N |
| **cyclopeptide** | BURP enzymes and putative peptide precursor repeat sequence. | 2.0 | 2.0 | No changes |
| **plant*** | Minimum of 4 enzyme domains from the full list. | 1.0 | 2.0 | No changes |

*Putative / uncategorized plant biosynthetic cluster.

---

## **Deprecated or Merged Types**
| Putative cluster type | Characterized by the presence of | Added | Removed |
|-------|-------------|---------|---------|
| **putative** | Putative / uncategorized biosynthetic cluster. | 1.0 | 2.0 |
| **hybrid** | Biosynthetic cluster containing signature traces from both A and B secondary metabolite types. | 1.0 | 2.0 |

---
## Reference Links

For reference, you can find the detection rules for different plantiSMASH versions here:

- **Version 1 Rules:** [View on GitHub](https://github.com/plantismash/plantismash/releases/tag/1.0/antismash/generic_modules/hmm_detection/plants/cluster_rules.txt/)
- **Version 2 Rules:** [View on GitHub](https://github.com/plantismash/plantismash/releases/tag/2.0-beta2)


This glossary provides an overview of the secondary metabolite types detected by plantiSMASH. If you have any questions, refer to the documentation or reach out to the development team.

