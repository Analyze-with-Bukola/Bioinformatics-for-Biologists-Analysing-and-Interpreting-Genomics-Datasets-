# Bioinformatics-for-Biologists-Analysing-and-Interpreting-Genomics-Datasets-
Analyzing and Interpreting Genomic Datasets
## Key Topics
1. Next-generation sequencing, its significance and different file formats used.
2. How to run different commands on the UNIX command line for sequence quality control, mapping, and variant calling.
3. Concepts of workflows and workflow management systems such as Nextflow
4. How to install Nextflow and use the existing viralrecon pipeline from the nf-core project.
5. Set up a samplesheet to be used as input for viralrecon
6. Examined the outputs from viralrecon and explain how these could be used to decide whether the data we analysed was of sufficient quality for downstream analyses.
## My Bioinformatics Setup
1. Ubuntu (Linus)
2. MIniConda
3. GitBash
# NGS Sequencing Technologies

## Overview

Next-generation sequencing (NGS) refers to high-throughput sequencing technologies that allow DNA and RNA to be analysed rapidly and at a large scale. In this module, I learned about three major sequencing technologies: **Illumina, PacBio, and Oxford Nanopore Technologies (ONT)**. The main difference between them is how they detect nucleotide sequences and the length of reads they produce.

## Illumina Sequencing: Short Read Sequencer

Illumina is a **short-read sequencing** technology based on **Sequencing by Synthesis (SBS)**. DNA is fragmented and attached to a solid surface, where the fragments are amplified. Fluorescently labelled nucleotides are then incorporated during DNA synthesis, and the emitted signals are detected to determine the sequence.

Illumina is known for its **high accuracy, high throughput, and relatively low cost per base**. Reads are typically around 50–300 base pairs long. It is widely used for applications such as whole-genome sequencing, whole-exome sequencing, RNA-seq, ChIP-seq, and amplicon sequencing. However, because the reads are short, repetitive and structurally complex regions of genomes can be difficult to resolve.

## PacBio Sequencing: Long Read Sequencer

**Pacific Biosciences (PacBio)** uses **Single-Molecule Real-Time (SMRT) sequencing**, which produces long reads. DNA polymerase is positioned inside a small optical structure called a **Zero-Mode Waveguide (ZMW)**, where nucleotide incorporation is detected through fluorescence in real time.

One important feature of PacBio is its ability to sequence circular DNA molecules multiple times. These repeated observations can be combined to produce a highly accurate **Circular Consensus Sequence (CCS)**, also known as a HiFi read. The long and accurate reads make PacBio particularly useful for **de novo genome assembly, structural variant detection, full-length transcript sequencing, and resolving repetitive genomic regions**.

## Oxford Nanopore Technology (ONT): Long Read Sequencer

**Oxford Nanopore Technology (ONT)** is another long-read sequencing technology, but it works differently from Illumina and PacBio. Instead of detecting fluorescence, ONT detects **changes in electrical current** as nucleic acids pass through a nanopore embedded in a membrane.

A motor protein controls the movement of the DNA or RNA through the nanopore. As different bases pass through the pore, they produce characteristic changes in the electrical current. These changes are analysed to determine the nucleotide sequence.

ONT is particularly useful when **very long reads, rapid sequencing, or real-time data generation** are important. It can be applied to genome assembly, metagenomics, structural variant detection, full-length transcript sequencing, and analysis of complex genomic regions.

## Short-Read vs Long-Read Sequencing

The main distinction I learned is that **Illumina produces short, highly accurate reads, while PacBio and ONT produce much longer reads**. Short reads are cost-effective and supported by a large range of established bioinformatics tools, making Illumina useful for many high-throughput applications. However, they can have difficulty spanning repetitive or complex regions.

Long-read technologies provide much more sequence information from each individual molecule. This makes them particularly valuable for **de novo genome assembly, structural variation, repetitive regions, and full-length transcripts**. The choice between short- and long-read sequencing therefore depends on the biological question, the type of genomic information required, and the downstream analysis.

## Key Takeaway

The key concept I took from this topic is:

**Sequencing technology → read characteristics → bioinformatics workflow → biological interpretation**

Illumina can be remembered as **short reads and fluorescence-based sequencing**, PacBio as **long reads and real-time polymerase activity**, and ONT as **long reads and electrical signals through a nanopore**.

Understanding these differences is important in bioinformatics because the sequencing technology determines the type of data generated and influences how the data should be processed and analysed.
