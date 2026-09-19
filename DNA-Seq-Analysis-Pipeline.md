# DNA-Seq Analysis Pipeline

## Overview

A DNA-seq analysis pipeline is a series of steps used to transform raw sequencing data into biologically meaningful information. One of the most important things I learned is that the pipeline should be designed around the **biological question being investigated**. The research goal influences the experimental design, sequencing platform, data processing, and downstream analysis.

## Main Steps

The pipeline begins with **raw sequencing data**, which can be generated using platforms such as Illumina or PacBio. The raw reads are first assessed using **quality control (QC)**, followed by trimming to remove low-quality bases and adapter sequences.

After preprocessing, the reads can either be **aligned to a reference genome** or used for **de novo genome assembly** when a suitable reference is unavailable. The choice depends on the research question and the characteristics of the sequencing data.

For analyses involving genetic variation, the aligned reads are used for **variant calling** to identify variants such as **single nucleotide polymorphisms (SNPs) and insertions/deletions (indels)**. These variants can then undergo **functional annotation** to determine their potential effects on genes and proteins.

### Basic Workflow

**Raw sequencing data → Quality control → Trimming → Alignment/Assembly → Variant calling → Functional annotation → Biological interpretation**

## Important File Formats

During the analysis, different file formats are used at different stages. **FASTQ** commonly stores raw sequencing reads and their quality scores, while **FASTA** is used for reference or assembled sequences. **SAM/BAM** are used for storing sequence alignments, with BAM being the binary form of SAM. **VCF** is commonly used to store genetic variants, while formats such as **BED, GFF, and GTF** are used for genomic features and annotations.

Some files also require **index files** to allow software to access specific regions efficiently. For example, a BAM file may have a corresponding BAI index.

## Key Takeaways

The main lesson for me is that bioinformatics analysis is not simply about running tools in a particular order. **The biological question should come first**, because it determines the experimental design, sequencing approach, and appropriate analysis pipeline.

I also learned that understanding the characteristics of sequencing platforms is important when designing an experiment. Short-read and long-read technologies have different strengths, and combining sequencing technologies can sometimes be useful, particularly for complex genome assembly.

Finally, understanding file formats, indexing, and coordinate systems is essential for working correctly with genomic data. For example, genomic formats may use either **0-based or 1-based coordinates**, so knowing which system a tool or file uses is important when interpreting genomic positions.

Source: [Wellcome Connecting Science](https://www.futurelearn.com/courses/bioinformatics-for-biologists-analysing-and-interpreting-genomics-datasets/4/todo/208398)
