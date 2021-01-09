# 风险

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

与任何计息工具一样, 持有 OUSD 也有相关的风险。 这些风险可以大致分为3类：

* 智能合约风险
* 底层平台风险
* 底层稳定币风险

**智能合约风险**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**平台风险**

因为 OUSD 是建立在其他 DeFi 平台之上，因此这些平台会增加额外的智能合约风险。 我们选择与管理着数亿美元资产并已努力确保其协议的正确性的平台合作。 但是，我们不能保证基础平台将继续按预期运行。基础策略的任何故障或问题都很可能导致 OUSD 持有者损失资金。

**稳定币风险**

必须了解的是，OUSD 仅与支持它的稳定币一样强大。 底层资产的任何损失都将造成 OUSD 相似的损失。

值得注意的是，所有这些稳定币都会带来重要的交易对手风险。 尤其是 Tether 遇到了许多银行业麻烦和监管挑战。 此外，USDT 和 USDC 都有后门，可以让发行者有权冻结持有者钱包中的资金。 尽管 DAI 没有任何直接后门程序，但由于 USDC 可以作为铸造 DAI 的抵押品，因此 DAI 的资产也可能受到负面影响。

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







