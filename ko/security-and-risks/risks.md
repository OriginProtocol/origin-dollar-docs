# 위험

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

As with any yield-generating DeFi product, there are associated risks with holding OUSD that are important to understand. These risks can be broadly classified into 3 categories:

* OUSD smart contract risk
* Underlying third-party platform risk
* 기초 스테이블 코인 위험

**OUSD smart contract risk**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic. While we have taken every precaution to ensure the safety and security of our smart contracts, users are reminded to use at their own risk. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Third-party platform risk**

OUSD is built on top of other DeFi platforms like Aave, Compound, and Curve that add additional smart contract risk. We are choosing to work with platforms that have hundreds of millions of dollars of assets under management and have made a reasonable efforts to ensure the security of their protocols. However, there are no guarantees that the underlying third-party platforms will continue to work as intended, and any failure in an underlying strategy would potentially lead to a loss of funds for OUSD holders.

**스테이블 코인 위험**

OUSD는 이를 뒷받침하는 스테이블 코인 만큼 강하다는 점을 이해하는 것이 중요합니다. Any loss of value in to an underlying stablecoin asset will cause a similar loss to the value of OUSD. While OUSD is designed to maintain a one to one relationship between supply and number of backing stablecoins, it does not guarantee which stablecoins will make up that backing nor the value of those coins.

지원되는 각 스테이블 코인은 서로 다른 상대방에 대한 리스크를 유발한다는 점에 유의해야 합니다. 특히 테더(Tether) 는 잘 문서화된 은행 문제 및 규제 문제를 안고 있습니다. 또한 USDT와 USDC는 발행인이 보유자의 지갑에있는 돈을 동결(freeze) 할 수 있는 권한을 부여하는 백도어(backdoors) 기능이 있습니다. While DAI does not have any direct backdoors, its assets can also be negatively impacted since USDC is accepted as collateral for minting DAI.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. In addition to our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contracts' source code ourselves.







