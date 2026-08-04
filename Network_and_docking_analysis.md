# PR-Focused Network Pharmacology and Molecular Docking of Selected Flavonoids in Uterine Fibroids
## 1. Research Background and Rationale
Uterine fibroids are steroid-dependent benign tumors in which progesterone receptor (PR) signaling contributes to tumor growth and maintenance. Progesterone promotes cell proliferation and survival through direct transcriptional regulation and crosstalk with growth-factor and kinase pathways. It can also increase the expression of the anti-apoptotic protein BCL2 through PR binding to the BCL2 promoter. These findings support PR and its associated signaling network as relevant therapeutic targets in uterine fibroids (Kim & Sefton, 2012; Yin et al., 2007). 

The clinical activity of selective progesterone receptor modulators (SPRM) further supports PR as a therapeutic target. However, its use for uterine fibroids was restricted following reports of serious adverse effects. This safety concern highlights the need to explore alternative compounds capable of modulating PR-related pathways. Mifepristone was selected as the pharmacological comparator because it has demonstrated clinical effects on fibroid volume and symptoms, and has an experimentally determined PR-bound structure (Esteve et al., 2013; Raaijmakers et al., 2009).

## 2. Research Objective
This study aimed to identify PR-associated targets and biological pathways potentially modulated by seven selected flavonoids in uterine fibroids, determine key proteins within the integrated PR–compound network, and evaluate the binding potential of the flavonoids toward prioritized protein targets and different PR conformations using molecular docking.

## 3. Methodology
A PR-focused gene set was established from progesterone-related Gene Ontology annotations and literature-supported genes associated with progesterone signaling in uterine fibroids. Human protein targets of the seven selected flavonoids were predicted using SwissTargetPrediction and standardized to official gene symbols. Exact overlap with the PR-focused gene set identified only five unique proteins. Because this limited overlap was insufficient for meaningful PPI topology analysis, the PR-focused genes and compound-predicted targets were combined for exploratory network construction. Protein associations were obtained from STRING and analyzed in Cytoscape using Degree and Maximal Clique Centrality, while functional enrichment was performed using ShinyGO. Hub proteins were interpreted as central components of the combined network and not necessarily as direct targets of all compounds (Purnamasari et al., not published).

Molecular docking was conducted using SwissDock with the AutoDock Vina. Human wild-type X-ray structures were selected based on structural resolution and the availability of experimentally defined ligand-binding pockets. Redocking parameters were optimized by varying grid size and exhaustiveness, with RMSD <2.0 Å considered acceptable (Purnamasari et al., not published). Docking scores were reported in kcal/mol, with more negative values indicating more favorable predicted binding (Bugnon et al., 2024; Trott & Olson, 2010).
 
Figure 1. Workflow.
![Figure 1. Workflow](/small_project_workflow.png)

## 4. Results and Interpretation
### 4.1 Compound–PR-Focused Target Intersection

Table 1. Shared targets between selected flavonoids and the PR-focused uterine fibroid gene set

| Rank | Protein | MCC score | MCC rank | Degree | Degree rank |
| ---: | ------- | --------: | -------: | -----: | ----------: |
|    1 | SRC     |   1235935 |        1 |     49 |           3 |
|    1 | AKT1    |   1231978 |        2 |     49 |           3 |
|    3 | CTNNB1  |   1041697 |        3 |     57 |           1 |
|    4 | HIF1A   |    714838 |        4 |     43 |           5 |
|    5 | BCL2    |    650055 |        5 |     33 |          10 |
|    5 | EGFR    |    620413 |        6 |     50 |           2 |
|    5 | ESR1    |    605226 |        7 |     38 |           7 |
|    8 | MMP9    |    600146 |        8 |     30 |          11 |
|    8 | MAPK3   |    548758 |        9 |     34 |           9 |
|    8 | TNF     |    516800 |       10 |     36 |           8 |


Intersection of the SwissTargetPrediction results with the PR-focused gene set identified only five unique shared proteins: SRC, BCL2, CD38, CTNNB1, and AKT1. Because the exact intersection contained only five unique proteins, it was considered insufficient for reliable hub and clustering analyses. A combined network was therefore constructed from the PR-focused genes and compound-predicted targets to examine whether the two sets were connected through shared protein interactions and signaling pathways. Importantly, proteins identified as hubs in this network were regarded as central network connectors and not automatically classified as direct compound targets.
### 4.1 Identification of Hub Genes in the Core Network
 
Figure 2. Core protein-protein interaction network.
![Figure 2. Core protein-protein interaction network](/MCC_layout.png)

The integrated network identified SRC, AKT1, CTNNB1, HIF1A, and BCL2 as the five highest-ranked proteins using MCC. Degree analysis produced a similar core group, with CTNNB1 ranking first, followed by EGFR, SRC, AKT1, and HIF1A. The agreement between the two methods suggests that SRC, AKT1, and CTNNB1 occupy important positions connecting PR-related signaling with growth, survival, and fibrotic pathways. BCL2, EGFR, ESR1, MAPK3, TNF, and MMP9 also occupied central positions, linking hormonal regulation with proliferation, apoptosis, inflammation, hypoxia, and extracellular-matrix remodeling.

Table 2. Top hub proteins ranked by Maximal Clique Centrality (MCC) and Degree centrality in the combined PR–compound network

| Rank | Protein | MCC score | MCC rank | Degree | Degree rank |
| ---: | ------- | --------: | -------: | -----: | ----------: |
|    1 | SRC     |   1235935 |        1 |     49 |           3 |
|    1 | AKT1    |   1231978 |        2 |     49 |           3 |
|    3 | CTNNB1  |   1041697 |        3 |     57 |           1 |
|    4 | HIF1A   |    714838 |        4 |     43 |           5 |
|    5 | BCL2    |    650055 |        5 |     33 |          10 |
|    5 | EGFR    |    620413 |        6 |     50 |           2 |
|    5 | ESR1    |    605226 |        7 |     38 |           7 |
|    8 | MMP9    |    600146 |        8 |     30 |          11 |
|    8 | MAPK3   |    548758 |        9 |     34 |           9 |
|    8 | TNF     |    516800 |       10 |     36 |           8 |


### 4.3 Gene Ontology molecular-function enrichment
 
Figure 3. Gene Ontology Molecular Function enrichment. 
![Figure 3. Gene ontology molecular function enrichment](/go_mol.png)

The GO molecular-function analysis was dominated by transcription coregulator binding, kinase activator activity, phosphatase binding, kinase-regulator activity, and transcription-factor binding. This pattern suggests that the combined network is enriched in proteins that regulate signal transmission and transcription rather than proteins involved in a single enzymatic function. The simultaneous enrichment of kinase- and phosphatase-related terms supports extensive communication between PR-associated transcriptional regulation and intracellular kinase pathways, including SRC, AKT, MAPK, and PI3K signaling.

### 4.4 KEGG pathway enrichment
 
Figure 4. KEGG pathway enrichment of the candidate targets.
![Figure 4. KEGG pathway enrichment](/KEGG_shinygo_barplot.png)

These pathways largely converge on PI3K–AKT–MAPK and TGF-β-associated signaling modules that may contribute to leiomyoma-cell proliferation, apoptosis resistance, and fibrotic matrix accumulation (Purnamasari et al., not published). Enrichment of endocrine-resistance and cancer-related pathways likely reflects shared proteins such as SRC, AKT1, EGFR, CTNNB1, and MAPKs rather than disease-specific activity; therefore, interpretation should focus on the underlying molecular mechanisms relevant to uterine-fibroid pathophysiology rather than individual KEGG pathway labels.
4.5 Integrated compound-target-pathway network
 
Figure 5. Integrated compound–target–pathway network connecting seven selected flavonoids, central proteins, and uterine-fibroid-relevant signaling pathways. 
![Figure 5. Integrated compound-target-pathway network](/network_pharmacology.png)

The integrated Cytoscape network showed that the seven flavonoids were connected to overlapping groups of proteins, which subsequently converged on a limited number of biological pathways. SRC, AKT1, CTNNB1, BCL2, MAPK1/3, EGFR, and ESR1 formed a central signaling region connecting the compounds with PI3K–AKT, MAPK, mTOR, JAK–STAT, apoptosis, and hormone-related pathways. FN1, CAV1, TGFB1, MMP9, and PTGS2 extended this network toward focal adhesion, extracellular-matrix remodeling, inflammation, and angiogenesis. The network therefore supports a multi-target and multi-pathway model, in which structurally related flavonoids may influence different but interconnected components of PR-associated uterine fibroid biology. 

### 4.6 Selection of Proteins and Binding Pockets for Molecular Docking
SRC, BCL2, and AKT1 were prioritized by combining network centrality, compound–target overlap, PR-related evidence, and the availability of experimentally defined ligand-binding pockets. PR was included separately because it was the central biological focus of the study.

Table 3. Binding pockets and ligands selection

| Target | PDB structure | Selected chain | Resolution | Co-crystallized ligand |
| ------ | ------------- | -------------- | ---------- | ---------------------- |
| SRC    | 4MXO          | A              | 2.10 Å     | Bosutinib              |
| BCL2   | 6O0K          | A              | 1.62 Å     | Venetoclax             |
| PR     | 2W8Y          | A              | 1.80 Å     | Mifepristone           |
| PR     | 2OVH          | A              | 2.00 Å     | Asoprisnil             |


### 4.6 Molecular-Docking Results
Table 4. Molecular docking affinities (kcal/mol)  of selected flavonoids and reference ligands against SRC, BCL2, and progesterone receptor (PR) structures

| Ligand       | SRC 4MXO | BCL2 6O0K | PR 2W8Y | PR 2OVH |
| ------------ | -------: | --------: | ------: | ------: |
| EGCG         |     -3.9 |      -7.9 |    -9.2 |    -9.4 |
| Baicalein    |     -3.6 |      -7.3 |    -8.7 |    -8.5 |
| Fisetin      |     -3.4 |      -7.1 |    -8.8 |    -8.3 |
| Prunetin     |     -3.7 |      -7.2 |    -8.0 |    -8.9 |
| Formononetin |     -3.2 |      -7.0 |    -7.4 |    -8.1 |
| Biochanin A  |     -3.4 |      -6.8 |    -7.5 |    -8.1 |
| Irilone      |     -3.7 |      -7.3 |    -8.9 |    -9.0 |
| Mifepristone |     -4.0 |      -8.5 |   -11.0 |    -7.2 |
| Asoprisnil   |        - |         - |       - |   -10.7 |
| Bosutinib    |     -2.9 |         - |       - |       - |
| Venetoclax   |        - |      -8.8 |       - |       - |


The docking results indicated target- and conformation-dependent binding profiles. For BCL2, venetoclax showed the most favorable affinity (−8.8 kcal/mol), followed by mifepristone (−8.5 kcal/mol), while EGCG was the highest-ranked flavonoid (−7.9 kcal/mol). For PR, each reference ligand performed best in its corresponding receptor conformation: mifepristone in 2W8Y and asoprisnil in 2OVH, both at −10.7 kcal/mol. Among the flavonoids, EGCG and irilone showed the most consistent affinities across both PR structures.

In contrast, the SRC results were not considered reliable because bosutinib, the co-crystallized inhibitor, produced an unexpectedly weak score (−2.9 kcal/mol). This suggests that the SRC docking protocol requires further validation.

## 5. Conclusion
This study identified SRC, BCL2, CD38, CTNNB1, and AKT1 as shared targets of seven flavonoids and demonstrated convergence on hormone-related, PI3K–AKT, MAPK, TGF-β, and focal-adhesion pathways involved in cell survival, proliferation, and extracellular-matrix regulation. Among the flavonoids, validated PR docking indicated that EGCG and irilone had the most consistent predicted binding across PR conformations, with EGCG also showing favorable BCL2 binding. These findings identify EGCG and irilone as the leading candidates for further study. Biochemical and uterine fibroid cell-based experiments are required to confirm their predicted target interactions and biological effects.
## 6. References
1.	Bugnon, M., Röhrig, U. F., Goullieux, M., Perez, M. A. S., Daina, A., Michielin, O., & Zoete, V. (2024). SwissDock 2024: Major enhancements for small-molecule docking with Attracting Cavities and AutoDock Vina. Nucleic Acids Research, 52(W1), W324–W332. DOI: 10.1093/nar/gkae300.
2.	Esteve, J. L. C., Acosta, R., Pérez, Y., Rodríguez, B., Seigler, I., Sánchez, C., & Tomasi, G. (2013). Mifepristone versus placebo to treat uterine myoma: A double-blind, randomized clinical trial. International Journal of Women’s Health, 5, 361–369. DOI: 10.2147/IJWH.S42770.
3.	Purnamasari HY, et al. (2026). Unpublished Draft.
4.	Kim, J. J., & Sefton, E. C. (2012). The role of progesterone signaling in the pathogenesis of uterine leiomyoma. Molecular and Cellular Endocrinology, 358(2), 223–231. DOI: 10.1016/j.mce.2011.05.044.
5.	Raaijmakers, H. C. A., Versteegh, J. E., & Uitdehaag, J. C. M. (2009). The X-ray structure of RU486 bound to the progesterone receptor in a destabilized agonistic conformation. Journal of Biological Chemistry, 284(29), 19572–19579. DOI: 10.1074/jbc.M109.007872.
6.	Trott, O., & Olson, A. J. (2010). AutoDock Vina: Improving the speed and accuracy of docking with a new scoring function, efficient optimization, and multithreading. Journal of Computational Chemistry, 31(2), 455–461. DOI: 10.1002/jcc.21334.
7.	Yin, P., Lin, Z., Cheng, Y.-H., Marsh, E. E., Utsunomiya, H., Ishikawa, H., Xue, Q., Reierstad, S., Innes, J., Thung, S., Kim, J. J., Xu, E., & Bulun, S. E. (2007). Progesterone receptor regulates Bcl-2 gene expression through direct binding to its promoter region in uterine leiomyoma cells. The Journal of Clinical Endocrinology & Metabolism, 92(11), 4459–4466. DOI: 10.1210/jc.2007-0725.
