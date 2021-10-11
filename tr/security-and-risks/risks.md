# Riskler

{% hint style="tehlike" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

As with any yield-generating DeFi product, there are associated risks with holding OUSD that are important to understand. These risks can be broadly classified into 3 categories:

* OUSD smart contract risk
* Underlying third-party platform risk
* Stabilcoin riskinin altında yatan

**OUSD smart contract risk**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic. While we have taken every precaution to ensure the safety and security of our smart contracts, users are reminded to use at their own risk. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Third-party platform risk**

OUSD is built on top of other DeFi platforms like Aave, Compound, and Curve that add additional smart contract risk. We are choosing to work with platforms that have literally billions of dollars of assets under management and have made a reasonable efforts to ensure the security of their protocols. However, there are no guarantees that the underlying third-party platforms will continue to work as intended, and any failure in an underlying strategy would potentially lead to a loss of funds for OUSD holders.

**Stablecoin riskleri**

OUSD'nin yalnızca onu destekleyen stabilcoinler kadar güçlü olduğunu anlamak önemlidir. Any loss of value to an underlying stablecoin asset will cause a similar loss to the value of OUSD. While OUSD is designed to maintain a 1:1 relationship between supply and number of backing stablecoins, it does not guarantee which stablecoins will make up that backing nor the value of those coins.

Tüm bu stablecoin'lerin önemsiz olmayan karşı taraf riski oluşturduğuna dikkat etmek önemlidir. Özellikle Tether, iyi belgelenmiş bankacılık sorunları ve yasal zorluklar yaşadı. Ek olarak, hem USDT hem de USDC, ihraççılarına sahiplerinin cüzdanlarında para dondurma yetkisi veren arka kapılara sahiptir. While DAI does not have any direct backdoors, its assets can also be negatively impacted since USDC and USDT are accepted as collateral for minting DAI.

**Risk mitigation**

While it's impossible to guarantee our contracts are 100% safe, we have taken every step possible to mitigate the chance of losing funds:

We regularly have our work [audited ](audits.md)by the top auditors in the industry.

We've worked with the top two [DeFi insurance](insurance.md) providers to offer smart contract coverage as an optional add-on service for OUSD holders.

We have retained [Certora](https://www.certora.com) to formally verify the various security properties of our contracts. They helped us establish automated verifications that will run anytime we update our contract code. We have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are incredibly rigorous. We require at least two engineers to review each change with a detailed checklist and we prioritize security reviews over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contracts' source code ourselves. We've observed that attackers often exploit the same fundamental vulnerability on multiple different projects. By reviewing other project's vulnerabilities, we force ourselves to stay up to date on the latest security threats in our industry and are constantly learning from their mistakes.

**Actions speak louder than words**

You should also know that many members of the Origin team, including both founders, are holding a significant portion of their personal wealth in OUSD. Origin Protocol's corporate treasury is also holding millions of dollars in OUSD. We have skin in the game and are willing to put our own money at risk with the code we have written.

