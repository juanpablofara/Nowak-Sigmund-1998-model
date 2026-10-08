# Nowak-Sigmund-1998-model

# Computational Replication of Nowak & Sigmund (1998)

Computational replication in R of the models presented in:

> Nowak, M. A. & Sigmund, K. (1998). *Evolution of indirect reciprocity by image scoring*. Nature, 393, 573–577.

## Overview

This project reproduces the main computational and analytical models developed by Nowak and Sigmund to study the evolution of cooperation through indirect reciprocity.

The central idea is that cooperation can evolve between individuals who may never interact again, provided that individuals use information about the reputation of potential recipients when deciding whether to cooperate.

## Models reproduced

The R Markdown document implements:

- **Figure 1:** Basic image-scoring model.
- **Figure 2:** Selection-mutation dynamics and long-term cycles between cooperation and defection.
- **Figure 3:** Incomplete information and the effect of population size.
- **Figure 4:** AND/OR strategies incorporating the donor's own image.
- **Analytical model 1:** Discriminators vs. defectors.
- **Analytical model 2:** The good, the bad and the discriminating.
- **Analytical model 3:** Unlimited image scores and the critical fraction of initially negative reputations.

## Implementation

The models were implemented from scratch in R using stochastic simulations, evolutionary selection, mutation and replicator dynamics.

The main simulation engine is:

```r
run_ir_simulation()
```

which allows different combinations of:

- population size;
- number of interactions per generation;
- mutation rate;
- benefit and cost of cooperation;
- information quality;
- strategy type;
- image-score range.

The project uses `ggplot2` for visualization.

## Main result

The simulations reproduce the central qualitative result of the original paper: cooperation can be maintained through reputation-based indirect reciprocity when individuals have sufficiently reliable information about the reputation of others.

The simulations also reproduce the role of population size, information quality, mutation and strategic behavior in determining the stability of cooperation.

## Reproducibility

The simulations are stochastic and therefore individual runs may differ depending on the random seed.

For computational convenience, some simulations use fewer generations than the original paper. The R Markdown document specifies the original parameters reported by Nowak and Sigmund and explains where computationally shorter simulations are used.

To reproduce the analysis, open:

`nowak_sigmund_1998_modelos.Rmd`

and knit the document using RStudio.

## Requirements

R and the following packages:

```r
install.packages(c(
  "ggplot2",
  "knitr",
  "gridExtra"
))
```

## Reference

Nowak, M. A. & Sigmund, K. (1998). Evolution of indirect reciprocity by image scoring. *Nature*, 393, 573–577.

https://doi.org/10.1038/31225

## Author

Computational replication project developed in R.
