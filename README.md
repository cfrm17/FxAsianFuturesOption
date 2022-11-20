# Asian Futures Option Valuation


A commodity Asian Futures option is a vanilla Asian option on one or several commodity futures. The matured payoff of the Asian option depends on an arithmetic average of the underlying futures prices over a specified set of reset dates. The pricing model of the Commodity Asian Futures Option is used for pricing, marking-to-the-market (P&L) and risk number calculations. 

The complexity of the distribution of the matured payoff makes its pricing in full explicit analytical exact solution form almost impossible. The most common approach is by using Monte Carlo simulation, which is rather time consuming and is not appropriate for risk management purposes, either. In this article, a close-form analytical approximation for pricing the Asian option, named modified Levy model, is applied and implemented.

The Asian option on futures is of European type vanilla arithmetic average call/put option on futures
prices. The term of “vanilla arithmetic average” means that weighting factors in the average are of
constant and positive. The matured payoff of the Asian option is the arithmetic average of one or several
futures prices over a preset period of reset time points. Assume the current time is zero. Let k _ 1 be a
given positive integer, which is the number of underlying futures contracts of the option, {!A1 , · · · , !Ak } be a set of positive weighting factors such that

 

be a set of reset time points, {!(1)1 , · · · , !m2(mj ) : j = 1, · · · , k} be a set of positive weighting factors
such that

 

Without the loss of generality, we may assume t(1)1 > 0. Let F(j) be the jth futures price process. In a
dual-currency market, suppose that all futures prices are measured in a currency Cu and the option value
and matured payoff are measured in another currency Cv. Let Xt be the currency exchange rate which
is in a number of units of Cv per unit of Cu at a time of t _ 0. Let T _ t(k)mk be a payment time of the
option. Then the matured payoff of the option at the payment time of T is given by

 

where N is the volume, _ is the call-put index, K is a strike, and . Clearly, we have

 

A single-currency market is a special case of a dual-currency market, in which just simply set Xt _ 1.
Let us define

 

Then the foreign futures F(j) becomes also a tradable asset ˆ F(j) in the domestic market Cv. Let ru and
rv be the riskless short rates (see https://finpricing.com/lib/FiBondCoupon.html ) in Cu and Cv, respectively. Then, for a fixed j 2 {1, · · · , k}, under the
Cv-risk neutral measure, we have

 

where _e = (_x, 0)>, _a = (__(j)f ,p1 − _2_(j)f )>, W(j) is a standard 2D-Wiener process under the measure, _x is the volatility of X, _(j)f is the volatility of F(j), and _ is the correlation coefficient between driving forces of X and F(j). One should know that the “quanto” equation is derived from the dynamics of F(j) under the Cu-risk neutral measure which is given by

 

where W(j) is a standard 1D-Wiener process under the measure, since F(j) is a strictly positive martingale
under that measure. Now, simply applying Ito’s lemma, from equations (3) and (4), we have, under
the Cv-risk neutral measure,

 

where W(j) is a standard 1D-Wiener process under the measure and

 

is called the (instantaneous) volatility of ˆ F(j). If the dual-currency market is degenerated to a single currency market, then _x = 0, _ = 0, rv = ru, and equation (6) is simply reduced to equation.







