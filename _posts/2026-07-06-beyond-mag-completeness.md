---
layout: single
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
share: true
related: false
header:
  image: og-thierry-pellegrinetti.png
---

<p class="article-deck">A metagenome-assembled genome can pass a familiar quality threshold and still fail to recover some of the regions most important for microbial adaptation. The number is useful. The interpretation needs more care.</p>

<div class="article-meta-line">
  <span>Genome-resolved metagenomics</span>
  <span>6 min read</span>
  <a href="https://doi.org/10.3389/fmicb.2026.1884628" target="_blank" rel="noopener noreferrer">Based on our 2026 opinion paper ↗</a>
</div>

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

## The missing fraction is not random

Some of the regions most likely to be under-recovered are also among the most ecologically informative:

- **rRNA operons and other repeated elements**, which create assembly ambiguity;
- **plasmids and genomic islands**, which often have atypical composition or copy number;
- **prophages and transposons**, which shape genome plasticity and horizontal gene transfer;
- **CRISPR arrays**, which record parts of a population’s interaction with mobile genetic elements;
- **biosynthetic and accessory regions**, which may contribute to competition, host association, antimicrobial resistance, or niche adaptation.

In other words, conserved chromosomal regions can be reconstructed more consistently than flexible genome fractions. A high score may therefore coexist with a systematic blind spot for traits that help distinguish strains and explain how microbes respond to their environment.

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

## A more careful reading workflow

No single metric can resolve every limitation, but a few habits improve interpretation:

1. **Match quality criteria to the biological question.** A genome suitable for broad taxonomy may not be sufficient for claims about plasmids, biosynthetic clusters, or strain-specific adaptation.
2. **Inspect assembly structure, not only a summary score.** Contig count, N50, coverage variation, and the placement of key loci can reveal limitations hidden by a headline percentage.
3. **Use complementary quality signals.** Marker-based estimates, taxonomic consistency, read mapping, long-read support, and comparisons with close references answer different questions.
4. **Report uncertainty at the level of the conclusion.** If a relevant pathway is absent, distinguish “not detected” from “biologically absent.”
5. **Treat missingness as potentially biased.** Ask whether the workflow is less likely to recover precisely the class of region under study.

## From quality control to epistemology

The deeper issue is not whether a threshold should be 90%, 95%, or 98%. It is how a computational proxy becomes a biological statement.

A completeness score compresses a complex reconstruction process into a number that helps us make decisions at scale. Good science begins when we unpack that compression: which evidence produced the estimate, which genome fractions were easiest to recover, and whether the remaining uncertainty could change the ecological story.

MAGs have opened an extraordinary window into uncultivated microbial diversity. Reading them well requires both enthusiasm for what they reveal and precision about what they may still leave out.

---

<div class="article-citation">
  <span>Original perspective</span>
  <p>Pellegrinetti, T.A., Molligan, J., Mendes, L.W., Pedrinho, A., &amp; Pérez-López, E. (2026). <em>Rethinking metagenome-assembled genome completeness: are we truly recovering complete genomes?</em> Frontiers in Microbiology, 17, 1884628.</p>
  <a class="profile-button profile-button--primary" href="https://doi.org/10.3389/fmicb.2026.1884628" target="_blank" rel="noopener noreferrer">Read the open-access paper <span aria-hidden="true">↗</span></a>
</div>
