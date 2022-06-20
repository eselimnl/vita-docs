(Figure-2)=
```{image} images/workflow.svg
:alt: workflow
:class: bg-primary
:width: 1000px
:align: center
```

## How does it work?

User uploads aligned FASTA file of the virus of interest to ViTA. ViTA then uses the DiMA tool ([https://doi.org/10.48550/arxiv.2205.13915](https://doi.org/10.48550/arxiv.2205.13915)), embedded within the ViVA system, to extract historically conserved sequences (HCS). Briefly, DiMA is designed to facilitate the dissection of sequence diversity dynamics for viruses. As a base, DiMA provides a quantitative overview of sequence diversity by use of Shannon's entropy, applied via a user-defined k-mer sliding window to an input alignment file. Distinctively, the key feature is that DiMA interrogates diversity dynamics by dissecting each k-mer position to various diversity motifs, defined based on the incidence of distinct sequences ([see next section])(Section_diversity). DiMA identifies HCSs across the input alignment length, selected based on a user-defined index incidence threshold (default: 100%). Selected index sequences that overlap or are immediately adjacent in their k-mer positions are concatenated as longer sequences. An HCS of 80% or higher incidence may be attractive for further consideration as an intervention target. The HCS are then further annotated by using of various bioinformatics tools: structure-function annotation, immune-relevance, virus coverage (intra-species analysis), and virus specificity (inter-species analysis).

## Defining diversity motifs
(diversity_motifs)=
For a given sequence alignment, all sequences at each of the aligned *k-mer* positions are quantified for distinct sequences and ranked-classified into diversity motifs based on their incidences, as described in Hu et al. (2013)(PMID: 23593157).

```{image} images/diversity_motifs.svg
:alt: diversitymotifs
:class: bg-primary
:width: 300px
:align: center
```
<a></a> 
: **Figure 1. Definitions of diversity motifs.** The ‘‘Index’’ nonamer is the most prevalent sequence, present in 8 of the 20 isolates. The ‘‘Major’’ variant is the most common variant of the index (5/20). ‘‘Minor’’ variants are multiple different repeated sequences, each with incidences less than the major variant. ‘‘Unique’’ variants are those represented by a single aligned sequence. Distinct variant sequences at a given nonamer position are the different sequence at the position; in this example one of major, two of minor, and three of unique.
(section-two)=

