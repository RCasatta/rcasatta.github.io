---
layout: post
title:  "Flow coin, a market driven pegged sidechain"
---

I am hereby proposing an idea for getting desired properties from both an altcoin and a two-way pegged token.
Let's call it **Flow coin**.

What are the differences between an altcoin and a token based on a sidechain?

### Altcoin

An altcoin is a crypto currency with a stand alone blockchain. During past years a lot of new altcoins were introduced, some with great new features.
After the altcoin-hype, we can now see that just really new users jump on the train of the latest altcoin, even if they have some interesting characteristics in comparison to bitcoin.
The main reason why it is so hard to propose a new coin is the [network effect](https://en.wikipedia.org/wiki/Network_effect).
One medium of exchange is as valuable as more accepted and in blockchain tech is more secure as is more valuable.  

Some proofs of this are the market cap of bitcoin (90% of all cryptos) and the tcp/ip which is the protocol all the internet is using even more recent protocols were probably superior in some ways...

### Sidechain

Then [sidechain](https://blockstream.com/sidechains.pdf) were invented. There are many details but the basic principle is to leverage bitcoin blockchain safeness in a symbiotic relationship with the sidechain.

Sidechain refer to *two way pegging* when bitcoins are frozen to create sidechain tokens that could be exchanged in the sidechain. If the tokens owner wants, he could go back in the mainchain getting back the frozen bitcoins.

### Problems

Suppose tokens are backing some commodities.
The exchange rate is fixed at the beginning of the sidechain. As times goes, commodities price changes in relation to each other but the exchange rate isn't. So everybody wants the token backing the commodities with the greater value.

Another problem is financing innovation. Altcoins developer used initial announcement and IPO to finance development. Unfortunately many use this to scam investor but basically it is something that drives innovation.

### Flow coin

As stated in the [sidechain](https://blockstream.com/sidechains.pdf) paper:

> Two-way peg refers to the mechanism by which coins are transferred between sidechains and
back at a fixed or otherwise deterministic exchange rate.

What if a deterministic exchange rate could be used to enable a market driven price discovery?

Let's define M as the total bitcoin frozen to create Flow coin and F as the total Flow coin in circulation. When moving bitcoin to the sidechain the exchange rate is 1/(M+1) for every step of a bitcoin. The first bitcoin flowing in the sidechain market cap will have an exchange rate of 1:1, the second will have rate 1:½ the third 1:⅓ and so on and so forth.

FLC(A) is the Flow coin balance of Alice and BTC(A) is her bitcoin balance. BTC(B) & FLC(B) are the respective balances for Bob. The rows in the table are in chronological order.


| Who | Transaction          | FLC(A) | BTC(A) | FLC(B) | BTC(B) |    M |    F |
| --- | -------------------- | ------:| ------:| ------:| ------:| ----:| ----:|
|     |                      |   0.00 |   1.00 |   0.00 |   2.00 | 0.00 | 0.00 |
| A   | 1.00 BTC -> 1.00 FLC |   1.00 |   0.00 |   0.00 |   2.00 | 1.00 | 1.00 |
| B   | 1.00 BTC -> 0.50 FLC |   1.00 |   0.00 |   0.50 |   1.00 | 2.00 | 1.50 |
| B   | 1.00 BTC -> 0.33 FLC |   1.00 |   0.00 |   0.83 |   0.00 | 3.00 | 1.83 |
| A   | 0.33 FLC -> 1.00 BTC |   0.66 |   1.00 |   0.83 |   0.00 | 2.00 | 1.50 |

In the last row of the table above, Alice go back to the main chain with 1/3 FLC she gets 1 BTC. She is making a profit entering in the market at the beginning of Flow coin and exiting after more people entered the sidechain.
As long as users find FLC interesting because of feature X they are willing to enter even if the exchange rate is decreasing. If FLC is not promising, users could exit, in the worst case they will change with a 1:1 rate.

With this principle but tweaking the exchange formula at the time of creating the sidechain allows to adapt to various scenarios. In any case buyers & sellers know in advance the formula and the rules.

One consideration is that the bitcoin frozen when entering the sidechain will not necessarily be unfrozen with the same Flow coins. In a federated sidechain this isn't a problem because the fiduciaries will follow the mathematical rules established.
At the time of writing, federated sidechain are the only viable option so this isn't a big issue for now.

In the case of an entity releasing shares legally pegged to the Flow coin the price of the coin will follow the one of the shares because of the arbitrage opportunities.


### Conclusion

By defining a deterministic formula we can create a pegged token with market driven price discovery.
