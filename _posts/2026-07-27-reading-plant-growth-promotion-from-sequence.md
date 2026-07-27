---
layout: research-note
title: "From sequence data to plant-growth hypotheses"
description: "How PGPg_finder turns genomes and metagenomes into testable hypotheses about microbial traits that may support plant growth."
date: 2026-07-27
categories:
  - research-notes
tags:
  - bioinformatics
  - rhizosphere
  - scientific software
author_profile: false
read_time: true
share: false
related: false
paper_url: "https://doi.org/10.1016/j.rhisph.2024.100905"
paper_label: "Based on our 2024 software paper"
note_topic: "Bioinformatics & plant microbiomes"
summary: "PGPg_finder searches genomes and community data for more than 800 plant growth-promoting traits, helping move from long gene lists to ecological questions that can be tested."
paper_highlight: "Scientific software · 43 OpenAlex citations"
---

Plant-associated sequencing projects routinely produce thousands—or millions—of predicted genes. The difficult step is not generating that inventory. It is deciding which genes might help explain how a microbial community acquires nutrients, tolerates stress, competes in the rhizosphere, or influences a host plant.

**PGPg_finder** was built to make that interpretive step more systematic. The pipeline searches genomic, metagenomic, and metatranscriptomic data for traits associated with plant growth promotion, then organizes the results into biologically meaningful categories.

<aside class="article-pullquote">
  <span>Key idea</span>
  <p>A functional annotation is most useful when it becomes a testable ecological hypothesis—not when it is treated as proof of a phenotype.</p>
</aside>

## A vocabulary for plant–microbe functions

Plant growth promotion is not a single mechanism. It can involve nutrient acquisition, phytohormone modulation, protection against oxidative stress, competition with pathogens, biofilm formation, or changes in the chemical environment around the root.

PGPg_finder brings more than 800 plant growth-promoting traits into one curated analytical framework based on PLaBAse. Instead of manually searching annotations for many disconnected gene names, a researcher can ask whether a genome or microbial community carries coherent sets of functions related to:

- nitrogen, phosphorus, sulfur, or iron metabolism;
- hormone production and modulation;
- stress tolerance and detoxification;
- root colonization, motility, and biofilm formation;
- antimicrobial activity and microbial competition.

The pipeline accepts both assembled sequences and workflows that begin from raw data. That matters because plant microbiome projects operate at different resolutions: an isolate genome can reveal the repertoire of one strain, whereas a metagenome describes the collective potential of a community.

## What a pipeline changes

Automation is not only about speed. A reproducible workflow makes the same criteria available across samples, projects, and research groups. It records which databases and thresholds were used, reduces ad hoc decisions, and makes comparisons easier to audit.

In the original study, we tested PGPg_finder with five rhizobacterial strains and with metagenomes from Amazon forest and pasture soils. The resulting profiles recovered lineage-specific functions in the isolates and differences in plant-associated functional potential between environments.

Those results illustrate a useful change in scale. A strain can be described as a candidate inoculant; a soil community can be compared across land uses; and both can be interpreted through a common functional vocabulary.

<div class="article-comparison" role="group" aria-label="Two levels of interpretation with PGPg_finder">
  <div>
    <span class="article-comparison__label">Genome or isolate</span>
    <strong>Who could perform the function?</strong>
    <p>Link a trait repertoire to a cultured strain or reconstructed genome.</p>
  </div>
  <div>
    <span class="article-comparison__label">Community data</span>
    <strong>Where is the potential enriched?</strong>
    <p>Compare functional profiles across soils, treatments, hosts, or time points.</p>
  </div>
</div>

## Presence is not expression—and expression is not effect

Finding a gene does not establish that it is expressed under a particular condition. Detecting a transcript does not prove that the encoded process changes plant performance. Even a complete pathway can behave differently depending on substrate availability, microbial interactions, spatial organization, and the host genotype.

The best use of a functional screen is therefore directional. It can prioritize strains for experiments, identify pathways for targeted quantification, or show where contrasting communities deserve closer study. Validation may then involve gene expression, metabolite measurements, mutant analysis, synthetic communities, or plant phenotyping.

This distinction also protects against a common form of overinterpretation: equating a familiar annotation with an ecological role. Genes are reused across contexts, reference databases are incomplete, and many plant-associated effects emerge from interactions rather than from a single marker.

## From catalogues to experiments

A good bioinformatics tool reduces a large search space without pretending to eliminate uncertainty. PGPg_finder narrows millions of sequences into a structured set of candidate mechanisms. The researcher still decides which mechanisms are plausible in the environmental context and which experiment could distinguish among them.

That is the deeper value of scientific software in microbiome research. It does not replace biological reasoning. It gives that reasoning a reproducible starting point.

---

<div class="article-citation">
  <span>Original publication</span>
  <p>Pellegrinetti, T.A., Monteiro, G.G.T.N., Lemos, L.N., Santos, R.A.C., Barros, A.G., &amp; Mendes, L.W. (2024). <em>PGPg_finder: a comprehensive and user-friendly pipeline for identifying plant growth-promoting genes in genomic and metagenomic data.</em> Rhizosphere, 30, 100905.</p>
  <a class="academic-button" href="https://doi.org/10.1016/j.rhisph.2024.100905" target="_blank" rel="noopener noreferrer">Read the paper <span aria-hidden="true">↗</span></a>
</div>
