# Network Pharmacology Analysis of EGCG, Tanshinone I, and E-Guggulsterone Against Breast Cancer
## 1. Research Background and Rationale
Breast cancer is a molecularly heterogeneous disease involving multiple genetic alterations and interconnected signaling pathways. Tumor cells can activate alternative survival and growth mechanisms that support proliferation, apoptosis resistance, invasion, and resistance to endocrine or targeted therapies [1]. Network pharmacology is therefore suitable for investigating breast cancer because it integrates compound targets, disease-associated genes, protein–protein interactions, and enriched biological pathways within a unified analytical framework [2].

EGCG, tanshinone I, and E-guggulsterone were selected because they represent different natural-product chemical classes and have shown anticancer activity in preclinical breast-cancer models. EGCG induced apoptosis in T47D cells through modulation of the PI3K–AKT pathway and suppression of telomerase-related expression [3]. Tanshinone I induced apoptosis in both estrogen receptor-positive MCF-7 and estrogen receptor-negative MDA-MB-231 cells [4] and suppressed tumor growth, invasion, and angiogenesis in MDA-MB-231 models [5]. E-guggulsterone corresponds to the E or trans stereoisomer of guggulsterone; in MCF-7 cells, trans-guggulsterone suppressed MAPK/AP-1 signaling, MMP-9 expression, and cellular invasion [6]. 

Together, these findings provide a biological basis for comparing the predicted targets and pathways of the three compounds in a single network-pharmacology analysis.
## 2. Research Objective
The objective of this analysis was to identify possible protein targets and biological pathways through which EGCG, Tanshinone I, and E-Guggulsterone may act against breast cancer, and to determine the central proteins that may be considered for further analysis such as molecular docking or experimental validation.
## 3. Methodology
![Figure 1. Workflow](/workflow.png "Workflow")
 
## 4. Results and Interpretation
### 4.1 Core protein-protein interaction network
 ![Figure 2. Core protein-protein interaction network generated from the candidate breast-cancer targets. Node color appears to represent relative topological importance, while edges show protein-protein associations. ](/Map_core_networ.png "Map of the core network")

Based on the visual color scale, STAT3, CTNNB1, EGFR, SRC, and AKT1 appear among the most central nodes. These proteins connect major cancer processes. EGFR, SRC, PIK3CA, AKT1, and PTEN form a growth and survival signaling group. MAPK3 and MAPK14 connect mitogen and stress-response pathways. ESR1, PPARG, and EP300 connect hormone-receptor and transcriptional regulation. TNF, IL18, STAT1, STAT3, and PTGS2 represent inflammatory or immune signaling. HIF1A and MMP9 relate to hypoxia, angiogenesis, tissue invasion, and metastasis, while BCL2 is involved in resistance to apoptosis.
### 4.2 Identification of Hub Genes in the Core Network
| Gene     | Betweenness Centrality | Closeness Centrality | Degree |
| -------- | ---------------------: | -------------------: | -----: |
| AKT1     |            0.022219717 |          1.000000000 |     19 |
| STAT3    |            0.022219717 |          1.000000000 |     19 |
| SRC      |            0.021144726 |          0.950000000 |     18 |
| CTNNB1   |            0.018687885 |          0.950000000 |     18 |
| EGFR     |            0.016352988 |          0.904761905 |     17 |
| ESR1     |            0.014972368 |          0.904761905 |     17 |
| IL1B     |            0.013755883 |          0.904761905 |     17 |
| HIF1A    |            0.011396509 |          0.904761905 |     17 |
| STAT1    |            0.014348479 |          0.863636364 |     16 |
| BCL2     |            0.010691398 |          0.863636364 |     16 |
| MAPK3    |            0.008233298 |          0.826086957 |     15 |
| MMP9     |            0.005026352 |          0.826086957 |     15 |
| PTEN     |            0.007542046 |          0.791666667 |     14 |
| PPARG    |            0.006173093 |          0.791666667 |     14 |
| TNF      |            0.004044877 |          0.791666667 |     14 |
| HSP90AA1 |            0.006883348 |          0.760000000 |     13 |
| MAPK14   |            0.004829603 |          0.760000000 |     13 |
| PTGS2    |            0.003139837 |          0.760000000 |     13 |
| EP300    |            0.003812459 |          0.730769231 |     12 |
| PIK3CA   |            0.000899685 |          0.655172414 |      9 |

The protein–protein interaction network contained 20 genes and 153 interactions, showing a highly connected network. Centrality analysis identified AKT1 and STAT3 as the main hub genes, as both had the highest degree, betweenness centrality, and closeness centrality values. SRC and CTNNB1 were also highly central, followed by EGFR, ESR1, IL1B, and HIF1A. These genes may act as important connection points between several breast cancer-related processes, including cell proliferation, survival, hormone signaling, inflammation, and response to cellular stress.

Overall, the results suggest that the possible effects of EGCG, tanshinone I, and E-guggulsterone may involve multiple interconnected signaling pathways rather than a single molecular target. AKT1, STAT3, SRC, and CTNNB1 may therefore be considered the most important candidates for further analysis. However, centrality only shows the structural importance of a gene within the selected network and does not confirm direct compound–target binding or therapeutic activity.

### 4.3 Gene Ontology molecular-function enrichment
 
![Figure 3. Gene Ontology Molecular Function enrichment.](/GO_Molecular_Barplot.png "Go Barplot") 

The largest fold-enrichment value was observed for nitric-oxide synthase regulator activity. This means that this molecular function occurred much more frequently in the selected gene set than expected from the reference genome. However, an extreme fold-enrichment value can be produced by a small number of genes when the background category is small. Therefore, this term should not automatically be treated as the main mechanism without checking the number and identity of contributing genes.

The broader pattern is more informative. Enriched terms included transcription coactivator binding, nuclear estrogen receptor binding, transcription coregulator binding, nuclear receptor binding, protein phosphatase binding, protein kinase binding, chromatin binding, and ubiquitin-ligase binding. These functions match the core network, which contains ESR1, PPARG, EP300, STAT proteins, kinases, phosphatase-related regulators, and HSP90AA1. The result suggests that the candidate compounds may affect breast-cancer biology through regulation of signaling proteins and transcriptional complexes.

### 4.4 KEGG pathway enrichment

![Figure 4. KEGG pathway enrichment of the candidate targets.](/KEGG_barplot.png "KEGG pathway.") 

KEGG enrichment analysis showed that the core targets were mainly associated with interconnected pathways involved in hormonal signaling, growth-factor responses, immune regulation, hypoxia, and treatment resistance, particularly prolactin, estrogen, EGFR, HIF-1, TNF, and PD-L1/PD-1 signaling. These pathways largely converge on PI3K–AKT, MAPK, STAT, and HIF-1 signaling modules that contribute to breast-cancer progression and therapeutic response. Enrichment of prostate cancer and infection-related pathways likely reflects shared signaling proteins rather than disease-specific effects; therefore, interpretation should focus on the underlying molecular mechanisms rather than individual KEGG pathway labels.
### 4.5 Integrated compound-target-pathway network

![Figure 5. Integrated Cytoscape network connecting EGCG, Tanshinone I, E-Guggulsterone, selected targets, and enriched KEGG pathways.](/KEGG_enriched_core.png "KEGG pathways enriched in the core network")
 
The integrated network revealed that EGCG, tanshinone I, and E-guggulsterone converge on a limited number of highly connected targets that link the compounds to multiple cancer-related pathways. MAPK3 and MAPK14 formed important connections between growth-factor, inflammatory, stress-response, apoptosis, and immune-related pathways, whereas EP300 linked several transcriptional regulatory pathways, including JAK–STAT and Wnt signaling. PIK3CA, MET, CYP19A1, and PPARG further connected the network with cell-survival signaling, receptor tyrosine kinase activity, estrogen biosynthesis, and nuclear-receptor regulation. This network structure supports a multi-target model in which the three compounds may affect complementary but overlapping regulatory processes in breast cancer. 
## 5. Conclusion
The network pharmacology analysis suggests that EGCG, tanshinone I, and E-guggulsterone may influence breast cancer through interconnected hormonal, growth-factor, inflammatory, hypoxia, and survival-related pathways. Among the predicted targets, AKT1, STAT3, SRC, CTNNB1, EGFR, ESR1, HIF1A, MAPK3, and MAPK14 emerged as key proteins implicated in breast-cancer pathophysiology, particularly in the regulation of cell proliferation, survival, treatment resistance, immune signaling, and tumor progression. Overall, the findings support a multi-target and multi-pathway mechanism, although experimental validation is still required to confirm the predicted biological effects.
## 6. References
1.	The Cancer Genome Atlas Network. Comprehensive molecular portraits of human breast tumours. Nature. 2012;490:61–70. doi:10.1038/nature11412. 
2.	Yellapu NK, Pei D, Nissen E, Thompson JA, Koestler DC. Comprehensive exploration of JQ1 and GSK2801 targets in breast cancer using network pharmacology and molecular modeling approaches. Computational and Structural Biotechnology Journal. 2023;21:3224–3233. doi:10.1016/j.csbj.2023.06.003. 
3.	Moradzadeh M, Hosseini A, Erfanian S, Rezaei H. Epigallocatechin-3-gallate promotes apoptosis in human breast cancer T47D cells through down-regulation of PI3K/AKT and telomerase. Pharmacological Reports. 2017;69(5):924–928. doi:10.1016/j.pharep.2017.04.008. 
4.	Nizamutdinova IT, Lee GW, Son KH, et al. Tanshinone I effectively induces apoptosis in estrogen receptor-positive MCF-7 and estrogen receptor-negative MDA-MB-231 breast cancer cells. International Journal of Oncology. 2008;33(3):485–491. doi:10.3892/ijo_00000031. 
5.	Nizamutdinova IT, Lee GW, Lee JS, et al. Tanshinone I suppresses growth and invasion of human breast cancer cells, MDA-MB-231, through regulation of adhesion molecules. Carcinogenesis. 2008;29(10):1885–1892. doi:10.1093/carcin/bgn151. 
6.	Noh EM, Chung EY, Youn HJ, et al. Cis-guggulsterone inhibits the IKK/NF-κB pathway, whereas trans-guggulsterone inhibits MAPK/AP-1 in MCF-7 breast cancer cells: guggulsterone regulates MMP-9 expression in an isomer-specific manner. International Journal of Molecular Medicine. 2013;31(2):393–399. doi:10.3892/ijmm.2012.1214.
