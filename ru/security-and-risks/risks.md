# Риски

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

Как и любой процентный инструмент, существуют риски, связанные с хранением OUSD, которые важно понимать. Эти риски можно условно разделить на 3 категории:

* Риск смарт-контракта
* Риск базовой платформы
* Риск базового стейблкоина

**Риск смарт-контракта**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Риск платформы**

OUSD надстроен поверх других платформ DeFi, что увеличивает риск смарт-контрактов. Мы выбираем для работы платформы, у которых под управлением находятся активы на сотни миллионов долларов, и которые приложили разумные усилия для обеспечения правильности их протоколов. Однако нет никаких гарантий, что лежащие в основе платформы будут продолжать работать по назначению, и любой сбой в базовой стратегии, скорее всего, приведет к потере средств для держателей OUSD.

**Риски стейблкоина**

Важно понимать, что OUSD настолько устойчив, насколько устойчивы стейблкоины, которые его обеспечивают. Любая потеря базовых активов приведет к аналогичным убыткам в OUSD.

Важно отметить, что каждый из поддерживаемых стейблкоинов представляет собой нетривиальный риск для контрагента. У Tether, в частности, были хорошо задокументированные проблемы с банковской системой и нормативными требованиями. Кроме того, и в USDT, и в USDC есть лазейки, которые дают их эмитентам право замораживать деньги в кошельках их владельцев. Не смотря на то, что в DAI нет таких лазеек, на его активы также может возникнуть негативное влияние, поскольку USDC принимается в качестве обеспечения для добычи DAI.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







