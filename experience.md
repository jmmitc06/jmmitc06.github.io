---
layout: default
title: Experience
---

## The Jackson Laboratory
**Associate Computational Scientist / Data Scientist** · Farmington, CT · 2023–2026
{: .role}

*Recipient, 2024 MANA Mark P. Styczynski Early Career Award*
{: .award}

- Architected [PCPFM (Python-Centric Pipeline for Metabolomics)](https://github.com/shuzhao-li-lab/PythonCentricPipelineForMetabolomics), an end-to-end processing pipeline for high-resolution LC-MS datasets. PCPFM performs all steps from raw data to final annotated feature table, including QA/QC (blank masking, normalization, automated outlier detection) and supports authentic standard, MS2, and MS1-based annotations. Optimized for non-domain experts on commodity hardware while scaling to 1000+ sample studies.
- Lead developer and maintainer of [Asari](https://github.com/shuzhao-li-lab/asari), a high-performance LC-MS feature extraction engine. Implemented a GC-capable prototype of Asari as part of ARPA's IndiPharm project.
- Extended the [Khipu](https://github.com/shuzhao-li-lab/khipu) framework to handle stable isotope tracing data in an untargeted manner — a first-of-its-kind approach, as most stable isotope tracing tools are inherently targeted.
- Built a lipid formula enumerator that permutes possible lipid formulas from given backbones, enabling the tentative identification of a previously unreported phosphatidylserine biomarker of T-cell exhaustion. Identity was later confirmed using neutral loss patterns in MS2.
- Created Jupyter/Colab training materials and led workshops for 50+ scientists at national and international events. Materials available on the [Teaching](teaching) page.
- Collaborated on chemoselective derivatization protocols boosting metabolite detection 10x; prototyped algorithms for resulting data complexity.
- Performed differential abundance and pathway analysis identifying biomarkers across anti-retroviral treatment (see [HIV preprint](https://www.medrxiv.org/content/10.1101/2026.01.01.634273v1)), CRISPR knockouts in hiPSCs as part of the NIH [MorPhiC Consortium](https://morphic.bio/) (an effort to characterize every human gene's function in every human tissue), and culture media conditions.
- Helped debug LC-MS equipment and designed multi-modal experiments combining direct infusion mass spectrometry with LC-MS to maximize instrumentation capabilities. Randomized and block-designed experiments to minimize the impact of instrument drift and degradation.
- Aided in deployment of web-based applications to the lab's GCP account, including Khipu-Web and Asari.app.

---

## Los Alamos National Laboratory
**Postdoctoral Research Associate, Information Sciences & Chemical Diagnostics** · Los Alamos, NM · 2021–2022
{: .role}

*Recipient, 2022 LANL Spot Award*
{: .award}

- Optimized metabolite extraction methods for maize leaf, root, and exudate tissues and developed instrument methods for a LECO Pegasus HRT-4D+ (2D-GC-TOFMS) as part of an LDRD studying plant-soil-microbiome interactions under drought — motivated by the intersection of climate change and food/biofuel security. Developed normalization approaches (mass, internal standard, detector voltage correction) and a computational workflow combining ChromaTof Tile-based Fischer Ratio Analysis, PLS-DA, and custom Python scripts to identify metabolic biomarkers differentiating microbiome inoculation and watering treatments.
- Investigated and diagnosed instrument drift on the LECO Pegasus HRT-4D+, including filament degradation, S_LENS voltage shifts, and detector voltage changes across acquisition batches — enabling corrective normalization strategies for long-running experiments.
- Developed methods for evaluating how nylon rope wicks added to potted plants can eliminate anoxic zones and mimic field soil hydrology. Aqueous solutions collected at different depths were analyzed to observe how wicks improved the movement of sugars and fertilizer compounds through the soil, demonstrating their potential as a low-cost intervention to improve plant growth.
- Developed a solid phase microextraction (SPME) based method for analyzing the effect of ionizing radiation on gaseous plant metabolites.
- Applied non-parametric statistics and Kendall tau correlation to analyze radioactive iodine (¹²⁵I) uptake in forest soils from Japan (including Fukushima-contaminated sites) and the United States, identifying extracellular oxidase activity as the [primary driver of soil iodination](https://pubmed.ncbi.nlm.nih.gov/36936531/).
- Developed a novel AI similarity metric using ~300k NIST EI-MS spectra, graph coloring-based substructure representation, and Random Forest classifiers combined via Genetic Algorithm (PyGAD) optimization on LANL's Darwin HPC cluster (SLURM) to infer chemical substructures from EI-MS data — a hybrid approach bridging spectral similarity and machine learning for metabolite identification.
- Selected as Finalist in "Science in 3" competition for translating complex research to non-technical stakeholders.
- See [LANL technical report](https://www.osti.gov/servlets/purl/1888206) for additional detail.

---

## University of Kentucky
**M.D./Ph.D. Candidate, Dept. of Molecular and Cellular Biochemistry** · Lexington, KY · 2014–2021
{: .role}

- Engineered [SMIRFE](https://pubmed.ncbi.nlm.nih.gov/31260262/) (Small Molecule Isotope Resolved Formula Enumeration), a high-performance Cython/multiprocessing/SQLite algorithm that constructs a nearly comprehensive search space of all isotopologues within a given mass range — searching >10<sup>140</sup> formula space without relying on metabolite databases. Each assignment is statistically evaluated with an e-value representing the probability of occurring by chance. Patented (US 10,607,723).
- Applied [Random Forest to predict lipid category and class from molecular formula](https://pubmed.ncbi.nlm.nih.gov/32214009/) with >90% accuracy and >83% precision across eight lipid categories. Used the convex hull of known formulas to generate plausible but nonsensical formulas as negative controls, validating that models learned genuine biochemical signatures rather than dataset artifacts.
- Applied these tools to an [untargeted lipidomics study of 86 paired NSCLC tissue samples](https://pubmed.ncbi.nlm.nih.gov/34822397/), identifying a shared metabolic phenotype — elevated sterol esters and sphingolipids with reduced cardiolipins and glycerophospholipids — across genetically distinct lung cancer subtypes, suggesting targetable metabolic vulnerabilities.
- Designed algorithms to [detect and mitigate previously unreported spectral artifacts](https://pmc.ncbi.nlm.nih.gov/articles/PMC6153687/) in Orbitrap instruments, including a novel "fuzzy site" artifact with Gaussian-like intensity distributions spanning 0.5–3 m/z. Used Random Forest to demonstrate that these artifacts encode spurious information (6 of the top 30 classification features were artifact-derived), then developed a sliding-window statistical detection method to systematically remove them — illustrating both the limitations of ML on uncurated data and the value of combining physics-based reasoning with computational approaches.
- Developed [graph coloring approaches](https://pubmed.ncbi.nlm.nih.gov/25120557/) for chemical substructure representation, enabling functional group detection that uniquely identified up to 71% of KEGG compounds (vs 41% with formula alone). Extended this to a [neighborhood-specific atom identifier method](https://pubmed.ncbi.nlm.nih.gov/32933023/) that harmonized KEGG and MetaCyc databases, identifying 8,865 cross-database compound correspondences and flagging representation errors in both databases.
- Helped maintain and design the lab's computational infrastructure, including migrating the lab gateway server to a KVM-based virtual machine with PCIe passthrough.

---

## University of Louisville
**M.D. Candidate / Undergraduate Researcher, Dept. of Chemistry** · Louisville, KY · 2010–2014
{: .role}

- Developed [CASS](https://pubmed.ncbi.nlm.nih.gov/25120557/) (Chemically-Aware Substructure Search), a graph-based algorithm to solve the Maximum Common Subgraph Isomorphism problem in chemical structures. CASS achieves pseudo-linear performance where the classical Ullmann algorithm scales exponentially, enabling database-scale functional group searches across HMDB and KEGG.
- Built a functional group resolved metabolic database to aid chemoselective reagent design.
- Became proficient in HPC, Perl, Linux, and Linux system administration through computational chemistry research.
