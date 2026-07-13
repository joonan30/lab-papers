# Advancing precision diagnosis in autism: Insights from large-scale genomic studies

## Bibliographic Information
- **Authors**: Soo-Whee Kim (first author), Joon-Yong An (corresponding author, joonan30@korea.ac.kr). Both authors are affiliated with Korea University (Department of Integrated Biomedical and Life Science; L-HOPE Program; School of Biosystem and Biomedical Science)
- **Journal / Year**: Molecules and Cells (Mol. Cells) 2025; 48(8): 100248 (Available online 26 June 2025; Received 2 May 2025, Revised 9 June 2025, Accepted 22 June 2025)
- **PMID / DOI**: PMID 40581089 / https://doi.org/10.1016/j.mocell.2025.100248
- **Article Type**: Review

## One-Line Summary
A review that synthesizes the integrated genetic architecture of autism spectrum disorder (ASD) revealed by large-scale whole-exome (WES) and whole-genome (WGS) sequencing—spanning coding and noncoding variants and polygenic burden—and consolidates the current status and challenges of translating these insights into clinical applications: gene-based therapeutics, noncoding-variant interpretation, and genetic diagnosis.

## Research Summary
This review synthesizes the complex genetic architecture of autism spectrum disorder (ASD) uncovered by large-scale genomic studies over the past decade or so. Beginning with early microarray-based CNV analyses and GWAS, next-generation sequencing—particularly WES—revealed that de novo protein-truncating variants (PTVs) are overrepresented in loss-of-function-intolerant, constrained genes, and that rare inherited variants also contribute more subtly to risk. However, because WES is confined to the protein-coding region, which is roughly 1.5% of the genome, the authors emphasize that WGS captures both coding and noncoding variants (regulatory elements, promoters, UTRs, short tandem repeats [STRs], etc.), bridging the gap between rare high-effect variants and common polygenic influences.

The review organizes the history of gene discovery alongside the development of large-scale datasets and statistical models (TADA, Bayesian de novo/transmission association models). Discovery expanded from the first SSC-based TADA identifying 33 genes (De Rubeis 2014), to 65 genes (Sanders 2015), to 102 genes from 35,584 WES samples (Satterstrom 2020), to 72 genes—including CNVs—from 63,237 individuals with the addition of SPARK (Fu 2022), and to 53 genes from integrated MSSNG, SSC, and SPARK WGS (Trost 2022). The review also stresses the importance of ensuring ancestral diversity, introducing non-European population studies such as a Chinese ASD cohort (22 genes including the novel gene SLC35G1, Wang 2023), a sex-stratified TADA integrating a Korean cohort with SSC and SPARK yielding 98 genes (Kim 2024c), and a Latin American ancestry consortium identifying 61 genes (Avila 2025).

The review then addresses the functional characteristics of ASD risk genes. Recurrent de novo CNVs in synaptic genes (NRXN1, NLGN3, SHANK2/3, SYNGAP1) were identified early on, and WES showed that risk converges on the neuronal communication (NC) and gene expression regulation (GER) pathways. Co-expression network and single-cell transcriptomic analyses showed that GER genes are concentrated in early progenitor and pre-mitotic neurons, while NC genes are concentrated in mature excitatory neurons, suggesting that the timing of gene perturbation and the targeted cell type shape clinical outcomes (ASD-predominant vs developmental delay [DD]-predominant). The authors introduce advances in experimental models such as patient-derived cerebral organoids and CRISPR screens, while using their own NLP analysis (Fig. 2) to quantify that many of the 185 ASD genes compiled by Fu 2022 have not yet been experimentally validated, thereby highlighting the gap between gene discovery and biological understanding.

Another axis of the review is noncoding risk variants and polygenic burden. Through WGS, ASD associations of rare and de novo variants have been reported in 5'/3' UTRs, promoters, enhancers, DNase I hypersensitive sites, 3D chromatin enhancer-promoter interactions, and STRs, and the functional effects of some variants are being validated by massively parallel experiments such as MPRA, CRISPRi, and CROP-seq (Table 1). On the polygenic side, the review explains the additive and compensatory interactions of rare and common variants and the sex differences (female protective effect) through polygenic scores (PS), the polygenic transmission disequilibrium test (pTDT), and the liability-threshold model (Fig. 3), in which the cumulative genetic burden must exceed a diagnostic threshold for ASD to manifest.

Finally, the review presents near-term clinical applications along three axes: (1) gene-based therapeutics already advanced in monogenic disorders (Table 2), (2) clinical interpretation of noncoding variants (e.g., the snRNA genes RNU4-2/RNU2-2, and splicing variants), and (3) individualized risk prediction and genetic diagnosis leveraging PS, machine learning, and deep learning. The authors conclude that large-scale population studies encompassing somatic mosaicism, environmental and gene-environment interactions, multi-omics integration, and well-curated longitudinal phenotype data are the future tasks for realizing precision medicine.

## Methods & Technologies
(Major research methodologies and data types the review synthesizes and discusses)
- Whole-exome sequencing (WES) and whole-genome sequencing (WGS) — detection of rare coding/noncoding variants, de novo variants (DNVs), and STRs
- Microarray-based CNV analysis, GWAS (genome-wide association study), and array-based genotyping
- TADA (Transmission And De novo Association) — a Bayesian risk-gene discovery framework integrating de novo PTVs, missense variants, and CNVs
- Polygenic score (PS) and polygenic transmission disequilibrium test (pTDT)
- Liability-threshold model
- Single-cell RNA-seq / ATAC-seq, co-expression network analysis, developmental transcriptomic and regulatory maps
- Analysis of enhancer-promoter interactions using 3D chromatin conformation data
- Massively parallel reporter assay (MPRA), CRISPRi/CRISPR activation, CROP-seq, and other functional validation experiments
- Patient-derived cerebral organoids, iPSC models, and animal models (Mouse, Rat, Xenopus, Drosophila, Zebrafish)
- Functional annotation tools (GERP, ENCODE) and deep-learning prediction models (Enformer, Sei, AlphaFold, AlphaMissense, ESM, etc.)
- Automated NLP analysis of PubMed abstracts (OpenAI GPT-4o-mini) to compile the experimental-validation status of genes (Fig. 2)

## Key Genes / Proteins
- **SCN2A**: A representative ASD risk gene with a broad syndromic spectrum (gain-of-function → early-onset epilepsy; loss-of-function → ASD, intellectual disability, language impairment); an example of a high-effect variant in the liability-threshold model
- **SHANK2 / SHANK3**: Postsynaptic scaffold proteins that anchor glutamate receptors; SHANK3 haploinsufficiency induces the ASD phenotype
- **SYNGAP1**: Regulates synaptic signaling; de novo CNVs and organoid neurogenesis defects
- **NRXN1 / NLGN3**: Early-discovered risk genes related to synaptic adhesion and connectivity
- **ARID1B**: Component of the SWI/SNF chromatin-remodeling complex; regulates chromatin accessibility in deep-layer excitatory neurons and interneurons; a DD-predominant gene
- **FOXP1**: Regulates neuronal gene expression; converges on genetic targets with ARID1B; an ASD-predominant gene
- **TBR1**: A transcription factor participating in mid-fetal neuronal gene-expression regulatory networks
- **PTEN**: Its loss induces synaptic overgrowth and mTOR dysregulation
- **CNTNAP2**: Involved in synaptic vesicle cycling and mitochondrial function; related to mTOR and ubiquitin pathways
- **TRIO / BRAF**: TRIO mediates actin remodeling via Rac1; BRAF, a RAS-MAPK component, regulates neuronal differentiation and dendrite formation
- **DYRK1A / KMT2A**: An example contrasting an ASD-predominant gene (DYRK1A) vs a DD-predominant gene (KMT2A)
- **CHD8, MECP2, SUV420H1, CTCF, GLI3, TP53, PAX6**: In CRISPR and organoid experiments, perturb cortical layer formation, progenitor proliferation, and synaptic maturation
- **UBE3A (and UBE3A-ATS)**: Target of Angelman syndrome; a target for paternal-allele reactivation therapy
- **MECP2**: Cause of Rett syndrome; a therapeutic target for AAV, ASO, and ADAR2 RNA editing
- **FMR1 / FMRP**: Cause of Fragile X syndrome; its loss affects synaptic protein synthesis and causes hyperexcitability; a target for mGluR5 inhibition and splicing correction
- **NAV3**: An example of a moderate-effect variant in the liability-threshold model (requires additional burden)
- **SLC35G1**: A novel risk gene discovered in a Chinese ASD cohort
- **NR3C2, DLG2**: Noncoding risk targets with reported promoter tandem-repeat deletions (Ruzzo 2019)
- **LRRC4, ZNF644**: 5' UTR de novo variants altering neuronal translational activity (Plassmeyer 2023)
- **LRP1**: Near a schizophrenia GWAS variant (rs324017); altered neuronal excitability and ASD association
- **DMPK, FXN, FGF14, CACNB1**: Loci with reported STR expansions (Trost 2020, Kim 2024a)
- **RNU4-2 / RNU2-2**: Noncoding genes encoding the U4/U2 snRNAs; emerging as common monogenic causes of neurodevelopmental disorders

## Main Findings
(Key points and consensus/debates the review consolidates)
- Larger sample sizes and improved ancestral diversity have continuously expanded ASD-associated gene discovery (33 → 65 → 102 → 72 [+CNV] → 53, etc., depending on cohort and method).
- ASD risk converges on two pathways—neuronal communication (NC) and gene expression regulation (GER)—with GER-gene expression concentrated in early progenitors and NC-gene expression concentrated in mature excitatory neurons.
- The developmental timing and target cell type of gene perturbation shape ASD-predominant vs DD-predominant clinical outcomes (e.g., FOXP1 and DYRK1A are ASD-predominant; KMT2A and ARID1B are DD-predominant).
- Many discovered ASD genes have not yet been experimentally validated—among the 72 high-confidence genes, only 58 have functional studies, and among the remaining 113, only 79 do (Fig. 2). A gap exists between gene discovery and biological understanding.
- WGS captures noncoding risk variants in 5'/3' UTRs, promoters, enhancers, DNase hypersensitive sites, conserved regulatory regions, and 3D chromatin loops, and these are particularly enriched in inhibitory neurons and transcription-factor binding regions.
- Rare STR expansions (STRs comprise ~6.8% of the genome) contribute roughly 2.6–4% to ASD risk and are associated with lower IQ, poorer adaptive ability, and more severe phenotypes.
- Functional validation via MPRA, CRISPRi, and CROP-seq has begun to confirm the enhancer, translational, and chromatin-accessibility effects of individual noncoding variants, although in some cases (common variants from psychiatric GWAS) strong MPRA activity was not detected.
- Common inherited variants account for most of the ASD genetic burden (albeit with small effect sizes), and the liability-threshold model explains the additive and compensatory interactions of rare and common variants (e.g., de novo variant carriers have lower PS—a compensatory effect).
- Sex differences: ASD is roughly 4 times more common in males, and female patients carry a greater burden of rare high-effect variants (female protective effect). The sex difference may be explained by a higher diagnostic threshold in females and/or greater variance in genetic burden in males (Fig. 3B).
- In monogenic disorders (Angelman, Rett, Fragile X, SCN2A-related), CRISPR-, ASO-, and RNA-editing-based therapies have shown partial success in animal, non-human primate, and patient-derived cell models (Table 2).
- The predictive power of PS is still limited (explaining ~2% of burden variance), but there is room for improvement by integrating multiple psychiatric phenotypes, combining developmental measures/CNVs/DNVs, and using deep learning (STAR-NN, AUC 0.73).

## Applications
- **Development of gene-based therapeutics**: Precision therapeutic strategies for monogenic ASD/syndromes, including Angelman (UBE3A-ATS silencing/paternal-allele reactivation, CRISPR/ASO), Rett (MECP2, AAV/ASO + 5-Aza-dC/ADAR2 RNA editing), Fragile X (FMR1 splicing correction/mGluR5 inhibition), and SCN2A (ASO knockdown/CRISPR activation).
- **Clinical interpretation of noncoding and splicing variants**: Expanding diagnosis through interpretation of pathogenic variants in snRNA genes (RNU4-2, RNU2-2) and noncanonical splice-site variants (ARID1B, SCN2A, SHANK3, SYNGAP1).
- **Risk stratification and genetic diagnosis**: Risk stratification using PS (e.g., in 22q11.2 deletion carriers, risk from lowest to highest decile 9% → 33%), an intellectual-disability prediction model integrating developmental measures, rare variants, and PS (Bourque 2025, AUROC ~0.65), and WES-based deep-learning prediction (Wu 2024, AUC 0.73).
- The precision-medicine goal of maximizing children's cognitive and functional potential through early detection and early intervention.

## Extensibility / Future Directions
- **Somatic mosaicism**: Somatic variants in the developing brain may affect regulatory elements, but analyses in ASD remain rare—systematic profiling of brain-specific somatic variants is needed.
- **Environmental and gene-environment interactions**: Modeling the convergence of genetics and environment is needed, including prenatal factors (maternal immune activation, toxin exposure, metabolic stress), epigenetic modifications (DNA methylation, chromatin remodeling), and indirect effects of non-transmitted parental alleles.
- **Multi-omics integration**: Moving beyond single omics to integrate genome, transcriptome, epigenome, proteome, chromatin accessibility, and spatial transcriptomics, and using deep-learning models (AlphaFold, AlphaMissense, ESM, Enformer, Sei, scGPT, CFGen, Geneformer, etc.) to elucidate variant effects and convergence mechanisms.
- **Large and diverse cohorts and longitudinal data**: Improving predictive generalization and equity using large populations with ancestral and phenotypic diversity and well-curated longitudinal phenotype data.
- **Expanded functional validation of noncoding elements**: Developing large-scale perturbation platforms and simulators to capture relatively unexplored regions (e.g., 3' UTRs), validation in native chromatin contexts, and combinatorial and pathway-level effects.
- **Deeper understanding of genotype-phenotype relationships** to enable prognostic prediction and individualized intervention.

## Disease Relevance
The entire paper focuses on autism spectrum disorder (ASD). The review consolidates the genetic architecture of ASD (rare high-effect variants + polygenic burden), the pathophysiological roles of coding and noncoding variants, developmental and cell-type-specific convergence, and the heterogeneity of genetic burden across sex and phenotype, and it emphasizes the clinical implications of translating these into early diagnosis, risk stratification, and gene-based therapeutics. It also presents therapeutic cases from adjacent neurodevelopmental disorders such as Angelman, Rett, and Fragile X syndromes and SCN2A-related disorders as reference points for ASD precision medicine.

## Novelty vs. Prior Work
- Unlike prior reviews centered on coding variants, this review integrates the **noncoding regulatory variants, STRs, and 3D genome architecture** opened up by WGS, together with **polygenic burden**, alongside coding variants for a comprehensive perspective.
- Through the authors' own **automated NLP analysis of PubMed abstracts (GPT-4o-mini)**, they quantify the experimental-validation status of 185 ASD genes (Fig. 2), explicitly revealing the gap between gene discovery and biological validation (code: github.com/joonan-lab/ASD_gene_review).
- It presents in parallel two liability-threshold models explaining sex differences (mean difference vs variance difference), emphasizing that phenotypic differences can confound the assessment of sex differences in genetic burden.
- It systematizes the three axes of translating genetic discovery into the clinic (gene-based therapeutics, noncoding-variant interpretation, and genetic diagnosis) through tables (Table 1, 2) and a conceptual schematic (Fig. 4).

## Data / Code Availability
- NLP analysis code and resulting gene list for Fig. 2: https://github.com/joonan-lab/ASD_gene_review
- Otherwise, as a review it introduces no new primary datasets; data from the cohorts of the cited individual studies (SSC, SPARK, MSSNG, AGRE, PGC, and Korean/Chinese/Latin American cohorts, etc.) follow the respective original papers.

## Keywords
Autism spectrum disorder (ASD), Whole-genome sequencing (WGS), Noncoding variants, Polygenic score / liability threshold, Gene-based therapeutics, De novo variants (PTV), TADA / gene discovery, Neurodevelopment (NC/GER convergence), Short tandem repeats (STR), Precision diagnosis
