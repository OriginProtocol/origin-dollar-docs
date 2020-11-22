# FAQ

## Dove posso acquistare OUSD?

Dai un'occhiata a [Guida introduttiva](https://docs.ousd.com/getting-started) per vedere una varietà di opzioni.

## Quali sono i costi per coniare e riscattare OUSD?

Come con qualsiasi transazione Ethereum, avrai bisogno di Ether per interagire con lo smart contract OUSD. Abbiamo adottato misure per ridurre il consumo di gas ove possibile, ma questi costi possono variare.

Ogni volta che coni o riscatti OUSD, verrà applicato un tasso di cambio alle tue stablecoin depositate o ritirate. Puoi saperne di più visitando [Oracoli di Prezzo](https://docs.ousd.com/core-concepts/price-oracles).

To encourage long-term holding of OUSD and to protect the protocol from attackers, an exit fee of 0.5% is charged on all redeems. You can read more about this in [How Works](https://docs.ousd.com/how-it-works).

## How soon will my balance increase once I have OUSD?

The amount of OUSD in your wallet will grow each time there is a positive rebase event. You can read more about this in [Elastic Supply](https://docs.ousd.com/core-concepts/elastic-supply). The supply is currently rebased several times per day and is usually correlated with how many people are minting and redeeming OUSD.

## Why does OUSD not grow when it's held in Uniswap, SushiSwap, etc?

By default, rebase events don't affect the supply of OUSD that is sitting in smart contracts. These contracts can opt in to receiving additional OUSD if they are capable of handling elastic supply tokens. You can read more about this in [Rebasing & Smart Contracts](https://docs.ousd.com/core-concepts/elastic-supply/rebasing-and-smart-contracts).

## How is it possible for the APY to be so high?

You can read about our various strategies in [Yield Generation](https://docs.ousd.com/core-concepts/yield-generation). We currently get most of the yield from harvesting rewards tokens \(namely COMP and CRV\). Additionally, the yield increases as more OUSD is held in smart contracts that do not opt into rebasing since the underlying collateral continues to earn for the average OUSD holder.

## Why is my balance increasing at a slower rate than the advertised APY?

OUSD balances increase when the supply is rebased. But the size of each rebase varies wildly depending on how much the vault has earned since the last rebase. And while most rebases collect a small amount earnings from lending strategies, other rebases involve liquidating rewards tokens or collecting fees. As a result, the yield will vary significantly during short time periods.

