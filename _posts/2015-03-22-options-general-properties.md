---
layout: post
title: Options General Properties
comments: True
---

## Definitions

* **European call option** is a contract giving the holder the right to **buy an asset**, called the underlying, for a price $X$ fixed in advance, known as *exercise price* or *strike price*, at a specified time $T$, called the *exericse* or *expiry* time. Similalry, a *European put* option gives the right to sell the underlying asset for the strike price $X$ at the exercise time $T$.

* **American call option** or put option gives the right to buy or, respectively, to sell the underlying asset $X$ for the strike price $X$ at any time between now and a specified future time $T$, called the *expiry time*.

* **Underlying asset**: Apart from the typical assets such as stocks, commodities, or foreign currency, there are options on stock indices, interest rates, or even the snow level at a ski resort. Some underlying asset may be impossible to buy or sell.

* The **payoff** of a European call is given by $(S(T)-X)^{+}$, where we use the notation
$$x^{+} = \left\{ \begin{array}{cl} x& \text{if } x>0 \\ 0 & \text{otherwise.} \end{array} \right.$$
For a put option, the payoff is given by $(X-S(T))^{+}$.

* Since the investor will not lose money under any circumstance, a *premium* has to be paid to enter into an option. The prices of the calls and puts will be denoted by $C_E$ and $P_E$ (for European options) and $C_A$, $P_A$ (for American options).

* The gain of an option buyer at time $T$ is given by (for a European call)

$$ (S(T) - X)^{+} - C_{E}e^{rT}$$

## Put-call parity

>**Theorem** For a stock that pays no dividends the following relation holds between the prices of European calls and put options, both with exercise price $X$ and exercise time $T$:
>
>$$ C_E - P_E = S(0) - Xe^{rT} $$

The above result can easily be shown using the no-arbitrage principle. By making an equivalence with the forward contracts, we can prove the following results:

* If the stock pays a dividend of $d_0$ in between $0$ and $T$, then the put-call parity relation is given by

$$ C_E - P_E = S(0) - d_0 - Xe^{-rT} $$

* If the dividends are paid continuously, at a rate $r_d$, then

$$ C_E - P_E = S(0)e^{-r_dT} - Xe^{-rT} .$$

> **Theorem** The prices of Americal put and call options with the same strike price $X$ and expiry time $T$ on a stock that pays no dividends satisfy
>
> $$ S(0) - Xe^{-rT} \ge C_A - P_A \ge S(0) - X $$


## Bounds on option prices

The following inequalities are obvious:

$$ C_E \le C_A, \qquad P_E \le P_A $$

One can also prove the following ones

$$ \begin{align*}
C_E &< S(0) \\
S(0) - Xe^{-rT} &\le C_E \\
P_E &< Xe^{-rT} \\
-S(0)+Xe^{-rT} & \le P_E
\end{align*}$$

For dividend paying stocks, the bounds are

$$ \begin{align*}
\max\{0, S(0) - d_0 - Xe^{-rT}\} &\le C_E \le S(0) - d_0 \\
\max\{0, -S(0)+d_0+Xe^{-rT}\} &\le P_E < Xe^{-rT} \\
\end{align*}$$

