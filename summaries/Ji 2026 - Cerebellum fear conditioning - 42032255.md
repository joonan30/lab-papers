# Region- and cell type-specific changes in gene expression in the cerebellum after classical fear conditioning

## Bibliographic Information
- **Authors**: Jungeun Ji¹˒²·Jinhee Baek³˒⁴·Kyoung-Doo Hwang³˒⁴ (co-first authors, equal contribution), Seunghwan Choi⁵, Junko Kasuya⁶, Seung-Eon Roh⁷, Sang Jeong Kim³˒⁴˒⁸˒⁹, **Ted Abel⁶ (corresponding)**, **Joon-Yong An¹˒²˒⁵ (corresponding, joonan30@korea.ac.kr)**, **Yong-Seok Lee³˒⁴˒⁸˒⁹˒¹⁰ (corresponding, yongseok7@snu.ac.kr)**
  - Affiliations: ¹Integrated Biomedical Science, Korea University; ²BK21FOUR R&E Center, Korea University; ³Department of Physiology, Seoul National University College of Medicine; ⁴Department of Biomedical Sciences, Seoul National University College of Medicine; ⁵Department of Biosystems and Biomedical Sciences, College of Health Sciences, Korea University; ⁶Iowa Neuroscience Institute (University of Iowa); ⁷Department of Neuroscience, Johns Hopkins University; ⁸Neuroscience Research Institute, Seoul National University; ⁹Wide River Institute of Immunology, Seoul National University; ¹⁰Convergence Dementia Research Center, Seoul National University
  - A lab publication in which Prof. Joon-Yong An (An Lab) participated as a co-corresponding author
- **Journal / Year**: Communications Biology (Nature Portfolio) / 2026 (Article in Press; received 2025-04-17, accepted 2026-03-30)
- **PMID / DOI**: PMID 42032255 / DOI 10.1038/s42003-026-10034-0
- **Article Type**: Original research article (experimental study based on spatial transcriptomics and single-nucleus RNA-seq; also serving as a data resource)

## One-Line Summary
Using spatial transcriptomics and single-nucleus RNA-seq, this study shows that classical auditory fear conditioning strongly induces immediate-early genes (IEGs) in the deep cerebellar nuclei (DCN) and, in particular, selectively increases Grm5 (mGluR5) expression in Kit+ inhibitory neurons of the DCN, thereby presenting a region-, cell type-, and learning-stage-specific molecular landscape of non-motor learning in the cerebellum.

## Research Summary
The cerebellum has traditionally been regarded as a motor-control structure, but recent work has revealed its involvement in non-motor functions such as fear learning and social behavior. It has also become clear that, despite being composed of seemingly uniform cell types such as Purkinje cells and granule cells, the cerebellum exhibits considerable molecular, structural, and physiological heterogeneity. Nevertheless, how a non-motor associative learning task such as classical fear conditioning reorganizes the molecular architecture of the cerebellum has remained largely unknown. Whereas transcriptional and translational changes in cerebellar circuits have been well characterized in motor learning (e.g., vestibulo-ocular reflex, delay eyeblink conditioning), the molecular changes in the cerebellum driven by non-motor stimuli had remained an uncharted area.

To address this problem, the authors combined spatial transcriptomics (10X Visium) and single-nucleus RNA sequencing (snRNA-seq) in male mice to examine cerebellar gene expression across the learning stages of auditory fear conditioning. The experimental groups comprised three conditions: home-cage control (HC), 1 hour after fear conditioning (CD, the memory acquisition stage), and 1 hour after auditory memory (tone) retrieval (TN, the retrieval stage). Spatial transcriptomics was performed on coronal sections with one animal per condition; the integrated dataset comprised 9,780 spots and 18,779 genes, yielding 13 clusters that were classified into 7 regions (molecular layer, granule layer, Purkinje layer, DCN, white matter, fourth ventricle, and medulla).

As a key result, in the DCN — the sole output structure of the cerebellum — the immediate-early genes (IEGs) Fos, Junb, Egr1, and Npas4 were strongly upregulated upon fear learning (the DCN was the only region in which these IEGs were upregulated). Among these, Npas4 was the top upregulated gene in the CD-vs-HC comparison but showed no clear change in TN, suggesting selective involvement in acquisition rather than in memory retrieval. To confirm that the IEG changes reflected associative learning rather than merely the footshock response, freezing behavior, or sensory stimulation, the authors compared with control groups such as shock-only, tone-only, context retrieval, and novel exposure using fluorescence in situ hybridization (RNAscope); Fos and Egr1 were significantly increased only in the conditioned (CD) and retrieval (TN) groups. Among the three DCN subnuclei (FN, fastigial nucleus; IPN, interposed nucleus; DN, dentate nucleus), Fos increased in all three, whereas Egr1 increased only in IPN and DN, demonstrating subnucleus-specific molecular differentiation.

To resolve the cell-type level, the DCN was microdissected and subjected to snRNA-seq, identifying 6 cell types. Significant LRT DEGs were most numerous in oligodendrocytes (n=2,106), followed by inhibitory neurons (n=944) and astrocytes (n=728). Notably, in the retrieval (TN) versus conditioning (CD) comparison, oligodendrocytes showed overwhelmingly more DEGs than any other cell type, and these were strongly associated with myelination-related processes (with the key transcription factor Smad3), consistent with recent findings that new myelin formation supports the maintenance of remote fear memory. Furthermore, subdividing the inhibitory neurons into three subtypes according to the Kebschull et al. classification (Inh-Zfhx4, Inh-Kit, Inh-Piezo2) revealed that the Inh-Kit subtype showed the most DEGs in both CD and TN, and among these, Grm5 — encoding the metabotropic glutamate receptor mGluR5 — was the top upregulated gene at both the CD and TN stages. RNAscope verified that the increase in Grm5 occurred only in Kit+ inhibitory cells (not in Kit- cells), persisted into the retrieval stage, and was absent in the tone-only and context-retrieval groups, confirming that it was specific to associative learning. Thrb (thyroid hormone receptor β) was identified as the key regulatory transcription factor for Grm5 in Inh-Kit.

In conclusion, this study demonstrates that classical fear conditioning induces region-, cell type-, and learning-stage-specific transcriptomic changes in the cerebellum. The IEG induction in the DCN, together with the distinct transcriptional responses of glia (oligodendrocytes) and a specific inhibitory neuron population (Kit+), suggests molecular mechanisms by which the cerebellum contributes to non-motor associative learning beyond motor coordination, and provides both candidate molecules for future functional studies targeting these axes and a valuable data resource.

## Methods & Technologies
- **Animal model**: C57Bl/6N male wild-type mice (6–8 weeks old, Orient Bio). Approved by the Seoul National University IACUC (SNU-221014-3). 12-hour light/dark cycle.
- **Behavioral paradigm (classical auditory fear conditioning)**: After a 2-minute exploration period, 5 presentations of a CS (30 s, 2800 Hz, 79 dB pure tone) were paired with a US (2 s, 0.5 mA footshock) in a co-terminating manner, with a 30 s inter-trial interval. Control groups used shock-only (shock without tone) and tone-only (tone without shock). The retrieval test presented the pure tone 2–3 times in a novel chamber (cylinder) 24 hours later (tone retrieval); context retrieval consisted of re-exposure to the original chamber for 180 s; novel exposure involved exposure to the retrieval chamber without tone presentation.
- **Spatial transcriptomics**: 10X Genomics Visium. Fresh-frozen → OCT-embedded → 10 μm sections (RIN>7) → methanol fixation and H&E staining → library preparation. Illumina Novaseq 6000 (S1 reagent, 120M reads per library, dual indexing). Spot diameter 55 μm, center-to-center distance 100 μm, approximately 1–10 cells per spot.
  - Pipeline: Space Ranger v1.3.1 (aligned to mm10) → Scanpy v1.10.0 → Scrublet v0.2.3 (doublet removal), Gm42418 removal, exclusion of spots with >35% mitochondrial content → scVI v1.1.2 (batch correction, top 2,000 HVGs, Seurat v3 flavor) → Squidpy v1.2.2 (spatial connectivity) → Leiden clustering (resolution 0.8) on a combined graph weighting gene-expression connectivity 0.8 + spatial connectivity 0.2.
  - Region annotation: cell2location v0.1.3 mapping of Allen Brain Cell Atlas reference scRNA-seq, N_cells_per_location=6, detection alpha=20, 30,000 epochs. After 99th-percentile binarization, cluster-wise annotation of the cell type with the highest OR by Fisher's exact test. Manual correction using Allen Brain Atlas ISH references.
- **Single-nucleus RNA-seq (snRNA-seq)**: 30 minutes after the behavioral test, the DCN was microdissected from 200–300 μm coronal sections using a vibratome (VT1200S). Pipeline: cellranger v7.1.10 (mm10) → Scanpy v1.10.0 → Scrublet (doublets), Gm42418 removal, exclusion of nuclei with <200 or >8,000 genes, >60,000 UMIs, or >20% mitochondrial content → scVI v1.1.2 → Leiden clustering (resolution 1) and manual annotation.
- **Differentially expressed gene (DEG) analysis**:
  - Spatial transcriptomics: **DESeq2 v1.40.1** pseudo-bulk approach. LRT (likelihood ratio test) for overall significance, with pairwise comparisons of CD vs HC, TN vs HC, and TN vs CD. For Purkinje subregions, 2 pseudo-replicates were generated with 100 iterations (criterion: adj.P<0.05 and log2FC>±0.1 in ≥80% of iterations); for the cerebellar regions, 3 pseudo-replicates with a single analysis.
  - snRNA-seq: **MAST v1.28.0**, with the zlm function and a Hurdle model (cellular detection rate as covariate). Only genes expressed in >5% of cells per cell type were included. adj.P<0.05, log2FC>±0.1.
- **Pathway enrichment analysis**: clusterProfiler v4.10.0 (GO biological process), Benjamini-Hochberg correction P<0.05.
- **Transcription factor (TF) activity analysis**: pySCENIC v0.12.1, GRNBoost2 for TF-target adjacency, RcisTarget (mm10 motif-ranking DB) AUC enrichment scores, one-sided Wilcoxon rank-sum test on regulon activity scores (RAS), Bonferroni correction adj.P<0.01.
- **Validation (fluorescence in situ hybridization)**: RNAscope Multiplex Fluorescent Reagent Kit v2. 14 μm coronal sections (including DCN). Probes: Fos, Junb, Egr1, Npas4, Kit, Grm5, Gad2. ROI registration via the ABBA workflow, quantification with ImageJ and Qupath. Left and right DCN pooled for quantification.
- **Statistics**: Prism 9, mean ± S.E.M., two-tailed unpaired t-test, one-way repeated-measures ANOVA with post-hoc tests, significance at P<0.05.
- **References/schematics**: Purkinje subregion zebrin compartments were manually annotated based on the Allen Brain Atlas anatomical atlas (vermis = lobules 4/5, 6, simplex → zebrin-low; hemisphere = Crus I, II → zebrin-high). Schematics created with BioRender.

## Key Genes / Proteins
- **Fos (cFos)**: Immediate-early gene (IEG), marker of neural activity. Upregulated in all three DCN subnuclei during CD and TN; specific to associative learning.
- **Junb**: IEG. Upregulated in the DCN upon fear learning; consistent between spatial transcriptomics and ISH.
- **Egr1**: IEG. Upregulated in the DCN, but by subnucleus significantly increased only in IPN and DN (excluding FN).
- **Npas4**: Activity-dependent IEG. Top upregulated gene in CD (acquisition), unchanged in TN (retrieval) → selective for memory acquisition.
- **Grm5 (mGluR5)**: Metabotropic glutamate receptor. Central finding of this study — top upregulated gene in DCN Kit+ inhibitory neurons (Inh-Kit) at both CD and TN, specific to associative learning. A key regulator of neuroplasticity and fear acquisition/extinction (fear acquisition and extinction are impaired in mGluR5 KO).
- **Kit**: Marker of the DCN inhibitory neuron subtype (Inh-Kit). Partially overlaps with glycine/GABA co-releasing interneurons.
- **Gad2**: Marker of inhibitory (GABAergic) neurons. The Kit+/Gad2+ ratio differs across DCN subnuclei.
- **Zfhx4, Piezo2**: Markers of the other inhibitory neuron subtypes (Inh-Zfhx4, Inh-Piezo2) (Kebschull classification).
- **Smad3**: Transcription factor that regulates the timing of central nervous system myelination through TGF-β signaling. The most active TF in TN-stage oligodendrocytes; a candidate regulator of memory retrieval.
- **Thrb**: Thyroid hormone receptor β transcription factor. Identified as the key upstream regulator of Grm5 in Inh-Kit. Essential for normal brain development.
- **Aldoc (zebrin II) / Nptn**: Markers of the zebrin-high / zebrin-low bands, respectively. Correspond to the transcriptionally defined, established Purkinje zebrin compartments.
- **Plcb4**: (Introduction) Marker of a Purkinje cell subpopulation that undergoes transcriptional plasticity during motor learning, located mainly in zebrin-low regions.
- **Region markers (validation of spatial transcriptomics annotation)**: Spp1 (DCN), Aqp1 (fourth ventricle), Gabra6 (granule layer), Sncg / Lypd6 / Ppp1r17 (Purkinje layer), Mbp (white matter).
- **CD-upregulated memory/cognition-related DEGs**: Calb1, Egr1, Npas4, S100b, Slc6a1.
- **Key oligodendrocyte DEGs**: Fkbp5, Sgk1, Ptgds, Slc6a1 (upregulated), Cdh2, Mob3b, etc.

## Main Findings
- Integrated cerebellar spatial transcriptomics dataset: 9,780 spots · 18,779 genes · 13 clusters → classified into 7 regions. Region-wise cell composition distributions were similar across the three conditions (fear conditioning did not alter overall regional composition).
- **The DCN was the only cerebellar region in which the IEGs (Fos, Junb, Egr1, Npas4) were upregulated.** Fos, Junb, and Egr1 were the most strongly upregulated DEGs at both the CD and TN stages.
- **Npas4** was the top upregulated gene in CD vs HC but unchanged in TN vs HC → specific to acquisition.
- ISH validation: Fos and Egr1 increased significantly only in the CD and TN groups and did not increase in the shock-only, tone-only, context-retrieval, or novel-exposure control groups → involvement in associative learning.
- DCN subnucleus differentiation: **Fos** increased in all three subnuclei (FN, IPN, DN), whereas **Egr1** increased significantly only in IPN and DN.
- Purkinje layer heterogeneity: zebrin-low (mainly vermis) regions showed more DEGs upon fear learning than zebrin-high (hemisphere) regions → zebrin-low is more involved in fear-memory processing. The granule layer had relatively few DEGs, with fewer in TN vs HC than in CD vs HC.
- snRNA-seq (DCN) identified 6 cell types. **Number of LRT DEGs**: oligodendrocytes **n=2,106** > inhibitory neurons **n=944** > astrocytes **n=728**.
- **In the TN vs CD comparison, oligodendrocytes showed by far the most DEGs** → between memory consolidation and retrieval (with little change in other cell types), glial activity was prominent. GO enrichment: myelination-related (ensheathment of neurons, axon ensheathment). The most active TF was **Smad3**.
- Among the three DCN inhibitory neuron subtypes (Inh-Zfhx4/Inh-Kit/Inh-Piezo2), **Inh-Kit showed significantly the most DEGs in both CD vs HC and TN vs HC** (even though the cell proportions of Inh-Kit and Inh-Zfhx4 were similar).
- **Grm5 (mGluR5) was the top upregulated gene in Inh-Kit at both the CD and TN stages.** ISH confirmed an increase only in Kit+ inhibitory cells (not Kit- cells), persisting into the retrieval stage. No increase in the tone-only or context-retrieval groups → specific to associative learning.
- **Thrb** was identified as the key regulatory TF for Grm5 in Inh-Kit.
- Fear conditioning did not change the overall population size of inhibitory neurons or Kit+ inhibitory neurons (a transcriptional change, not a change in cell number).

## Applications
- Provides a **reference resource** offering the region-, cell type-, and learning-stage-specific transcriptomic landscape of cerebellar non-motor (fear) learning, serving as a basis for hypothesis generation in subsequent cerebellar cognitive/emotional studies.
- Presents the Grm5 (mGluR5), Kit+ inhibitory neuron, and oligodendrocyte myelination axes as **candidate molecular targets** for cerebellum-based fear-memory regulation.
- The multi-omics analysis pipeline combining spatial transcriptomics + snRNA-seq + ISH validation provides a methodological framework applicable to other brain regions and learning paradigms.

## Extensibility / Future Directions
- The tissue-collection timepoint (immediately after fear conditioning/retrieval) should be moved earlier to directly identify IEG-expressing cell types not captured by snRNA-seq (Visium captures tissue spots whereas snRNA-seq captures nuclear RNA, so at the 30-minute timepoint IEG mRNA has already moved to the cytoplasm).
- Characterizing the downstream circuits engaged by activated DCN neurons (e.g., FN–vlPAG, thalamo-cortical pathways).
- Functional verification of the contribution of mGluR5 to learning-dependent synaptic plasticity in Kit+ inhibitory neurons (currently a correlational observation).
- Comparing transcriptional changes of tone–footshock pairing versus footshock alone to distinguish pain processing versus associative learning in the vermis.
- Because the coronal sections were concentrated on lobules V and VI, changes in other posterior cerebellar regions such as lobule VIII remain unexplored → expansion needed.
- Given the exploratory nature of using one animal per condition (spatial transcriptomics), independent validation and larger sample sizes are needed.

## Disease Relevance
- Although not a direct disease-cohort study, fear memory and associative learning are underlying processes in **anxiety disorders, post-traumatic stress disorder (PTSD), and other fear-related psychiatric disorders**, and revealing the cerebellum's contribution to non-motor learning has implications for the circuit- and molecular-level understanding of these disorders.
- mGluR5 (Grm5) has been studied as a psychiatric therapeutic target as a key regulator of fear acquisition and extinction, and it is noted that Thrb (thyroid hormone receptor) deficiency is associated with intellectual and neurological disorders.

## Novelty vs. Prior Work
- Extends cerebellar transcriptional/translational plasticity — previously characterized mainly in motor learning — to **non-motor associative learning (fear conditioning)**, in one of the first integrated analyses combining spatial transcriptomics and snRNA-seq.
- Amid the debate over the reliability of cerebellar IEGs, specifies the **DCN as the region where IEGs are selectively induced** and presents subnucleus-specific (FN/IPN/DN) IEG differentiation.
- Dissects the heterogeneity of DCN inhibitory neurons at the subtype level (Inh-Kit), identifying the novel cell type–gene axis of **Grm5 upregulation in Kit+ inhibitory neurons** and validating its cell specificity and associative-learning specificity by ISH.
- Contrary to the prior assumption that glia–neuron interactions are greatest during memory retrieval, shows that **oligodendrocyte myelination** is prominent during the consolidation–retrieval interval, contrasting with conventional views.

## Data / Code Availability
- **Sequencing data**: NCBI GEO — spatial transcriptomics **GSE296375**, snRNA-seq **GSE296374**.
- **Numerical data**: Numerical values for the main figures are provided in Supplementary Data 1–6.
- **Additional data repository**: Korea BioData Station (K-BDS, https://kbds.re.kr), accession number **KAP241749**.
- **Code**: Analysis and visualization code is available at Zenodo (https://zenodo.org/records/15335138).

## Keywords
spatial transcriptomics, single-nucleus RNA-seq (snRNA-seq), cerebellum, deep cerebellar nuclei (DCN), classical fear conditioning, immediate-early genes (IEGs: Fos/Junb/Egr1/Npas4), Kit+ inhibitory neurons, Grm5/mGluR5, oligodendrocytes/myelination, Purkinje zebrin compartments
