---
title: 'Research summary - stitcher.py'
description: ''
pubDate: 'July 10 2022'
---

# The problem

Unprocessed RNA transcripts are composed of introns and exons, where the exons are _spliced_ together to form the mature transcript. Recent research have shown that each gene can undergo what is known as _alternative splicing_, where the available exons are spliced in various combinations. These splicing differences may have dramatic impact on the function the resulting protein can perform. We wanted to use widely available short-read sequencing technology to measure this variation in splicing across individual cells. The approach we chose was _in silico_ reconstruction of RNA using advanced biotechnology methods.

# The solution

In the wetlab method _stitcher.py_ is meant for, the end of each RNA molecule is tagged by a unique sequence (UMI). _stitcher.py_ can then group the resulting sequencing reads based on the UMI sequence, each read hopefully covering more of the original molecule sequence. The software can then calculate the most likely nucleotide sequenced on each position based on probabilistic measurements across all reads (known as the PHRED score). Once the RNA sequence has been, at least partially, reconstructed it can be assigned to a equivalence class of compatible splice variants.

# The tools

This project used Python, with the packages _numpy_, _scipy_ and _pysam_. Thorough understanding of the Sequencing Alignment/Map format.

All code can be found on github [here](https://github.com/AntonJMLarsson/stitcher.py).

# The impact 

This method has the potential to help uncover characterize fundamental aspects of human cell biology.

# The paper

[Read an associated paper here](https://doi.org/10.1038/s41587-020-0497-0)