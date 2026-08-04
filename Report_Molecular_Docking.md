# Molecular Docking Analysis of EGCG, Tanshinone I, and (E)-Guggulsterone Targeting AKT1 in Breast Cancer

AKT1 was selected for molecular docking because it showed the highest centrality in the core PPI network, indicating an important position in the predicted compound–target network. 

| PDB ID   | Resolution | Mutation status | Co-crystallized ligand      | Binding site               | Assessment|
 -------- | ---------: | ---------: | ---------: | ---------: | ---------:|
| **4GV1** | **1.49 Å** | No mutation     | Capivasertib (AZD5363; 0XZ) | ATP-binding site           | **Selected:** highest structural resolution                                                 |
| 4EKL     |     2.00 Å | One mutation    | Ipatasertib (GDC-0068; 0RF) | ATP-binding site           | Not selected because it contains a mutation and has lower resolution than 4GV1              |
| 3O96     |     2.70 Å | No mutation     | Allosteric inhibitor (IQO)  | PH–kinase domain interface | Not selected because it represents an allosteric pocket and has lower structural resolution |

  
![AKT1 Binding pocket](/AKT1_pocket.png)
*Figure 1. Prediction of the highest-ranked binding pocket of AKT1 (PDB ID: 4GV1) using PrankWeb. The selected pocket was centered at coordinates x = −19.9544, y = 1.4124, and z = 12.3768.*


Capivasertib (AZD5363) was used as the co-crystallized reference inhibitor, rather than a natural ligand, because its experimental binding pose is available in the selected ATP-binding pocket. The original structural study also reported potent AKT inhibition and suppression of tumor growth in a breast-cancer xenograft model (Addie et al., 2013)

Table 1. Predicted binding affinities of capivasertib and the selected herbal compounds toward AKT1 (PDB ID: 4GV1)

| Model | Capivasertib |   EGCG | Tanshinone I | (E)-Guggulsterone |
| ----: | -----------: | -----: | -----------: | ----------------: |
|     1 |       -8.459 | -8.241 |   **-8.511** |            -5.518 |
|     2 |       -8.367 | -7.809 |       -8.409 |            -4.554 |
|     3 |       -8.326 | -7.747 |       -7.816 |            -4.233 |
|     4 |       -8.216 | -7.706 |       -7.543 |                 — |
|     5 |       -8.131 | -7.475 |       -7.334 |                 — |
|     6 |       -7.978 | -7.357 |       -7.206 |                 — |
|     7 |       -7.809 | -7.265 |       -7.061 |                 — |
|     8 |       -7.787 | -7.125 |       -6.927 |                 — |
|     9 |       -7.772 | -7.103 |       -6.900 |                 — |
|    10 |       -7.751 | -6.964 |       -6.793 |                 — |
|    11 |       -7.516 | -6.892 |       -6.728 |                 — |
|    12 |       -7.509 | -6.830 |       -6.636 |                 — |
|    13 |       -7.498 | -6.756 |       -6.546 |                 — |
|    14 |       -7.490 | -6.753 |       -6.410 |                 — |
|    15 |       -7.425 | -6.717 |       -6.218 |                 — |
|    16 |       -7.328 | -6.701 |       -6.102 |                 — |
|    17 |       -7.148 | -6.698 |       -6.093 |                 — |
|    18 |       -7.095 | -6.630 |       -6.059 |                 — |
|    19 |       -7.033 | -6.611 |       -5.972 |                 — |
|    20 |       -6.938 | -6.428 |       -5.910 |                 — |	

![Docking all compound](/docking_all.png)
*Figure 2. Figure 2. Docked poses of capivasertib, EGCG, tanshinone I, and (E)-guggulsterone within the ATP-binding pocket of AKT1 (PDB ID: 4GV1).*

Among the tested compounds, tanshinone I produced the most favorable best docking score at −8.511, which was close to the score of capivasertib at −8.459. EGCG also showed a favorable score of −8.241, suggesting a potentially compatible interaction with the AKT1 binding pocket. In contrast, (E)-guggulsterone had a considerably weaker best score of −5.518 and generated only three poses, indicating a less favorable fit within the selected pocket.

Overall, the results identify tanshinone I and EGCG as the most promising compounds for predicted interaction with AKT1, whereas (E)-guggulsterone showed lower compatibility with the selected binding site. Capivasertib also maintained consistently favorable scores across its highest-ranked poses, supporting its use as the reference inhibitor. Docking scores only represent computational predictions rather than direct measurements of binding strength. The findings should therefore be supported by analysis of amino-acid interactions, redocking validation, and further experimental studies

### Reference:
https://www.rcsb.org/structure/4GV1

Matt Addie, et al., Discovery of 4 Amino N [(1S) 1-(4-chlorophenyl)-3-hydroxypropyl]-1-(7H pyrrolo[2,3 d]pyrimidin-4-yl)piperidine-4-carboxamide (AZD5363), an Orally Bioavailable, Potent Inhibitor of Akt Kinases. J. Med. Chem. 14 March 2013; 56 (5): 2059–2073. https://doi.org/10.1021/jm301762v
