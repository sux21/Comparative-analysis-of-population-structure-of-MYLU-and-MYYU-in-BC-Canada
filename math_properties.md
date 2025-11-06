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

Another equation can be derived from definition:
```math
\begin{aligned}
DX &= E(X-EX)^2 \\
   &= E(X^2 - 2XEX + (EX)^2) \\
   &= EX^2 - 2EXEX + (EX)^2 \\
   &= EX^2 - 2(EX)^2 + (EX)^2 \\
   &= EX^2 - (EX)^2
\end{aligned}
```

## Properties

1. $DC = 0$

2. $D(X+C) = DX$

3. $D(CX) = C^2 DX$

4. $D(kx+b) = k^2 DX$

5. $\text{X, Y are independent, } D(X \pm Y) = DX \pm DY$


# Covariance
## Definition

```math
Cov(X,Y) = E[(X - EX)(Y - EY)]
```

Another equation can be derived from definition:
```math
\begin{aligned}
Cov(X,Y) &= E[(X - EX)(Y - EY)] \\
         &= E(XY - XEY - YEX + EXEY) \\
         &= E(XY) - EYEX - EXEY + EXEY \\
         &= E(XY) - EXEY
\end{aligned}
```

Another equation:
```math
D(X \pm Y) = DX \pm DY \pm 2Cov(X,Y)
```
















