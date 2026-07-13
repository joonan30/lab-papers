# Tandem repeats in human brain evolution and disease susceptibility

## Bibliographic Information
- **Authors**: Hyeji Lee (first author), Joon-Yong An (corresponding author, joonan30@korea.ac.kr) — Department of Integrated Biomedical and Life Sciences / Department of Biosystems and Biomedical Science, Korea University, and affiliated units.
- **Journal / Year**: Molecules and Cells, 2026, 49(6): 100363
- **PMID / DOI**: 42055287 / 10.1016/j.mocell.2026.100363
- **Article Type**: Review Article — includes a resource (database) summary table.

## One-Line Summary
This review synthesizes an evolution–disease trade-off perspective in which tandem repeats (TRs), because of their high mutation rate, reversibility, and dose-dependent (graduated) phenotypic effects, have served as "evolutionary tuning knobs" for human brain evolution, while that very same genetic instability renders the nervous system especially vulnerable to repeat-mediated pathology.

## Research Summary
Tandem repeats (TRs) are elements composed of adjacent, arrayed DNA sequence motifs, and they make up roughly 7–8% of the human genome. They are classified by repeat-unit length into short tandem repeats (STRs, 1–6 bp) and variable number TRs (VNTRs, ≥7 bp); in recent assembly-based catalogs, STRs account for 85.6% and VNTRs for 14.4%. TRs have three distinguishing properties: (1) an exceptionally high mutation rate (10⁻³–10⁻⁶ per generation, one to four orders of magnitude higher than single-nucleotide substitutions), (2) reversibility (expansions can be reverted by contraction, functioning as a "fail-safe" mode of evolutionary experimentation), and (3) dose-dependent, continuous phenotypic effects that scale with repeat length rather than acting as a binary switch. The authors propose that these three properties make TRs "evolutionary tuning knobs" that enable rapid and precise phenotypic adjustment without permanent genetic change.

The review examines TRs from three perspectives. First, it organizes the molecular mechanisms by which TRs regulate genes in a length-dependent manner at the transcriptional/chromatin level, the post-transcriptional level (splicing, RNA metabolism), and the translational/protein level. Promoter-proximal TRs tune expression through transcription-factor binding, nucleosome positioning, chromatin accessibility, and CTCF-based chromatin boundaries; they can attenuate transcription via G-quadruplex formation, and short repeats can even act as their own transcription start sites. TRs in introns and untranslated regions participate in RNA secondary-structure formation, Dicer-mediated small-RNA generation, and alternative splicing (through changes in the branch point–splice site distance, complementary-repeat-mediated RNA loop formation, and sequestration of RNA-binding proteins). Trinucleotide repeats in coding regions generate homopolymeric amino-acid tracts (polyQ, polyA, etc.); these tracts reside predominantly in intrinsically disordered regions (IDRs) and modulate protein–protein interactions and biomolecular condensate formation.

Second, the review examines the role of TRs in human evolution. Over the short evolutionary window of ~5–6 million years since divergence from chimpanzees, the human brain expanded roughly threefold, and analyses based on complete telomere-to-telomere assemblies showed that human–chimpanzee genome divergence reaches ~12–13% once simple-repeat regions are considered, with simple repeats being the fastest-diverging regions. Approximately 1,600 human-lineage-expanded TR loci and approximately 9,000 human-expanded TR loci have been identified, and these are strongly and non-randomly enriched near genes for brain development and synaptic function. Cases across multiple lineages—yeast, plants, dogs, carnivores—in which TR-length variation finely tunes morphology and expression (e.g., RUNX2 and snout/face length, Alx4/Runx2 and limb/craniofacial morphology) support the view that TRs continuously generate adaptive diversification without disrupting core gene structure.

Third, the review addresses the evolutionary cost by which the same mutational instability makes the brain vulnerable to repeat-mediated disease. Since the discovery that trinucleotide-repeat expansions cause fragile X syndrome and Huntington's disease, pathogenic repeat expansions have been identified in more than 60 human diseases, with a pronounced clustering in brain and neurological conditions. The authors argue that the brain's distinctive cellular and molecular features—the permanently post-mitotic state of neurons and their long, transcriptionally complex genes—create an environment especially permissive to repeat-mediated pathology. They conclude that TRs are not isolated pathogenic loci but integral components of neural regulatory architecture, and that this perspective provides a framework for interpreting the genetic basis of neurological and psychiatric disorders. The authors tabulate the TR databases and resources that have rapidly grown on the back of recent long-read sequencing, and propose the transition of population-scale studies to long-read sequencing platforms as a future direction.

## Methods & Technologies
- **Article type**: A literature-synthesis review — centered on integrating existing research and presenting a conceptual framework rather than on large-scale in-house experiments/sequencing.
- **In-house computational analysis (Fig. 3A–C)**: Comparison of gene-architecture features between neural and non-neural tissues. Using GTEx Tissue Gene Expression Profiles (2023), the top 1,000 genes by tissue-specific expression z-score were defined as tissue-enriched protein-coding genes, and gene length, intron fraction, and TR overlap (bp) were computed. GENCODE v26 basic gene annotation and the UCSC hg38 Simple Repeat track were used, and P values were derived by two-sided Wilcoxon rank-sum tests (P = 1.29×10⁻⁷, 1.98×10⁻⁷, and 8.37×10⁻⁸, respectively).
- **Conceptual / data resources**: Cites results from telomere-to-telomere (T2T-CHM13) and haplotype-resolved assemblies, HPRC (Human Pangenome Reference Consortium), 1000 Genomes, long-read sequencing (PacBio HiFi, ONT), and single-cell analyses.
- **Curated TR catalogs / databases (Table 2)**: Illumina 174K TR catalog (2019), TREXplorer v2.0, TRCompDB v2.0, Adotto v1.2.1, PlatinumTRs v1.0, Comprehensive TR Catalog (Chiu et al.) v2.0, EnsembleTR, Tandem Repeat Aggregation Atlas (TR-Atlas), TR Constraint score (Danzi et al.), STRchive, and others — organized by locus counts, reference genome (GRCh37/38, T2T-CHM13), motif range, and URL.
- **Cited tools / techniques**: ExpansionHunter (repeat genotyping), Harmonizome 3.0, the GEM-HD Consortium GWAS (identifying somatic-expansion modifiers FAN1, PMS2, MSH3), CRISPR/Cas9-based repeat-editing validation, antisense oligonucleotides (ASO, MSH3-targeting), and others.

## Key Genes / Proteins
(Representative TR-containing genes from Table 1 and loci emphasized in the text)
- **CACNA1C** (TRACT, VNTR 30 bp, intron 3): Human-specific repeat; acts as a cis-regulatory enhancer in neural progenitor cells; associated with schizophrenia and bipolar-disorder risk.
- **FMR1** (CGG, 5′UTR): Fragile X syndrome, fragile X–associated tremor/ataxia, and premature ovarian failure; AGG interruptions modulate expansion risk.
- **FXN (frataxin)** (GAA, intron 1): Friedreich's ataxia; the repeat forms triplex/sticky DNA that silences frataxin transcription, while GGA/TCC interruptions prevent pathology.
- **CYTH4** (GTTT, promoter): Primate-specific repeat; length-dependent regulation of promoter activity; associated with Alzheimer's disease, multiple sclerosis, and schizophrenia.
- **GPM6B** (GA, promoter): CRISPR deletion of the GA repeat impairs neural differentiation — direct evidence that promoter-type repeats tune neurodevelopment.
- **NOTCH2NLC** (CGG/GGC, 5′UTR): Human-specific gene; GGC expansion → polyG non-canonical (RAN) translation; neuronal intranuclear inclusion disease, Alzheimer's disease, and Parkinson's disease.
- **C9orf72** (GGGGCC, intron 1): ALS/FTD; GGGGCC expansion drives RNA gain-of-function, dipeptide-repeat (DPR) production, and splicing-mediated exonization.
- **DMPK** (CTG, 3′UTR): Myotonic dystrophy type 1 (DM1) and ASD association; CUG-repeat RNA sequesters MBNL → splicing misregulation.
- **ABCA7** (VNTR, intron 18): Alzheimer's disease; VNTR expansion → exon 19 skipping, inversely correlated with expression.
- **WDR7** (VNTR 69 bp, intron 27): ALS; human-specific repeat, repeat-RNA aggregation.
- **ATXN10** (ATTCT, intron 9): Spinocerebellar ataxia type 10 (SCA10); AUUCU repeat-RNA foci.
- **RFC1** (AAGGG and other 5 bp motifs, intron 2): CANVAS / late-onset cerebellar ataxia; G-quadruplex formation causes replication stalling and impaired translation.
- **HSTR1** (VNTR 39 bp, ncRNA/HAR): Human-specific repeat; tunes ncRNA stability (more repeats → longer RNA half-life).
- **SLC6A3 (DAT)** (VNTR 40 bp, 3′UTR): Dopamine transporter; the 10-repeat allele yields ~50% higher protein/striatal activity than the 9-repeat allele.
- **ATXN1** (CAG, coding exon 8): SCA1; polyQ toxicity, with CAT interruptions reducing slipped-strand DNA formation and stabilizing the repeat.
- **HTT** (CAG, coding exon 1): Huntington's disease; polyQ gain-of-function, with MSH3-mediated somatic expansion driving crossing of the toxicity threshold (~150 CAG).
- **NBPF (Olduvai/DUF1220 domain)** (protein domain, coding): Human-specific extreme expansion (~102 → ~272–300 copies); dose-dependently associated with brain size, ASD severity, microcephaly, and schizophrenia.
- **Additional neurally expressed, VNTR-rich genes** mentioned include NOTCH2NLC/NOTCH2NL, ZMYM3, RASGEF1C, SBF1, RIT2, SOX5, MECOM, GABRA3, PTPRN2, DLGAP2, and CNTNAP2.
- **Key regulatory proteins**: MBNL (splicing), CELF1/CUG-BP, MSH3/FAN1/PMS2/PMS1 (mismatch-repair modifiers of somatic expansion), Dicer (cleavage of repeat RNA), FAM98B (tRNA-ligase complex, sequestered by polyG), and TDP-43 (binds m1A-modified repeat RNA).

## Main Findings
- TRs make up roughly 7–8% of the human genome, and the STR mutation rate is 10⁻³–10⁻⁶ per generation, one to four orders of magnitude higher than single-nucleotide substitutions.
- About 68.8% of proteins in the human proteome contain at least one TR, and repeat length is positively correlated with protein length.
- Based on T2T assemblies, human–chimpanzee genome divergence is ~12–13%, with simple repeats being the fastest-diverging regions.
- Approximately 1,600 human-lineage-expanded TRs and approximately 9,000 human-expanded TRs are strongly clustered near brain-development and synaptic-function genes, and 152 TRs arose de novo near neurodevelopmental genes.
- About 2% of human core-promoter STRs reach very long lengths (≥6 repeats) and are selectively expressed in neural-differentiation genes.
- The SLC6A3 (DAT) 10-repeat allele produces ~50% higher protein levels than the 9-repeat allele.
- The NBPF Olduvai/DUF1220 domain expanded from ~102 copies in the human–chimpanzee ancestor to ~272–300 copies in modern humans, and the CON1-subtype copy number correlates linearly and dose-dependently with ASD severity.
- Neural tissues show significantly higher mean gene length, intron fraction, and per-gene TR overlap than non-neural tissues (all P < 10⁻⁶; Fig. 3).
- In Huntington's disease, the polyglutamine CAG expansion size is negatively correlated with age of onset and explains 50–70% of its variability. Single-cell analyses showed that in specific cell types (striatal projection neurons) the repeat length undergoes somatic expansion over decades and, once the threshold is exceeded, switches to an abrupt degenerative trajectory.
- Genetic perturbation of Msh3/Pms1 slows or halts neuronal somatic expansion in vivo and ameliorates the phenotype — establishing that repeat dynamics themselves are a primary pathogenic axis.
- Pathogenic repeat expansions have been identified in more than 60 diseases, clustered in brain and neurological conditions; the length distributions of disease-associated loci are frequently multimodal and strongly stratified by ancestry (e.g., rarity of DM1 in individuals of African ancestry, rarity of FRDA in individuals of East Asian ancestry).

## Applications
- Provides a conceptual framework that reinterprets the genetic risk of neurological and psychiatric disorders not as a binary "expanded vs. non-expanded" distinction, but as a continuous spectrum combining repeat length, motif composition, interruption pattern, and cell-type-specific behavior.
- Enables pathogenicity prediction that considers not only repeat length but also motif composition and interruptions (e.g., FMR1 AGG, ATXN1/ATXN10 interruptions, FXN GGA/TCC interruptions) — applicable to clinical genetic diagnosis and risk stratification.
- Provides a rationale for therapeutic strategies that directly target somatic expansion (e.g., MSH3-targeting antisense oligonucleotides).
- Organizes long-read-based TR catalogs, constraint scores, and disease knowledge bases (Table 2) as clinical and research resources.

## Extensibility / Future Directions
- Transition of population-scale (biobank-scale) studies from short-read to long-read sequencing platforms — needed to resolve systematic undercalling of repeat-rich regions, ambiguous genotypes, and their exclusion from variant discovery.
- Harmonization of locus definitions across catalogs, robust cross-platform calibration of repeat length and motif composition, and development of complex-allele representations that preserve regulatory meaning.
- TR-contribution studies that extend beyond disease risk to encompass diverse phenotypic dimensions and population-specific expression.
- Comparative validation of TR-mediated regulatory evolution by obtaining haplotype-resolved assemblies in lineages where cognition evolved independently (e.g., cetaceans, elephants, corvids).

## Disease Relevance
Repeat expansions underlie a broad range of neurological and psychiatric disorders, including fragile X syndrome, Huntington's disease, Friedreich's ataxia, spinocerebellar ataxias (SCA1/10), myotonic dystrophy type 1, C9orf72-associated ALS/FTD, Alzheimer's disease (ABCA7, ZMYM3), Parkinson's disease and neuronal intranuclear inclusion disease (NOTCH2NLC), CANVAS (RFC1), and schizophrenia/bipolar disorder (CACNA1C, ZMYM3, NBPF). The authors summarize that the brain's vulnerability arises from (1) DNA-damage accumulation and replication-independent somatic expansion due to the permanent post-mitotic state, (2) structural vulnerability from long genes and complex recursive splicing, and (3) functional vulnerability from a highly interconnected network of neural genes and proteins. Pathology arises when repeats exceed the nervous system's buffering capacity and disrupt regulation, and newly elucidated mechanisms (splicing-mediated exonization, m1A repeat-RNA–TDP-43 aggregation, tRNA-ligase sequestration, and the reconceptualization of DNA-level mutagenesis as a primary pathogenic axis) go beyond classical models.

## Novelty vs. Prior Work
- Redefines TRs not as "isolated pathogenic mutations" but as integral, quantitative components of neural gene-regulatory architecture, and integrates the adaptation (tuning knobs) of human brain evolution and its disease vulnerability (evolutionary cost) into a single trade-off frame.
- Beyond transcriptional silencing, RNA gain-of-function, protein gain-of-function, and RAN translation that prior reviews covered well, places conceptual emphasis on newly revealed pathogenic axes (the primacy of DNA-level mutagenesis, splicing-mediated toxic reconfiguration, and extension into neurodevelopmental contexts such as ASD).
- Uses in-house computational analysis (Fig. 3) to quantitatively demonstrate that neural-tissue genes have significantly greater length, intron fraction, and TR overlap.
- Synthesizes the TR resources of the long-read sequencing era (Table 2) in an up-to-date state.

## Data / Code Availability
- No separate in-house data/code repository is specified (a review). However, the Fig. 3 analysis uses public resources (GTEx 2023, GENCODE v26, UCSC hg38 Simple Repeat track, Harmonizome 3.0).
- Table 2 lists URLs for public TR databases: Illumina RepeatCatalogs, trexplorer.broadinstitute.org, TRExplorer-catalog, TRCompDB (Zenodo), Adotto (github ACEnglish/adotto), PlatinumTRs (github dashnowlab), Comprehensive TR Catalog (github bcgsc_catalog), EnsembleTR (github gymrek-lab), TR-Atlas (wlcb.oit.uci.edu/TRatlas), STRchive (strchive.org), and others.
- **Generative-AI use disclosure**: ChatGPT was used during manuscript preparation to improve language clarity and readability; the authors reviewed and revised the output and take final responsibility for it.

## Keywords
Gene regulation, Genetic instability, Human brain evolution, Neurological disorders, Repeat expansion, Tandem repeats (STR/VNTR), Evolutionary tuning knobs, Somatic expansion, RAN translation, Long-read sequencing
