# Cluster types 

plantiSMASH uses some abbreviations internally and in outputs to refer to the different
types of secondary metabolite clusters detected.

Cluster rules and associated HMM profiles are available in the [plantiSMASH GitHub repository](https://github.com/plantismash/plantismash/). 


## Supported Cluster Types

For an overview of the supported cluster types across versions you can check the [changelog](./changelog/2.0.md). 


| Cluster Type         | Min. Generic Domains (v1 → v2) | Special Domains (v1 → v2)                                        | Version Added | Rule Changes |
|----------------------|-------------------------------|------------------------------------------------------------------|----------------|---------------|
| **plant***            | 4 → 4                         | – → –                                                            | v1             | **Expanded generic domain list**: added `NAD_binding_4`, `FAE1_CUT1_RppA`, `HAD_RAM2_N`, `Orn_DAP_Arg_deC`, `Pyridoxal_deC`, `BBE`, `FA_hydroxylase`, `CER1-like_C`, `ECH_2`, `Oxidored_FMN`, `3Beta_HSD`, `ADH_N`, `ADH_N_2`, `Abhydrolase_3`, `Aldo_ket_red`, `Methyltransf_11`, `TPMT`, `DAHP_synth_1`, `DAHP_synth_2` |
| **terpene**          | 3 → 3                         | Same (multi-domain list)                                         | v1             | No changes |
| **saccharide**       | 3 → 3                         | `Glycos_transf_1/2/28`, `UDPGT`, `UDPGT_2` → + `Glyco_hydro_1`, `Cellulose_synt` | v1 | **Expanded special domains** |
| **lignan**           | 3 → 3                         | `Dirigent` → `Dirigent`                                          | v1             | No changes |
| **alkaloid**         | 3 → 3                         | `Bet_v_1`, `Cu_amine_oxid`, `Str_synth` → + `BBE`, `Orn_DAP_Arg_deC`, `Pyridoxal_deC` | v1 | **Expanded rule logic** (OR logic) |
| **polyketide**       | 3 → 3                         | `Chal_sti_synt_C`, `Chal_sti_synt_N` → + `AMP-binding`, `Thr_dehydrat_C` (alternative rules) | v1 | **Multiple alternative rules added** |
| **sesterterpene**    | 2 → 2                         | Same                                                              | v1             | No changes |
| **cyclopeptide**     | – → –                         | `BURP`                                                            | v2             | **New rule** |
| **fatty_acid**       | – → 3                         | – → `FA_desaturase`, `FA_desaturase_2`, `FA_hydroxylase`, `CER1-like_C`, `Transferase`, `ECH_2`, `AMP-binding` | v2 | **New rule** |
| **strictosidine_like** | – → 2                       | – → `Str_synth`, `Pyridoxal_deC`                                  | v2             | **New rule** |
| **phenolamide**      | – → 2                         | – → `Transferase`, `Pyridoxal_deC`, `Orn_DAP_Arg_deC`, `Orn_Arg_deC_N` | v2 | **New rule with OR logic** |
| **MatE**             | – → 3                         | – → `MatE`                                                        | v2             | **New rule** |
| **transporter**      | – → 3                         | – → `LTP_2`, `ABC2_membrane`, `ABC_tran`                          | v2             | **New rule** |



*Putative / uncategorized plant biosynthetic cluster.

-- 

## Generic Domains Used in Version 1 vs Version 2

### Generic Domains in Version 1

`cMT`, `nMT`, `oMT`, `adh_short`, `Chal_sti_synt_C`, `Chal_sti_synt_N`, `COesterase`, `UDPGT`, `Glyco_transf_28`, `Glycos_transf_1`, `Glycos_transf_2`, `Lycopene_cycl`, `NAD_binding_1`, `p450`, `SQHop_cyclase_C`, `SQHop_cyclase_N`, `Prenyltrans`, `Terpene_synth_C`, `Terpene_synth`, `Transferase`, `Aminotran_1_2`, `AMP-binding`, `DIOX_N`, `Dirigent`, `Bet_v_1`, `Cu_amine_oxid`, `Str_synth`, `Trp_syntA`, `His_biosynth`, `adh_short_C2`, `Peptidase_S10`, `Prenyltransf`, `Epimerase`, `2OG-FeII_Oxy`, `Aminotran_3`, `Methyltransf_2`, `Methyltransf_3`, `Methyltransf_7`, `PRISE`, `Cellulose_synt`, `Chalcone`, `ERG4_ERG24`, `FA_desaturase`, `FA_desaturase_2`, `Methyltransf_11`, `polyprenyl_synt`, `SE`, `SQS_PSY`, `TPMT`, `UbiA`, `Lipoxygenase`, `Lyase_aromatic`, `HMGL-like`, `Chalcone_3`, `Chalcone_2`, `Acetyltransf_1`, `UDPGT_2`, `GMC_oxred_N`, `GMC_oxred_C`, `Amino_oxidase`, `DAHP_synth_1`, `DAHP_synth_2`

### Additional Generic Domains in Version 2

`NAD_binding_4`, `FAE1_CUT1_RppA`, `HAD_RAM2_N`, `Orn_DAP_Arg_deC`, `Pyridoxal_deC`, `BBE`, `FA_hydroxylase`, `CER1-like_C`, `ECH_2`, `Oxidored_FMN`, `3Beta_HSD`, `ADH_N`, `ADH_N_2`, `Abhydrolase_3`, `Aldo_ket_red`


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

