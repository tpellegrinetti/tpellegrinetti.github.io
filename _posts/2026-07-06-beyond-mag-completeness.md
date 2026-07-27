---
layout: research-note
title: "Beyond 95%: what genome completeness scores leave out"
description: "Why a highly complete metagenome-assembled genome may still miss ecologically important biology—and how to interpret MAG quality more carefully."
date: 2026-07-06
categories:
  - research-notes
tags:
  - metagenomics
  - MAGs
  - microbial ecology
author_profile: false
read_time: true
share: false
related: false
paper_url: "https://doi.org/10.3389/fmicb.2026.1884628"
paper_label: "Based on our 2026 opinion paper"
note_topic: "Genome-resolved metagenomics"
summary: "A high-quality MAG can satisfy conventional thresholds while still underrepresenting mobile, repetitive, and adaptive regions. A practical guide to interpreting the score without overreading it."
paper_highlight: "2026 perspective"
---

Genome-resolved metagenomics has transformed microbial ecology. Instead of describing a community only through marker genes or aggregate functions, we can reconstruct genomes directly from environmental sequencing data and ask which organisms carry which capacities.

That shift is powerful, but it comes with a deceptively simple question: **how complete is a reconstructed genome?**

The standard answer is usually a percentage. A MAG may be reported as 90%, 95%, or even more than 99% complete, often alongside a contamination estimate. These metrics are indispensable for filtering and comparing large genome collections. The problem begins when an estimated percentage is interpreted as a literal inventory of the genome.

<aside class="article-pullquote">
  <span>Key idea</span>
  <p>“95% complete” does not necessarily mean that 95% of every ecologically relevant part of a genome has been recovered.</p>
</aside>

## What the score actually measures

Completeness is not observed directly. It is **inferred** from evidence such as conserved single-copy marker genes, lineage-specific expectations, or machine-learning models. If most expected markers are present, the genome is likely to contain a large fraction of its conserved cellular machinery.

That is a defensible and extremely useful estimate. It tells us whether a bin looks broadly genome-like and whether major parts of the core genome are present. It does not guarantee that every type of genomic region has the same probability of recovery.

Assembly and binning are selective processes. Short-read assemblies struggle with repeated sequences. Regions with unusual nucleotide composition or coverage can be separated from the contigs to which they biologically belong. Closely related strains can collapse into a consensus or fragment into competing reconstructions.

## Why marker genes are useful proxies

Marker-based completeness works because some genes are broadly conserved across a lineage and usually occur in predictable copy numbers. If a bacterial genome is expected to contain a set of core cellular genes and nearly all are detected in a bin, the reconstruction probably includes much of its conserved chromosome.

The logic is statistical rather than literal. A marker set samples a particular fraction of genome biology, then uses that sample to estimate the whole. Lineage-specific marker sets improve the estimate because expectations for an archaeal genome, a streamlined symbiont, and a large free-living bacterial genome should not be identical.

Contamination estimates often use the same markers. Multiple copies of genes expected to occur once may indicate that contigs from more than one population were combined. Yet real biology can also produce gene duplication, and closely related strains may differ in ways that marker-based summaries do not resolve.

This makes the estimates extremely effective for triage across thousands of bins. They identify obviously incomplete or mixed reconstructions and create shared quality categories. Their limitation appears when a proxy designed for large-scale quality control is asked to support a highly specific biological claim.

## The missing fraction is not random

Some of the regions most likely to be under-recovered are also among the most ecologically informative:

- **rRNA operons and other repeated elements**, which create assembly ambiguity;
- **plasmids and genomic islands**, which often have atypical composition or copy number;
- **prophages and transposons**, which shape genome plasticity and horizontal gene transfer;
- **CRISPR arrays**, which record parts of a population’s interaction with mobile genetic elements;
- **biosynthetic and accessory regions**, which may contribute to competition, host association, antimicrobial resistance, or niche adaptation.

In other words, conserved chromosomal regions can be reconstructed more consistently than flexible genome fractions. A high score may therefore coexist with a systematic blind spot for traits that help distinguish strains and explain how microbes respond to their environment.

## Assembly and binning create different uncertainties

Assembly reconstructs longer sequences from overlapping reads. Binning then groups assembled contigs that are inferred to originate from the same population. A genome can be affected at either stage.

Repeats longer than the sequencing reads can break an assembly. Uneven coverage can leave low-abundance regions unsupported. Multiple closely related strains can create alternative sequence paths that are collapsed, split, or excluded. Once contigs exist, binning algorithms use signals such as nucleotide composition, coverage across samples, and taxonomic similarity to group them.

Accessory elements often violate those expectations. A plasmid can have a different copy number and nucleotide composition from its host chromosome. A recently acquired genomic island may resemble its donor lineage. A phage integrated into the chromosome may be difficult to distinguish from a free viral population.

Co-assembly across multiple samples can provide more sequence support and differential-coverage information, but it can also combine strain diversity from different conditions. Single-sample assembly avoids some cross-sample complexity while losing the comparative signal that helps binning. Neither choice is universally superior; it should follow the biological question and community structure.

Long reads can bridge repeats and link accessory regions to chromosomes, while short reads offer depth and lower per-base error. Hybrid approaches often improve contiguity, but they do not remove the need to evaluate population heterogeneity, coverage, and binning decisions.

<div class="article-comparison" role="group" aria-label="What completeness scores show and what they may miss">
  <div>
    <span class="article-comparison__label">Often well represented</span>
    <strong>Conserved core functions</strong>
    <p>Replication, translation, and other marker-rich cellular systems.</p>
  </div>
  <div>
    <span class="article-comparison__label">More easily under-recovered</span>
    <strong>Flexible &amp; adaptive functions</strong>
    <p>Mobile elements, strain-specific traits, and compositionally unusual regions.</p>
  </div>
</div>

## Why this matters for ecological conclusions

Imagine two MAGs reconstructed from contrasting environments. Both are estimated at 95% completeness. One contains a well-recovered accessory genome; the other is missing a genomic island involved in host association. Treating those two percentages as equivalent biological coverage could distort a comparison of ecological strategies.

The same issue affects public genome catalogues. Composite or consensus MAGs can appear clean according to conventional contamination estimates while obscuring real population structure. When those genomes become references, errors propagate into taxonomic annotation, pangenome analysis, metabolic reconstruction, and evolutionary inference.

This does not make MAGs unreliable. It means their uncertainty is structured—and should be carried into the biological claim.

## Absence is the hardest conclusion

The presence of a well-supported gene in a MAG can be informative. Its absence is more ambiguous because the relevant region may not have assembled, may have been placed in another bin, or may have been filtered as an unclassified contig.

This asymmetry matters in comparative studies. If one population appears to lack a pathway, researchers should ask whether the surrounding genomic region is recovered, whether read mapping supports the absence, and whether close references contain the pathway in an accessory locus. A missing single gene inside an otherwise continuous region is different from a missing pathway near a contig boundary.

The same caution applies to evolutionary claims. Gene loss is biologically meaningful, but demonstrating loss requires stronger evidence than failing to detect a gene in a fragmented reconstruction. Reference-guided searches of unbinned contigs and reads can help, although they introduce their own biases.

Precise language protects the inference. “Not detected in the recovered MAG” describes the observation. “Absent from the population” is a stronger biological conclusion that needs additional support.

## A more careful reading workflow

No single metric can resolve every limitation, but a few habits improve interpretation:

1. **Match quality criteria to the biological question.** A genome suitable for broad taxonomy may not be sufficient for claims about plasmids, biosynthetic clusters, or strain-specific adaptation.
2. **Inspect assembly structure, not only a summary score.** Contig count, N50, coverage variation, and the placement of key loci can reveal limitations hidden by a headline percentage.
3. **Use complementary quality signals.** Marker-based estimates, taxonomic consistency, read mapping, long-read support, and comparisons with close references answer different questions.
4. **Report uncertainty at the level of the conclusion.** If a relevant pathway is absent, distinguish “not detected” from “biologically absent.”
5. **Treat missingness as potentially biased.** Ask whether the workflow is less likely to recover precisely the class of region under study.

## Reporting enough information to reuse a MAG

A quality label is more useful when accompanied by the evidence behind it. Researchers can report the completeness and contamination tool, database version, lineage used for estimation, assembly strategy, sequencing technology, contig count, N50, coverage, and taxonomic assignment.

For claims about a particular function, pathway-level evidence is more valuable than the headline quality category. Which genes were detected? Are they located on the same contig? Does coverage support the region? Are key genes near contig ends? Were unbinned contigs or raw reads searched?

Depositing reads, assemblies, bins, and workflow parameters allows others to revisit those questions as methods improve. A MAG catalogue is not a finished representation of nature; it is a versioned reconstruction based on the data and algorithms available at the time.

Quality standards are still essential. The aim is not to replace them with an unmanageable checklist for every analysis. It is to scale the evidence with the claim: broad ecological surveys need consistent filters, while claims about mobile elements, gene loss, or fine-scale evolution require closer inspection.

## From quality control to epistemology

The deeper issue is not whether a threshold should be 90%, 95%, or 98%. It is how a computational proxy becomes a biological statement.

A completeness score compresses a complex reconstruction process into a number that helps us make decisions at scale. Good science begins when we unpack that compression: which evidence produced the estimate, which genome fractions were easiest to recover, and whether the remaining uncertainty could change the ecological story.

MAGs have opened an extraordinary window into uncultivated microbial diversity. Reading them well requires both enthusiasm for what they reveal and precision about what they may still leave out.

Future improvements will come from several directions: longer and more accurate reads, algorithms that model strain variation, better recovery of plasmids and viruses, reference databases that represent more lineages, and quality metrics tailored to specific research questions.

But no technological advance will remove interpretation from the process. Every reconstruction remains a model built from sampled DNA. The central scientific habit is to connect the confidence of the model to the confidence of the conclusion.

---

<div class="article-citation">
  <span>Original perspective</span>
  <p>Pellegrinetti, T.A., Molligan, J., Mendes, L.W., Pedrinho, A., &amp; Pérez-López, E. (2026). <em>Rethinking metagenome-assembled genome completeness: are we truly recovering complete genomes?</em> Frontiers in Microbiology, 17, 1884628.</p>
  <a class="academic-button" href="https://doi.org/10.3389/fmicb.2026.1884628" target="_blank" rel="noopener noreferrer">Read the open-access paper <span aria-hidden="true">↗</span></a>
</div>
