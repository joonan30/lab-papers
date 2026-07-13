# Non-coding de novo mutations in chromatin interactions are implicated in autism spectrum disorder

## Bibliographic Information
- **Authors**: Il Bin Kim, Taeyeop Lee, Junehawk Lee (co-first authors, all three contributed equally) et al. Corresponding authors: Eunjoon Kim, Jung Kyoon Choi, Hee Jeong Yoo, Jeong Ho Lee. (First-author affiliations: KAIST Graduate School of Medical Science and Engineering / Department of Psychiatry, Hanyang University Guri Hospital; corresponding-author affiliations: KAIST, IBS, Seoul National University Bundang Hospital, etc.)
- **Journal / Year**: Molecular Psychiatry (2022) 27:4680–4694
- **PMID / DOI**: 35840799 / 10.1038/s41380-022-01697-2
- **Article Type**: Original Article — whole-genome sequencing (WGS) cohort analysis + an integrative framework combining 3D chromatin interactions + hiPSC functional validation (with the character of both a resource and a methodology paper)

## One-Line Summary
By analyzing the whole genomes of 242 Korean simplex families, this study demonstrates—through multi-cohort replication and patient-derived hiPSC experiments—that non-coding de novo mutations (DNMs) located within enhancer–promoter three-dimensional chromatin interactions perturb the expression of distal target genes and thereby contribute to early neurodevelopmental abnormalities and low intelligence quotient (IQ) in ASD.

## Research Summary
In autism spectrum disorder (ASD), de novo mutations (DNMs) in protein-coding regions are known to contribute to 10–30% of patients; however, the functional consequences of DNMs in the non-coding regions, which make up the majority of the genome, remain poorly characterized. Because obtaining robust associations for non-coding variants requires very large sample sizes, the authors propose an alternative approach that leverages three-dimensional (3D) chromatin interaction information to prioritize functional non-coding variants. Their hypothesis is that, because enhancers and promoters contact each other over long distances through chromatin looping to finely regulate gene expression, non-coding DNMs located within these interactions could simultaneously perturb distal target genes.

To this end, the researchers generated WGS data from 813 individuals across 242 Korean ASD simplex families, detected DNMs in the non-coding genome, and then used significant chromatin interactions defined from DNase-seq (distal enhancer DHS ↔ proximal promoter DHS; Pearson r ≥ 0.8; spanning distances of up to and beyond 500 kb) to prioritize the target genes affected by these variants. As a result, 215 non-coding DNMs in probands were linked to 363 target genes (compared with 67 DNMs → 91 genes in unaffected siblings), and this approach was consistently replicated in two independent cohorts—the Simons Simplex Collection (SSC; 1,902 probands / 1,902 siblings) and MSSNG (517 probands).

Critically, 76.9% of the target genes (279/363) were located distal to the variant and were therefore not the "nearest gene," and 63.1% (229/363) formed long-range chromatin interactions of 100–500 kb (versus 17.2% for the nearest-gene set; P = 6.7×10⁻¹⁸). Proband target genes significantly overlapped with genes differentially expressed (DE) in the ASD brain (P = 0.01), whereas the nearest genes (P = 0.87) and the sibling target genes (P = 0.09) did not. The target genes overlapped with spatiotemporal expression signatures of the fetal brain (amygdala, cortex, cerebellum, hippocampus) and, during fetal developmental periods, were expressed significantly more highly in probands than in siblings. In addition, these variants disrupted more transcription factor binding sites (TFBS) than in siblings (P = 0.018), and pathways of pregnancy (P = 5.5×10⁻⁷) and histone modification (WP:2369, P = 3.7×10⁻¹³) were enriched among the histologically relevant pathways.

Clinically, probands carrying both non-coding DNMs within chromatin interactions and deleterious coding DNMs had significantly lower IQ than those carrying only one of the two types or than those with an unknown cause (Korea P = 0.02, SSC P = 0.002; not significant in siblings, P = 0.67). A trend was observed in which a greater number of affected genes was associated with lower IQ, suggesting that a multi-hit of non-coding and coding variants contributes cooperatively to severe psychopathology such as comorbid intellectual disability. Finally, using hiPSCs and primitive neural stem cells (pNSCs) generated from two Korean ASD families (ID 992, ID 1289), the authors experimentally verified that 7 of 10 target genes had significantly perturbed expression in probands relative to their parents (most of these genes being distal to the variant, supporting the reality of long-range interactions). Taken together, the study concludes that non-coding DNMs within chromatin interactions cause early neurodevelopmental disturbances through the three-dimensional genome architecture and are thereby implicated in ASD risk.

## Methods & Technologies
- **Cohort/sample**: 242 Korean ASD simplex families, a total of 813 WGS samples (484 unaffected parents, 242 ASD probands, 87 unaffected siblings). Clinical assessment: ADI-R, Wechsler IQ (WISC), Leiter International Performance Scale IQ, SRS, SCQ.
- **Replication cohorts**: SSC (latest WGS; 1,902 probands + 1,902 siblings from 1,902 quartet families) and the MSSNG database (517 probands; downloaded 2017-09-11).
- **Sequencing**: Illumina HiSeq X, read depth 30×, aligned to GRCh38 (BWA-MEM). Batch effects across different vendors (Macrogen, Theragen) were examined, and coverage depth was corrected for.
- **De novo variant calling**: Candidates generated with GATK HaplotypeCaller + FreeBayes, then refined with TrioDenovo; in-house filtering (removal of low-complexity regions, phred-scale filters, allele frequency cutoffs, etc.). Calling conditions of DQ > 7 and AC ≤ 1 to correct for coverage bias.
- **Quality validation**: Random-sampling validation by Sanger sequencing — de novo SNV validation rate 95.4% (416/436), INDEL 93.9% (46/49).
- **Definition of chromatin interactions**: From DNase-seq DHS data, significant interactions were defined by the correlation between distal enhancer DHS and proximal promoter DHS (Pearson r ≥ 0.8, minimum distance of 500 kb), yielding a total of 517,159 significant interactions; variant–interaction overlap was determined with BEDTools pairToPair.
- **Interaction validation**: Using Hi-C data from neural progenitor cells (5 kb resolution, distance-normalized interaction frequency matrix), the interaction strengths were compared among the DHS-correlated set, the TSS-containing set, and the baseline set.
- **TFBS loss**: TFBS loss caused by DNMs was quantified using TRANSFAC position weight matrices + FIMO from the MEME SUITE (P < 1.0×10⁻⁴).
- **Definition of deleterious coding DNMs**: After feature selection with Boruta in R, loss-of-function/missense classification was performed using a combination of CADD, PolyPhen, PhyloP, PhastCons, SIFT, etc.; gene burden testing was done with denovolyzeR.
- **Spatiotemporal expression signatures**: BrainSpan RNA-seq, 15 brain regions × 10 developmental periods = 150 spatiotemporal signatures (based on z-score/meta z-score). The differentially expressed (DE) gene set was 2,666 genes from two prior studies.
- **Statistics/networks**: Random permutation tests (10,000 iterations), Fisher's exact test, Benjamini–Hochberg / Bonferroni multiple-testing correction, Mann–Whitney/Student's t-test, chi-square test; ClueGO (a Cytoscape plugin) for GO and WikiPathways pathway analysis; haploinsufficiency of recurrent target genes evaluated with the pLI score.
- **Chromatin state/visualization**: ChromHMM (core 15-state model) to predict transcriptional activity of the target regions, the 3D-genome Interaction Viewer and database (3DIV), and the H3K4me3 profiles from 3DIV.
- **Functional validation (hiPSC)**: From PBMCs of two ASD families (ID 992, ID 1289), hiPSCs were generated by lentiviral delivery (hOCT4, hSOX2, hKLF4, hMYC) (a total of 41 lines). Pluripotency was characterized (immunostaining for NANOG, SOX2, OCT4, SSEA4; teratoma formation), and after differentiation into primitive neural stem cells (pNSCs), target-gene expression was quantified by qPCR (2^-ΔΔCt).

## Key Genes / Proteins
- **CDK5RAP2**: Function in microtubule formation at the centrosome during embryogenesis; reduced expression is associated with centrosomal/nuclear abnormalities and microcephaly. (Reduced expression validated in the ID992 proband.)
- **ARHGEF2**: Determines mitotic spindle orientation; homozygous frameshift variants cause intellectual disability and midbrain–hindbrain malformation. (Reduced expression in ID992.)
- **CTNNA2 (αN-catenin)**: Expressed in the cortex during development; loss of function causes defects in dendritic spine morphogenesis and axonal projection, and biallelic loss causes cortical neuronal migration defects. (Reduced expression in ID1289.)
- **GRB10**: An imprinted gene (paternally expressed), mediating negative feedback of mTORC1 signaling; associated with ASD and regulates the synaptic excitation/inhibition ratio. (Reduced expression in ID1289.)
- **IKZF1**: Promotes early cortical neuronal differentiation, highly expressed early in development and decreasing over time. (Reduced expression in ID1289.)
- **PDE3B**: Mediates hypothalamic leptin signaling (PI3K-PDE3B-cAMP) and is related to synaptic plasticity. (Reduced expression in ID1289.)
- **BACE1**: Regulates neuronal proliferation; overexpression causes microglial hyperactivation, excessive synaptic pruning, and neuroinflammation. (The only gene with increased expression in the ID1289 proband.)
- **DARS2**: Associated with leukoencephalopathy — a recurrently targeted gene in Korean probands.
- **MASP1**: Associated with learning disability — a recurrently targeted gene.
- **TAF2**: Associated with microcephaly and intellectual disability — a recurrently targeted gene.
- **CACNA1D, CADM1, CTNNA2, PBX1, SLC6A3, COL28A1**: Recurrently targeted genes that follow a high-haploinsufficiency (pLI > 0.9) pattern.
- **(SSC recurrent targets)** **AKAP9, CAMK2A, EIF4E, GRIP1, HLA-B, MBOAT7, CNOT3, ABCA13** (ASD), **CACNA2D4, DGKZ** (schizophrenia), **TMEM138** (Joubert syndrome), **CNOT10** (ADHD), and other genes associated with diverse neurodevelopmental disorders.

## Main Findings
- In Korean probands, 215 non-coding DNMs → 363 target genes (siblings: 67 DNMs → 91 genes); replicated with 1,262–1,421 target genes in SSC and 450–632 in MSSNG.
- 76.9% of target genes (279/363) were distal genes rather than the "nearest gene" to the variant.
- 63.1% of target genes (229/363) formed long-range interactions of 100–500 kb, versus 17.2% (21/122) for the nearest-gene set, P = 6.7×10⁻¹⁸.
- Only proband target genes significantly overlapped with ASD-brain DE genes (P = 0.01); the nearest genes and sibling targets were not significant. Replicated in SSC as well (P = 0.03).
- Neural progenitor cell Hi-C interaction strength: DHS-correlated set > TSS-containing set > baseline set (suggesting regulatory relevance during early neurodevelopmental stages).
- Target genes significantly overlapped with fetal-period spatiotemporal expression signatures (amygdala, cortex, cerebellum, hippocampus) (each P < 0.05).
- Non-coding DNMs within chromatin interactions constitute only about 1.2% of all non-coding DNMs (SSC 1.0%, MSSNG 1.2%), yet in probands they disrupted more TFBS than in siblings (P = 0.018) and had a higher proportion of variants disrupting multiple TFBS (≥4) (P = 0.01). Proband predominance was observed for ASD-related SFARI transcription factors.
- In Korean probands, 20 genes were recurrently targeted (P < 0.05, Bonferroni; including DARS2, MASP1, TAF2); 291 additional genes in SSC.
- Of 311 recurrent target genes, 69 (22.2%) followed a high-haploinsufficiency (pLI > 0.9) pattern (P = 0.035, 10,000 permutations).
- Pathway enrichment: pregnancy (GO:0007565, P = 5.5×10⁻⁷), histone modification (WP:2369, P = 3.7×10⁻¹³, non-coding targets) and histone modification (P = 6.6×10⁻⁴, deleterious coding targets) → suggesting disruption of epigenetic regulation.
- 72.3% of Korean probands carried at least one of a non-coding DNM within a chromatin interaction or a deleterious coding DNM; 20.7% carried both.
- Probands carrying both types had significantly lower IQ (Korea P = 0.02, SSC P = 0.002; siblings P = 0.67, not significant). A greater number of affected genes tended to be associated with lower IQ.
- In hiPSC-derived pNSCs, 7 of 10 target genes had significantly perturbed expression in probands relative to parents: ID992 — decreased ARHGEF2 and CDK5RAP2; ID1289 — decreased CTNNA2, GRB10, IKZF1, PDE3B and increased BACE1. Of the 7 validated genes, 5 (ARHGEF2, CDK5RAP2, CTNNA2, GRB10, PDE3B) are located distal to the variant.
- Example tested variants: chr1:155445465:T>C → ARHGEF2, chr9:123659550:G>A → CDK5RAP2 (ID992); chr7:50418513:C>T → DDC·FIGNL1·IKZF1·GRB10·ZPBP, chr2:79656045:G>A → CTNNA2, chr11:14963517:G>C → PDE3B, chr11:117170461:C>A → BACE1 (ID1289).
- No bi-allelic coding variants (rare homozygous/compound heterozygous) in the target genes were found in probands → supporting an oligogenic multi-hit model of non-coding and coding variants.

## Applications
- Provides an integrative framework (WGS + Hi-C/DNase-seq + hiPSC validation) that uses 3D chromatin interaction information to prioritize functional candidate non-coding variants without requiring a very large sample size.
- Proposes experimentally validated target genes (ARHGEF2, BACE1, CDK5RAP2, CTNNA2, GRB10, IKZF1, PDE3B, etc.) as novel candidate ASD risk genes.
- Provides a basis for stratifying clinical psychopathology, such as predicting IQ / comorbid intellectual disability through the combination of non-coding and coding DNMs.
- Builds and releases the Korean ASD genomic/phenotypic resource (KAGD), laying a foundation for follow-up research.

## Extensibility / Future Directions
- Additional replication of chromatin-interaction-based functional non-coding signals is needed in larger independent ASD cohorts.
- Further study is needed to establish the experimentally validated target genes as novel ASD risk genes (explicitly noted as "warrants further study" in the paper).
- There is room for in-depth study of individual gene mechanisms, such as time-dependent expression regulation of IKZF1 and PDE3B–leptin signaling and synaptic plasticity.
- Expansion beyond pNSCs to later neurodevelopmental stages such as mature neurons and organoids is possible.

## Disease Relevance
- Presents 3D-chromatin-architecture-mediated non-coding regulatory variants as one of the core etiologies of ASD, complementing the prevailing coding-variant-centric understanding.
- Links, through clinical IQ data, the cooperative (multi-hit) action of non-coding and coding variants to severe psychopathology such as ASD with comorbid intellectual disability.
- Suggests that perturbed target-gene expression during fetal neurodevelopment (the neural progenitor stage) is the molecular basis of early neurodevelopmental abnormalities in ASD.
- Recurrent target genes overlap with diverse neurodevelopmental disorders such as leukoencephalopathy (DARS2), microcephaly (TAF2, CDK5RAP2), intellectual disability (ARHGEF2), and Joubert syndrome (TMEM138), illustrating the genetic heterogeneity and convergent etiology of ASD.

## Novelty vs. Prior Work
- Unlike prior non-coding association studies that require large sample sizes (e.g., CWAS) or rely on methods that do not consider 3D structure (such as proximity to SFARI risk genes or disease-impact scores), this study explicitly uses enhancer–promoter chromatin interactions to prioritize distal target genes.
- As stated by the authors, this is the first study to elucidate the significance of non-coding DNMs in relation to transcriptional regulatory disruption—particularly long-range chromatin interactions in early human neural tissue.
- In contrast to a previous SSC-based CWAS study that reported non-coding variants have little effect on haploinsufficient genes, this study shows that non-coding DNMs within chromatin interactions do affect haploinsufficient genes (indicating that, even within the same cohort, differences in analytical method can lead to the detection of meaningful non-coding variants).
- Directly validates computational predictions with patient-derived hiPSC/pNSC experiments, demonstrating the reality of long-range interactions and the perturbation of gene expression.

## Data / Code Availability
- All sequencing and phenotype data are hosted in the Korean Autism Genomics Database (KAGD, https://kagd.kisti.re.kr) and are provided to approved researchers upon request after additional IRB approval.
- Replication data use the public resources SSC and MSSNG (MSSNG database, https://research.mss.ng).
- No separate code repository is specified in the paper (tools used—BWA-MEM, GATK, FreeBayes, TrioDenovo, BEDTools, FIMO/MEME, Boruta, denovolyzeR, ChromHMM, 3DIV, ClueGO, etc.—are specified).

## Keywords
Autism spectrum disorder (ASD), non-coding de novo mutations (non-coding DNM), three-dimensional chromatin interactions, enhancer–promoter looping, whole-genome sequencing (WGS), DNase-seq/Hi-C, neural progenitor cells (hiPSC/pNSC), haploinsufficiency (pLI)/multi-hit (oligogenic), intelligence quotient (IQ)/intellectual disability, fetal neurodevelopment
