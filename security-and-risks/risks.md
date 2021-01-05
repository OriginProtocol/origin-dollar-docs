# Risks

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

As with any interest-bearing instrument. there are associated risks with holding OUSD that are important to understand. These risks can be broadly classified into 3 categories:

* Smart contract risk
* Underlying platform risk
* Underlying stablecoin risk

**Smart contract risk**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Platform risk**

OUSD is built on top of other DeFi platforms that add additional smart contract risk. We are choosing to work with platforms that have hundreds of millions of dollars of assets under management and have made a reasonable effort to ensure the correctness of their protocols. However, there are no guarantees that the underlying platforms will continue to work as intended, and any failure in an underlying strategy would likely lead to a loss of funds for OUSD holders.

**Stablecoin risks**

It is important to understand that OUSD is only as strong as the stablecoins that are backing it. Any loss to the underlying assets will cause a similar loss to the value of OUSD. 

It is important to note that each of the supported stablecoins introduces non-trivial counter-party risk. Tether, in particular, has had well-documented banking troubles and regulatory challenges. In addition, both USDT and USDC have backdoors that grant their issuers the power to freeze money in their holder's wallets. While DAI does not have any direct backdoors, it's assets can also be negatively impacted since USDC is accepted as collateral for minting DAI. 

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







