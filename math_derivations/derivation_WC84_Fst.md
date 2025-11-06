# Derive equation 10 of the article "Estimating F -statistics for The Analysis of Population Structure"

## Sampling model
There is a single ancestral population in Hardy-Weinberg equilibrium and linkage equilibrium. A number of, r, populations of the same size descend from this ancestral population, and each population is also in Hardy-Weinberg equilibrium and linkage equilibrium. Samples of alleles collected from these descendent populations differ because of both genetic sampling (genetic drift) and statistical sampling (collect samples from a population).   

## 1. Derive components of variance (Ea, Eb, Ec) and equation 1
Original derived in the article "Analyses of gene frequencies"

### Assumptions: diploid organism, one locus, two alleles
Let $a_{ij}$ represent an index of jth allele in ith individual. 

Define $x_{ij}$: 

```math
x_{ij} =
  \begin{cases}
    1       & \quad \text{if } a_{ij} = A, \\
    0  & \quad \text{if } a_{ij} \neq A.
  \end{cases}
```

Let population frequency of allele A be $P(a_{ij}=A) = p$.

For random genes,

```math
Ex_{ij}=1 \cdot p + 0 \cdot (1-p) = p
```












References: <br>
1. Weir, Bruce S., and C. Clark Cockerham. "Estimating F-statistics for the analysis of population structure." evolution (1984): 1358-1370.
2. Cockerham, C. Clark. "Analyses of gene frequencies." Genetics 74.4 (1973): 679.








