# Risks

{% hint style="danger" %}
The OUSD smart contracts have not yet been audited. We strongly recommend reviewing our smart contracts before depositing significant amounts of capital.
{% endhint %}

As with any interest-bearing instrument. there are associated risks with holding OUSD that are important to understand. These risks can be broadly classified into 3 categories:

* Smart contract risk
* Underlying platform risk
* Underlying stablecoin risk

**Smart contract risk**

Our smart contracts have not yet been audited, and even with a formal audit, it is still possible for there to be logic errors that would lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Platform risk**

OUSD is built on top of other DeFi platforms that add additional smart contract risk. We are choosing to work with platforms that have hundreds of millions of dollars of assets under management and have made a reasonable effort to ensure the correctness of their protocols. However, there are no guarantees that the underlying platforms will continue to work as intended, and any failure in an underlying strategy would likely lead to a loss of funds for OUSD holders.

**Stablecoin risks**

It is important to understand that OUSD is only as strong as the stablecoins that are backing it. Any loss to the underlying assets will cause a similar loss to the value of OUSD.

It is important to note that each of the supported stablecoins introduces non-trivial counter-party risk. Tether, in particular, has had well-documented banking troubles and regulatory challenges. In addition, both USDT and USDC have backdoors that grant their issuers the power to freeze money in their holder's wallets. While DAI does not have any direct backdoors, it's assets can also be negatively impacted since USDC is accepted as collateral for minting DAI.

**In summary, OUSD is beta software. Use at your own risk. Don't deploy more capital than you are willing to lose.**







