---
title: 'Research summary - unspread.py'
description: ''
pubDate: 'June 16 2023'
---

# The problem

Sequencing data in single cell sequencing experiments are highly multiplexed. In one sequencing assay - thousands to millions of cells are measured concurrently. Each cell is given a unique combination of known sequences which identify the sequencing reads belonging to that cell. However, it was discovered that some sequencing machines allow these unique barcodes to attach to other DNA molecules present in the assay. As a result, many reads are identified as belonging to the wrong cell, called _index switching_. 

# The solution

For _dual-indexed_ sequencing data, i.e. where cells are identified by a unique combination of two barcodes, I found a solution. By comparing the same cells sequenced on an affected and unaffected sequencing machine, I made the observation that wrongly assigned sequencing reads tend to have one barcode in common with the true source of the read. This allowed me to apply linear algebra to this problem, [the sylvester equation](https://en.wikipedia.org/wiki/Sylvester_equation), which allowed by to recover the unaffected data from the data affected by index switching. The sylvester equation required a rate parameter for correct recovery, which was obtained by a regression model.

# The tools

This project used Python, with the packages numpy, scipy, statsmodels and matplotlib. Integral use of statistical modeling and linear algebra.

All code can be found on github [here](https://github.com/sandberg-lab/Spreading-Correction).

# The impact 

This tool is used in single cell genomics to detect and correct possible index switiching. Especially in fields where even the smallest contamination may affect conclusions (e.g. metagenomics).

# The paper

[Read the paper here](http://dx.doi.org/10.1038/nmeth.4666)