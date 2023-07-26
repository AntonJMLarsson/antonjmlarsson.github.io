---
title: 'Research summary - NASC-seq'
description: ''
pubDate: 'August 11 2022'
---

# The problem

NASC-seq is a method to detect newly transcribed RNA in single cells. The cells in your body contain many protein-coding RNA transcripts which can be translated to perform its function. The regulation of transcription essentially defines the _type_ of the cell, whether it is a neuron, epithelial or muscle cell and so on. However, transcription may also change in response to some kind of perturbation, for example when an immune cell is exposed to material foreign to the body. For this project, we sought out to measure which RNA in the cell is _new_. Our approach was to introduce a slightly different nucleotide than what is endogenous to the cell, called 4sU. 4sU may be incorporated into RNA during transcription, which through the NASC-seq method ultimately result in sequencing reads where newly transcribed RNA contain mismatches to the reference genome after the alignment step.

# The solution

To properly analyze this data, the new and old transcriptomes have to be separated. Together with a series of bioinformatic tools to correctly count the mismatches given sequencing reads aligned to the reference genome, I also implemented a binomial mixture model to estimate the proportion of RNA that is new for a given gene and cell. The mismatches can either be due to new transcription or due to technical error and the binomial mixture model separates these two signals. I also used Expectation-Maximization to estimate the two probabilities used for the two binomial distributions.

# The tools

This project used Python, with the packages _numpy_, _pystan_, _scipy_, _pysam_ and _matplotlib_. Integral use of statistical modeling and probabilistic programming (_STAN_, later implemented using _PyTorch_ and _Tensorflow_).

All code can be found on github [here](https://github.com/sandberg-lab/NASC-seq).

# The impact 

This method has been used to study fundamental biological processes taking place in individual cells.

# The paper

[Read the paper here](https://doi.org/10.1038/s41467-019-11028-9)