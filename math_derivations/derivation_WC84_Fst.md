# Derive equation 10 of the article "Estimating F -statistics for The Analysis of Population Structure"

## Sampling model
There is a single ancestral population in Hardy-Weinberg equilibrium and linkage equilibrium. A number of, r, populations of the same size descend from this ancestral population, and each population is also in Hardy-Weinberg equilibrium and linkage equilibrium. Samples of alleles collected from these descendent populations differ because of both genetic sampling (genetic drift) and statistical sampling (collect samples from a population).   

## 1. Derive components of variance (Ea, Eb, Ec) and equation 1
Originally derived in the article "Analyses of gene frequencies"

### Assumptions: diploid organism, one locus, two alleles
Let $a_{ij}$ represent an index of jth allele in ith individual. 

Define gene frequency $x_{ij}$: 

```math
x_{ij} =
  \begin{cases}
    1       & \quad \text{if } a_{ij} = A, \\
    0       & \quad \text{if } a_{ij} \neq A.
  \end{cases}
```

Let population frequency of allele A be $P(a_{ij}=A) = p$. <br>
Let inbreeding coefficient (probability of two alleles being identical by descent in one individual) be $F$. <br>
Let probability of two alleles being identical by descent be $P(a_{ij} = a_{kl})$.  

Probability of two alleles in individual i being both A (can be identical by descent or not identical by descent) = $P(a_{i1} = A, a_{i2} = A) = P(a_{i1} = A) P(a_{i2} = A | a_{i1} = A) = p[F_{i} + (1-F_{i})p]$.

Probability of any two alleles in any individuals being both A (can be identical by descent or not identical by descent) = $P(a_{ij} = A, a_{kl} = A) = P(a_{ij} = A) P(a_{kl} = A | a_{ij} = A) = p[P(a_{kl} \equiv a_{kl}) + (1-P(a_{kl} \equiv a_{kl}))p]$. 

For random genes,

```math
Ex_{ij}=1 \cdot p + 0 \cdot (1-p) = p
```

```math
Ex_{ij}^2 = 1^2 \cdot p + 0 \cdot (1-p) = p
```

```math
\begin{aligned}
\sigma_{x_{ij}}^2 &= E[(x_{ij} - Ex_{ij})^2] \\
                  & = E[x_{ij}^2 - 2x_{ij}Ex_{ij} + (Ex_{ij})^2] \\
                  & = Ex_{ij}^2 - 2Ex_{ij}Ex_{ij} + (Ex_{ij})^2 \\
                  & = Ex_{ij}^2 - 2(Ex_{ij})^2 + (Ex_{ij})^2 \\
                  & = Ex_{ij}^2 - (Ex_{ij})^2 \\
                  & = p^2 -p \\
                  & = p(1-p)
\end{aligned}
```

```math
\begin{aligned}
\sigma_{x_{i1}x_{i2}} &= Ex_{i1}x_{i2} - Ex_{i1}Ex_{i2} \\
                      &= 1 \cdot P(a_{i1} = A, a_{i2} = A) + 0 \cdot P(a_{i1} = A, a_{i2} = A) - p \cdot p \\
                      &= p[F_{i} + (1-F_{i})p] - p^2 \\
                      &= pF_{i} + p^2 - p^2 F_{i} - p^2 \\
                      &= pF_{i}(1-p)
\end{aligned}
```

```math
\begin{aligned}
\sigma_{x_{ij}x_{kl}} &= Ex_{ij}x_{kl} - Ex_{ij}Ex_{kl} \\
                      &= 1 \cdot P(a_{ij} = A, a_{kl} = A) + 0 \cdot P(a_{ij} = A, a_{kl} = A) - p \cdot p \\
                      &= p[P(a_{kl} \equiv a_{kl}) + (1-P(a_{kl} \equiv a_{kl}))p] - p^2 \\
                      &= pP(a_{kl} \equiv a_{kl}) + p^2 - p^2 P(a_{kl} \equiv a_{kl}) - p^2 \\
                      &= pP(a_{kl} \equiv a_{kl})(1-p)
\end{aligned}
```

Mean allele frequency of allele A in a sample of $N$ diploid individuals:

```math
\hat{p} = \bar{x}_{..} = \frac{\sum_{i=1}^{N} \sum_{j=1}^{2} x_{ij}}{2N}
```

Variance of this allele frequency of the sample can be calculated:

```math
\begin{aligned}
\sigma_{\hat{p}}^2 &= \sigma^2 (\frac{\sum_{i=1}^{N} \sum_{j=1}^2 x_{ij}}{2N}) \\
                   &= \frac{1}{4N^2} \sigma^2 (\sum_{i=1}^{N} \sum_{j=1}^2 x_{ij}) \\
                   &= \frac{1}{4N^2} \sigma^2 (x_{11} + x_{12} + x_{21} + x_{22} + \cdots) \\
                   &= \frac{1}{4N^2} [\sigma_{x_{11}}^2 + \sigma_{x_{12}}^2 + \sigma_{x_{21}}^2 + \sigma_{x_{22}}^2 + \cdots + 2 \sigma_{x_{11}x_{12}} + \sigma_{x_{21}x_{22}} + \cdots + 2 \sigma_{x_{11}x_{21}} + 2 \sigma_{x_{11}x_{22}} + \cdots] \\
                   &= \frac{1}{4N^2} [\sum_{i=1}^N \sum_{j=1}^2 \sigma_{x_{ij}}^2 + 2 \sum_{i=1}^N \sigma_{x_{i1}x_{i2}} + 2 \sum_{i<k}^N \sum_{j=1}^2
\end{aligned}
```

                   &= \frac{1}{4N^2} [\sum_{i=1}^N \sum_{j=1}^2 \sigma_{x_{ij}}^2 + 2 \sum_{i=1}^N \sigma_{x_{i1}x_{i2}} + 2 \sum_{i<k}^N \sum_{j=1}^2 \sum_{i=1}^2 \sigma_{x_{ij}x_{kl}}] 

References: <br>
1. Weir, Bruce S., and C. Clark Cockerham. "Estimating F-statistics for the analysis of population structure." evolution (1984): 1358-1370.
2. Cockerham, C. Clark. "Analyses of gene frequencies." Genetics 74.4 (1973): 679.

































