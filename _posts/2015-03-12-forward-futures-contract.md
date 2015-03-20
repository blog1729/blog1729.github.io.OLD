---
layout: post
title: Forward and Futures Contract
comments: True
---
[^reference]
**Forward contract** An agreement to buy or sell an asset on a fixed date in the future, called the *delivery time*, for a price specified in advance, called the *forward price*.

**Short forward position** The party who agrees to sell the asset is said to be taking a *short forward position*. The other party, who agrees to buy the asset at delivery, is said to have a *long forward position*.

**Notations** The time at which forward contract is exchanged is $0$, delivery time $T$, and the forward price $F(0,T)$. The time $t$ market price of the asset be $S(t)$. (No payment is made by any party at time $0$, when the forward contract is exchanged). The payoff at delivery is $S(T)-F(t,T)$ for a long forward position and $F(t,T)-S(T)$ for a short forward position.

## Forward price

Let $r$ denote risk free rate under continuous compounding which is assumed to be constant throughout.

>**Theorem** For a stock paying no dividends, the forward price is
>
> $$F(0,T) = S(0) e^{rT}$$
>
> if the contract is initiated at a time $t<T$, then $F(t,T) = S(t)e^{r(T-t)}$.

The proof of the above theorem can be easily done using no-arbitrage principle.

>**Theorem** The forward price of a stock paying dividend $d$ at time $t$, where $0<t<T$, is
>
>$$F(0.T) = [S(0) - e^{-rt}d]e^{rT}$$

The proof of the above theorem can also be done using no-arbitrage principle. The above formula can be generalized to the case when dividends are paid more than once:

$$F(0,T) = [S(0) - d_0]e^{rT},$$

where $d_0$ is the present value of all dividends due during the lifetime of the forward contract. 

## Dividend yield

Dividends are often paid continuously, with an interest $r_d>0$, the interest is called *(continuous) dividend yield*.

> **Theorem** The forward price for stock paying dividends continuously at a rate $r_d$ is
>
> $$ F(0,T) = S(0)e^{(r-r_d)T}$$
>
> In general, if the contract is initiated at time $t<T$, then
>
> $$F(t,T) = S(t)e^{(r-r_d)T}$$

## Value of forward contract

The value of a forward contract can be defined as the price one has to pay currently to initiate the forward contract $F(0,T)$. Every forward contract has value zero, when initiated. As the price of the commodity changes, the value of the forward contract too, changes. In particular, at delivery time, the value of a long forward contract is $S(T) - F(0,T)$. The value, of course, can be zero, positive and negative.

> **Theorem** For any $t$ such that $0 \le t \le T$ the time $t$ value of a long forward contract with forward price $F(0,T)$ is given by
>
> $$V(t) = [F(t,T) - F(0,T)]e^{-r(T-t)}$$

It should be noted that the above theorem works fine even if there is dividends involved! Now, for a stock paying no dividends, we see that $V(t) = S(t) - S(0)e^t$.[^1]

# Futures

One of the the two parties of a forward contract will be losing money (unless the payoff at $T$ is $0$). Futures contracts are designed to eliminate such risk. It costs nothing to initiate a futures position.

A *futures contract* involves an underlying asset and a specified time of delivery, a stock with prices $S(n)$ for $n=0,1,\cdots$ and time $T$. In addition to the usual stock prices, the market dictates the so called *futures prices* $f(n,T)$ for each step $n=0,1,\cdots$ such that $n\tau \le T$. A futures contract involves a random cash flow, known as *marking to market*. Namely, at each time set $n=1,2,\cdots$ such that $n\tau \le T$, the holder of a long futures position will receive the amount

$$f(n,T) - f(n-1,T)$$

if positive, or will have to pay it if negative. The opposite payments apply for a short futures account. We impose the following two conditions:

 1. The futures price at delivery is $f(T,T) = S(T)$.
 2. At each time step $n=0,1,\cdots$ such that $n\tau \le T$ the value of a futures position is zero.

## Working

* **Initial margin**: Each investor entering into a futures contract has to pay a deposit, called the initial margin, which is kept at the clear house as a collateral. Typically, a fixed percentage of current price of the stock.
* In case of a long futures position, the amount $f(n,T)-f(n-1,T)$ is added to the deposit if positive or subtracted if negative at each time step $n$ (the negative amount is added or subtracted in case of a short futures account).
* **Maintenance margin**: If the deposit falls below a certain level, known as maintenance margin, the clearing house will issue a *margin call*, requesting the investor to make a payment and restore the deposit to the level of *initial margin*.
* The futures position can be closed at any time, in which case the deposit will be returned to the investor. In particular, if the investor fails to respond to the margin call, the clearing house will forcefully close the account.

## Pricing of $f$

> **Theorem** If the interest rate is constant, then $f(0,T) = F(0,T)$.
> In an economy with constant interest rates $r$.

## Hedging with futures

It is possible to hedge risk associated with a stock by using the futures market, i.e., if you wishes to sell the stock at some point in the future, using a futures account can minimize the risk associated with this.

The difference between the spot and futures prices is called the *basis*:

$$ b(t,T) = S(t)- f(t,T)$$

Clearly, the Basis converges to zero as $t\rightarrow T$. In a market with constant interest rates, it is given explicitly by

$$ b(t,T) = S(t)(1-e^{r(T-t)}$$

Similarly, if the asset pays dividends at the rate $r_d>r$, then the basis is positive and is given by

$$ b(t,T) = S(t)(1-e^{(r-r_d)(T-t)})$$

### Hedging with $N$ futures account

We may invest in $N$ futures account to decrease the risk. In this case, the basis is given by $b_{N}(t,T) = S(t) - N f(t,T)$ and hence the variance is:

$$ \text{Var}(b_N(t,T)) = \sigma_s^2 + N^2\sigma_f^2 - 2 N\sigma_s \sigma_f \rho$$

and the quadratic expression has a minimum at

$$ N = \rho \frac{\sigma_s}{\sigma_f}.$$

This ration is known as **optimal hedge ratio**. If the interest rate is constant, it can be easily shown that $N = e^{-r(T-t)}$.

### Futures on stock index

A **stock exchange index** is a weighted average of a selection of stock prices with weights proportional to the market capitalization of stocks. An index of this kind is approximately proportional to the market portfolio. We can treat index as a security, for the purpose of the futures market.



* * * 

[^1]: <small> Some parts, before section 6.2 Futures are skipped </small>
[^reference]: **Reference** Mathematics for finance, an introduction to financial engineering. 