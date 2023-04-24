# Риски

{% hint style="danger" %}
Используйте на свой риск. Не вкладывайте больше капитала, чем вы готовы потерять.
{% endhint %}

Как и в случае с любым продуктом DeFi, приносящим доход, с удержанием OUSD связаны риски, которые важно понимать. Эти риски можно условно разделить на 3 категории:

* Риск смарт-контракта OUSD
* Риск базовой сторонней платформы
* Риск базового стейблкоина

**Риск смарт-контракта OUSD**

Наши смарт-контракты [прошли аудиты](audits.md) во множестве уважаемых компаний по безопасности. Однако важно отметить, что даже с учетом пройденных аудитов, все еще возможны логические ошибки, которые могут привести к потере средств держателей OUSD. Контракты используют сложную математику и логику. Несмотря на то, что мы приняли все меры предосторожности для обеспечения безопасности наших смарт-контрактов, напоминаем пользователям, что они используют их на свой страх и риск. Origin Protocol не несет ответственности за какую бы то ни было потерю средств, независимо от того, чья в этом вина.

**Риск базовой сторонней платформы**

OUSD надстроен поверх других платформ DeFi, таких как Aave, Compound и Curve, что увеличивает риски в смарт-контрактах. We are choosing to work with platforms that have literally billions of dollars of assets under management and have made a reasonable efforts to ensure the security of their protocols. Однако нет никаких гарантий, что базовые сторонние платформы будут продолжать работать по назначению, и любой сбой в базовой стратегии, скорее всего, приведет к потере средств для держателей OUSD.

**Риски стейблкоина**

Важно понимать, что OUSD настолько устойчив, насколько устойчивы стейблкоины, которые его обеспечивают. Any loss of value to an underlying stablecoin asset will cause a similar loss to the value of OUSD. While OUSD is designed to maintain a 1:1 relationship between supply and number of backing stablecoins, it does not guarantee which stablecoins will make up that backing nor the value of those coins.

Важно отметить, что каждый из поддерживаемых стейблкоинов представляет собой нетривиальный риск для контрагента. У Tether, в частности, были хорошо задокументированные проблемы с банковской системой и нормативными требованиями. Кроме того, и в USDT, и в USDC есть лазейки, которые дают их эмитентам право замораживать деньги в кошельках их владельцев. While DAI does not have any direct backdoors, its assets can also be negatively impacted since USDC and USDT are accepted as collateral for minting DAI.

**Risk mitigation**

While it's impossible to guarantee our contracts are 100% safe, we have taken every step possible to mitigate the chance of losing funds:

We regularly have our work [audited ](audits.md)by the top auditors in the industry.

[DeFi insurance](insurance.md) is availble  to offer smart contract coverage as an optional add-on service for OUSD holders.

We have retained [Certora](https://www.certora.com) to formally verify the various security properties of our contracts. They helped us establish automated verifications that will run anytime we update our contract code. We have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are incredibly rigorous. We require at least two engineers to review each change with a detailed checklist and we prioritize security reviews over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contracts' source code ourselves. We've observed that attackers often exploit the same fundamental vulnerability on multiple different projects. By reviewing other project's vulnerabilities, we force ourselves to stay up to date on the latest security threats in our industry and are constantly learning from their mistakes.

**Actions speak louder than words**

You should also know that many members of the Origin team, including both founders, are holding a significant portion of their personal wealth in OUSD. Origin Protocol's corporate treasury is also holding millions of dollars in OUSD. We have skin in the game and are willing to put our own money at risk with the code we have written.

