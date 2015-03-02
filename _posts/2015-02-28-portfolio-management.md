---
layout: post
title: Portfolio Management
comments: True
---

The return on a risky invesment may be measured using the expected value or $E(X)$, where $X$ is the random varaible that represent the amount of money to be received at the end. Risk may be measured by the variance of the random variable corresponding to return. Alternatively, one can also use the standard deviation which in certain cases is more convenient (when compared to variance) since the unit is same as the unit of return.

## Two securities

Let us prepare a portfolio $V$ whose value at time $t$ is given by $V(t)$ and consider two stocks $S_1$ and $S_2$ whose values at time $t$ is represented by $S_1(t)$ and $S_2(t)$ and define weights $w_1$ and $w_2$ by 
$$ w_1 = \frac{x_1 S_1(0)}{V(0)}, \quad w_2 = \frac{x_2 S_2(0)}{V(0)},$$ 
where $x_1$ and $x_2$ are share numbers of stock $1$ and stock $2$.

One can easily observe that $w_1+w_2 = 1$. If short-selling is allowed (borrowing of stock), the value of one of the weight can be negative and the other greater than $100%$.

<blockquote>
<b>Proposition</b>

The return $K_v$ on a portfolio consisting of two securities is the weighted average
$$K_v = w_1K_1 + w_2K_2,$$
where $w_1$ and $w_2$ are the weights and $K_1$ and $K_2$ the returns on the two components.
</blockquote>

The proof of the above proposition is trivial and hence omitted. Similarly, one can easily see the following equation regarding the expected return
$$ E(K_V) = w_1E(K_1)+w_2E(K_2).$$

<blockquote>


The variance of the return on a portfolio is given by
$${\operatorname{Var}}(K_V) = w_1^2 {\operatorname{Var}}(K_1) + w_2^2{\operatorname{Var}}(K_2) +  2w_1w_2{\operatorname{Cov}}(K_1,K_2).$$
</blockquote>

<blockquote>
<b>Theorem</b>

The variance $\sigma^2_V$ of a portfolio cannot exceed the greater of the variances $\sigma_1^2$ and $\sigma_2^2$ of the components,
$$\sigma_v^2 \le \max\{\sigma_1^2, \sigma_2^2\},$$
if short sales are not allowed.
</blockquote>

The proof of the above theorem easily follows from the fact that ${\operatorname{Cov}}(K_1,K_2) \le \sigma_1\sigma_2$. If short-selling is allowed there are examples for which the theorem is not true.

<blockquote>
If $\rho_{12}=1$, the correlation coefficient is $1$, then we can achieve $\sigma_v = 0$ when $\sigma_1 \neq \sigma_2$ under the weights
$$ w_2 = -\frac{\sigma_2}{\sigma_1 - \sigma_2}, \quad w_2 = \frac{\sigma_1}{\sigma_1 - \sigma_2}$$
(Short sales are necessary, since either $w_1$ or $w_2$ are negative.)

If $\rho_{12}=-1$, then $\sigma_V = 0$ for 
$$w_1 = \frac{\sigma_2}{\sigma_1+\sigma_2}, \quad w_2 = \frac{\sigma_1}{\sigma_1+\sigma_2}.$$
(No short sales are necessary, since both $w_1$ and $w_2$ are positive.)
</blockquote>

The last theorem can be easily verified.
## References

1. Mathematics for finance, Marek Capinski and Thomasz Zastawniak.
