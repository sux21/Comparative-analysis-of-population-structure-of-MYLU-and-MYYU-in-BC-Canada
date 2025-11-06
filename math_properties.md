# Expectation
## Definitions

Discrete random variable: 

```math
EX = \sum_{k=1}^{\infty} x_{k}p_{k}
```

Continuous random variable: 

```math
EX = \int\limits_{-\infty}^{+\infty} xf(x) dx
```

## Properties
1. $EC=C$, $C$ is a constant 

2. $E(X+C) = EX+C$

3. $E(CX) = CEX$

4. $E(kx+b) = kEX+b$

5. $E(X \pm Y) = EX \pm EY$

6. $\text{X and Y are independent, } E(XY) = EX \cdot EY$

## Expectation of a function of random variable

Y=g(x)

Y is discrete:

```math
EX = \sum g(x_{k})p_{k}
```

Y is continuous:

```math
EX = \int\limits_{-\infty}^{+\infty} g(x)f(x) dx
```

# Variance
## Definition

```math
DX = E(X - EX)^2
```

Second equation:

```math
\begin{aligned}
DX &= E(X-EX)^2 \\
   &= E(X^2 - 2XEX + (EX)^2) \\
   &= EX^2 - 2EXEX + (EX)^2 \\
   &= EX^2 - 2(EX)^2 + (EX)^2 \\
   &= EX^2 - (EX)^2
\end{aligned}
```
