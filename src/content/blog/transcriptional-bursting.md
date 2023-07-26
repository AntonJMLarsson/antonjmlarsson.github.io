---
title: 'Research summary - Transcriptional bursting'
description: ''
pubDate: 'March 21 2021'
---

# The problem

Transcription of RNA occurs in bursts, but this process is difficult to measure. We thought using data from single-cell RNA sequencing held promise to understand transcriptional bursting.

# The solution

I developed set of inference tools to obtain rate parameters for the _two-state model_ of transcriptional bursting. These inferred rates were then used to study a variety of interesting biological phenomena, which include a large range of other analyses and approaches.

# The tools

This project used Python, with the packages numpy, scipy and lots of other assorted packages. Required expert knowledge in statistical modeling and inference methods.

Code can be found on github [here](https://github.com/sandberg-lab/txburst) and [here](https://github.com/sandberg-lab/aRME_and_bursting). Also on Sourceforge [here](https://sourceforge.net/projects/kinetics-of-x-upregulation).

# The impact 

This method has uncovered fundamental prinicples of human cell biology.

# The paper

Read the multiple papers: 
* [On the inference method and application to regulatory sequences](https://doi.org/10.1038/s41586-018-0836-1)
* [Monoallelic expression](https://doi.org/10.1371/journal.pcbi.1008772)
* [X-chromosome upregulation](https://doi.org/10.1038/s41594-019-0306-y)