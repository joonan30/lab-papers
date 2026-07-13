# Cntnap2-dependent molecular networks in autism spectrum disorder revealed through an integrative multi-omics analysis

## Bibliographic Information
- **Authors**: Wooyoung Eric Jang, Ji Hwan Park (co-first authors, equal contribution), Gaeun Park, Geul Bang, Chan Hyun Na, Jin Young Kim, Kwang-Youl Kim, Kwang Pyo Kim, Chan Young Shin, **Joon-Yong An (co-author, An Lab)**, Yong-Seok Lee, **Min-Sik Kim (corresponding author, mkkim@dgist.ac.kr)**
- **Journal / Year**: Molecular Psychiatry (2023) 28:810–821 (advance online publication October 17, 2022; received 2022-03-12, revised 2022-09-15, accepted 2022-09-26)
- **PMID / DOI**: PMID 36253443 / DOI 10.1038/s41380-022-01822-1 (PMCID PMC9908544)
- **Article Type**: Original research — an integrative multi-omics study across mouse, human, and organoid systems (proteometabolomics + transcriptome + lipidome + single-cell RNA-seq)

## One-Line Summary
This study integrates mass-spectrometry-based proteometabolomics of the medial prefrontal cortex (mPFC) in Cntnap2 knockout mice with multi-omics data from the prefrontal cortex of autism patients and single-cell data from CNTNAP2-mutant organoids, defining a Cntnap2-dependent ASD molecular network centered on excitatory neurons and organized around mitochondrial dysfunction, axonal impairment, and synaptic vesicle trafficking abnormalities.

## Research Summary
Autism spectrum disorder (ASD) is a representative neurodevelopmental disorder whose core symptoms are deficits in social communication, restricted interests, and repetitive behaviors, yet its pathophysiology remains poorly understood. Variants in the Contactin-associated protein-like 2 (CNTNAP2) gene have been repeatedly reported as genetic risk factors for ASD, and disruption of Cntnap2 expression in mice is known to be associated with ASD-like phenotypes (impaired neuronal migration, reduced mPFC neuronal density, altered synaptic plasticity, and excitation/inhibition imbalance). However, the actual molecular pathological mechanisms mediated by this gene have remained an open question.

This study aimed to define, in an integrative and cross-species manner, the molecular changes caused by Cntnap2 deficiency. To do so, the authors performed quantitative proteomics and targeted metabolomics (proteometabolomics) on the mouse mPFC to identify Cntnap2-associated molecular features, and then cross-integrated these features with publicly available multi-omics data (transcriptome, metabolome, lipidome) from the prefrontal cortex (PFC) of ASD patients and with single-cell RNA-seq data from CNTNAP2-mutant forebrain organoids.

The approach was as follows: (1) The authors confirmed that Cntnap2 KO mice showed significantly impaired preference for a conspecific in the three-chamber social preference test, validating the model's suitability as an ASD model. (2) In the mPFC, TMT-based quantitative proteomics (8,821 proteins) and targeted quantitative metabolomics (114 metabolites) were used to identify differentially expressed molecules. (3) These mouse molecular features were contrasted with the human ASD PFC transcriptome, metabolome, and lipidome to select "bona fide" ASD molecular processes shared between mouse and patients. (4) CNTNAP2-related ASD organoid single-cell data were reanalyzed to determine which cell types these processes were mainly associated with.

As key results, Cntnap2 deficiency broadly altered lipid metabolism (upregulated) as well as synaptic vesicle (SV) trafficking, the axonal compartment, myelin, and oxidative phosphorylation (OXPHOS) processes (downregulated). The molecules commonly detected in both mouse and human ASD samples were concentrated in SV function and neuronal axon development. In the organoid reanalysis, CNTNAP2 was differentially expressed in excitatory neurons (Ex) relative to controls, and cellular processes related to axonal structure, SV function, and OXPHOS were concentrated in excitatory neurons, suggesting that excitatory neurons are the core cell type of CNTNAP2-dependent ASD.

Integrating these findings, the authors constructed a Cntnap2-associated ASD molecular network model organized along three axes: (1) myelin/mitochondria, (2) synapse, and (3) neuronal projection. In conclusion, this study presents, through multidisciplinary integrated data, that interconnected molecular pathways—mitochondrial dysfunction, disruption of synaptic vesicle trafficking, and axonal/neuronal projection impairment—mediate Cntnap2-dependent ASD pathology.

## Methods & Technologies
- **Animal model**: Male Cntnap2⁻/⁻ mice (Jackson Laboratory Stock No. 017482) were bred to produce Cntnap2⁺/⁺ (WT), Cntnap2⁺/⁻ (heterozygous), and Cntnap2⁻/⁻ (homozygous KO). IACUC approved (SNU 171220-2-5).
- **Behavioral test**: Three-chamber social preference test (control n=15, Cntnap2 KO n=16). Interaction time with a conspecific (M) vs. an inanimate object (O) and a preference index were calculated. Two-way ANOVA, Sidak multiple comparisons, Welch's t-test.
- **Mouse proteomics**: mPFC (KO n=5, control n=5) protein extraction → trypsin digestion → 10-plex TMT labeling → reversed-phase LC fractionation → high-resolution Orbitrap MS (DDA mode). 8,821 proteins identified from a total of 107,644 non-redundant peptides.
- **Mouse targeted metabolomics**: mPFC (KO n=4, control n=5) metabolite extraction + internal standard (IS) spike → split into 2 aliquots. Aliquot 1 (amino acids and 21 biogenic amines): PITC labeling followed by LC–MS/MS. Aliquot 2 (40 acylcarnitines, 14 LPCs, 76 PCs, 15 SMs, hexoses): FIA-MS/MS, MRM mode. 114 of 188 targets quantified.
- **Integration of public human PFC data**:
  - Bulk RNA-seq (38 controls, 25 ASD): GEO GSE51264 & GSE59288 (Liu et al. 2016).
  - Untargeted metabolome (14 controls, 32 ASD PFC): Kurochkin et al. 2019.
  - Untargeted lipidome (403 controls, 32 ASD PFC): Mendeley dataset (m4dt3z685s/1) (Yu et al. 2020).
  - ASD organoid single-cell RNA-seq: forebrain organoids GEO GSE174569 (de Jong et al. 2021, CNTNAP2 mutant).
- **Bioinformatics / statistics**: Adjusted t-test p (Pt) and median-ratio test (Pf) were computed by permutation testing and combined via the Stouffer method (Pcom). Thresholds: DEPeptide Pt≤0.05 and Pf≤0.10; DEG Pt≤0.05 and Pf≤0.10 (per cell type Pt≤0.10 and Pf≤0.20); DEM/DEL Pcom≤0.05. Hierarchical GO (GOBP) analysis, PLS-DA (partial least squares discriminant analysis), Venn diagram, and pivot-overlap analysis.
- **Single-cell analysis pipeline**: Spatiotemporal mapping using VoxHunt (Allen Developing Mouse Brain Atlas in situ hybridization, referenced to embryonic E15.5 [P15]) → selection of 5,932 dorsal pallium (DPal) cells. Leiden clustering into 13 clusters → manual curation into 5 representative cell types. Per-cell-type DEG and functional enrichment analysis.
- **Network analysis**: Construction of a protein-protein interaction network based on STRING-DB (assessing hubness and connectivity), and creation of three molecular network models (myelin/mitochondria, synapse, neuronal projection) reflecting curated interactions.

## Key Genes / Proteins
- **Cntnap2 / CNTNAP2**: Neurexin-family neuronal cell-adhesion molecule (contactin-associated protein-like 2). The central ASD risk gene in this study; shows high hubness in excitatory neurons and is downregulated in KO and in ASD patients.
- **Synaptic vesicle (SV) trafficking**: Vamp2, Rab3a (key SV docking molecule), Rab35, Erc2, Nectin1, Chmp6/7, Sept6, Snap25, Syt1 — mostly downregulated in mouse and human excitatory neurons.
- **Mitochondria**: Mcu (mitochondrial Ca²⁺ influx and membrane potential maintenance), Etfdh (flavin dehydrogenase regulating OXPHOS complex II and fatty acid oxidation), Sod1/2, Bcl2l1.
- **Lipid/fatty-acid metabolic enzymes**: Aldh7a1, Acsbg1, Acsf2, Acadm, Acaa2 — upregulated in mouse and human ASD (mitochondrial lipid metabolism and β-oxidation).
- **Neuronal projection/actin cytoskeleton**: Pak3 (key regulator of the actin cytoskeleton), Gap43 (axon formation), Map2k2, Mapk1, Pip4k2b, Brk1, Wasf1, Rac3, Cdc42, Apc, Arpc3, Cfl2 — related to the MAPK/ERK, RAC/CDC42/PAK, and JNK pathways.
- **Overlapping SFARI ASD genes**: Gabrb3, Cntnap2, Trim32, Dpp3, Vamp2 — commonly downregulated in mouse and human.
- **Major differentially expressed metabolites (DEM)**: Glutamine (Gln, decreased), PC(38:0), PC(O-36:0), PC(O-42:2) (increased), SM(d18:1/24:0), SM(d18:1/20:2) (increased), hexoses (increased).

## Main Findings
- **Social behavior deficit**: Unlike controls, Cntnap2 KO mice did not show a significant preference for a conspecific (control M vs O ****p<0.0001; KO p=0.0634, non-significant), and their preference index was significantly lower (Welch's t-test *p=0.0441), confirming impaired social preference for a conspecific.
- **Proteome changes**: From 11,215 DEPeptides (4,938 up, 6,277 down), 844 DEPs were derived (378 up, 466 down). In GOBP (LV1), metabolic processes accounted for the largest fraction at 40.1%. Upregulated DEPs were concentrated in lipid metabolism (fatty-acid and phospholipid metabolism), while downregulated DEPs were concentrated in SV trafficking (SV cycle, Ca²⁺-regulated exocytosis, endocytosis) and the axonal compartment (neurofilament, myelin sheath, axon terminus, axon diameter regulation). Both up- and downregulated sets were significantly associated with OXPHOS.
- **Metabolome changes**: Among the 114 quantified metabolites, PLS-DA component 1 (LV1 11.74%) separated KO from control. Seven DEMs were identified (Gln decreased; 3 PCs, 2 SMs, and hexose increased).
- **Molecules shared between mouse and human ASD**: 7,413 genes were common with Liu 2016, of which 48 DEGs matched the direction of the mouse DEPs (12 up, 36 down). For metabolites, 73 were detected in both datasets; PC(38:0) and PC(O-42:2) were increased in both mouse KO and ASD patients. Of the 48 metabolites correlated between mouse and patients, 36 were significantly associated with SV function (synaptic vesicle/membrane/secretory vesicle) and neuronal axon (axon development, terminus, neuron projection). Five SFARI genes (Gabrb3, Cntnap2, Trim32, Dpp3, Vamp2) were commonly downregulated, and 12 upregulated genes were concentrated in mitochondrial lipid metabolism (β-oxidation).
- **Excitatory neurons as the core cell type**: In organoids, 13 clusters were resolved into 5 cell types (Ex 4,303; Int 153; RG 217; NPC 90; U 1,169). 1,177 cell-type-specific DEGs were identified (Ex 619, etc.). Ex-specific DEGs were enriched in axonal structure, SV function, and OXPHOS. CNTNAP2 differential expression (ASD vs control) was observed only in the Ex cluster (not in NPCs). Twenty-four Ex-specific genes resembling the mouse proteome formed a single connected network in which CNTNAP2 showed high hubness (p=0.0767).
- **Mitochondrial dysfunction**: Mitochondrial proteins such as Mcu, Etfdh, Acaa2, Acadm, Aldh7a1, and Acsf2 were altered in mouse and human ASD. Downregulation of Mcu is expected to cause abnormalities in mitochondrial membrane potential (MMP), while upregulation of Etfdh and OXPHOS complex II is inferred to increase lipid metabolism and electron transport activity. Lipid metabolic enzymes (Aldh7a1, Ascbg1, Acsf2, Acadm, Acaa2) were commonly increased.
- **SV trafficking disruption**: Vamp2, Cntnap2, Erc2, Rab3a, Nectin1, Rab35, Chmp6, Chmp7, Sept6, and others were downregulated in mouse and human excitatory neurons. Downregulation of the key SV docking molecule Rab3a suggests impaired SV docking.
- **Neuronal projection impairment**: Pak3, Gap43, PC(38:0), and PC(O-42:2) are involved in actin cytoskeleton regulation. Pak3 downregulation (related to long-term synaptic plasticity and learning) and Gap43 downregulation suggest inhibition of axon formation via the JNK pathway. MAPK/ERK inactivation leads to increased lipid (PC) metabolism.

## Applications
- Proteometabolomics of the Cntnap2-deficient mPFC can serve as a platform for comprehensively exploring the molecular changes of neurodevelopmental disorders.
- The cross-species integrative strategy linking mouse, human, and organoids provides a methodological framework for selecting "bona fide" ASD molecular processes while controlling for inter-species differences when translating animal-model results to the clinic.
- Specific lipids/metabolites such as SM(d18:1/24:0) and PC(O-36:0) are proposed as potential biomarker candidates for neurological disorders.

## Extensibility / Future Directions
- Follow-up validation is needed to determine whether the key genes of the mitochondrial, SV, myelin, and neuronal projection pathways identified in this study indeed play central roles in ASD models and patients (noted by the authors).
- Because the converting enzymes involved in the mechanism of lipid increase (e.g., PC-to-SM conversion) were not detected as DEPs, there is room for further study of the regulatory mechanisms of the relevant metabolic enzymes.
- The work can be extended to functional experiments and therapeutic target discovery targeting the excitatory-neuron-specific network.

## Disease Relevance
- Copy number variation, genomic inversion, single-nucleotide polymorphisms (SNPs), and complete loss of CNTNAP2 are associated with ASD and other neurological disorders. In its disease-association analysis, this study showed that Cntnap2 is more strongly involved in ASD pathophysiology than in other disorders such as schizophrenia.
- By presenting that interconnected molecular pathways—mitochondrial dysfunction, disruption of SV trafficking, and neuronal projection (axonal) impairment—mediate Cntnap2-dependent ASD pathology, the study contributes to understanding ASD pathology and to the discovery of therapeutic targets.

## Novelty vs. Prior Work
- Whereas prior Cntnap2 studies were limited to individual phenotypes (neuronal migration, synaptic plasticity, circuit development), this study applied proteometabolomics—combining mass-spectrometry-based proteomics with targeted metabolomics—to the mPFC to comprehensively quantify molecular changes.
- Cross-integrating the mouse omics with the human ASD PFC transcriptome, metabolome, and lipidome as well as with CNTNAP2-mutant organoid single-cell data enabled the identification of a cell-type-specific molecular network centered on excitatory neurons beyond inter-species differences—a novel contribution.
- The study presents Cntnap2-dependent ASD pathology in a multilayered manner through an integrated network model linking mitochondria, synapse, and neuronal projection.

## Data / Code Availability
- **Proteome data**: PRIDE database accession number **PXD031656**.
- **Reanalyzed public data**: human PFC RNA-seq GSE51264 and GSE59288; ASD organoid scRNA-seq GSE174569; human PFC lipidome Mendeley dataset (m4dt3z685s/1); human PFC metabolome (Kurochkin et al. 2019).
- Data needed to draw the conclusions are presented in the main text and Supplementary Materials (open access, CC BY 4.0).
- No separate analysis-code repository is specified in the paper.

## Keywords
Cntnap2/CNTNAP2, autism spectrum disorder (ASD), integrative multi-omics, proteometabolomics (TMT/MRM), medial prefrontal cortex (mPFC), synaptic vesicle trafficking, mitochondrial dysfunction, neuronal projection/axonal impairment, excitatory neurons, forebrain organoid single-cell RNA-seq
