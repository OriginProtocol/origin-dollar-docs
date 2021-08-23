# Riesgos

{% hint style="danger" %}
Úselo bajo su propio riesgo. No gaste más capital del que está dispuesto a perder.
{% endhint %}

Al igual que con cualquier producto DeFi que genere rendimiento, existen riesgos asociados con la tenencia de OUSD que es importante comprender. Estos riesgos se pueden clasificar ampliamente en 3 categorías:

* Riesgo de contrato inteligente
* Riesgo subyacente de la plataforma de terceros
* Riesgo de moneda estable subyacente

**Riesgo de contrato inteligente**

Nuestros contratos inteligentes han sido [auditados](audits.md) por varias empresas de seguridad respetadas. Sin embargo, es importante tener en cuenta que incluso con auditorías formales, todavía es posible que haya errores lógicos que podrían conducir a la pérdida de fondos para los holders de OUSD. Los contratos involucran matemáticas y lógica complejas. Si bien hemos tomado todas las precauciones para garantizar la seguridad de nuestros contratos inteligentes, se recuerda a los usuarios que lo utilicen bajo su propio riesgo. Origin Protocol no se hace responsable de ninguna pérdida de fondos, independientemente de quién tenga la culpa.

**Riesgo de plataforma de terceros**

OUSD se basa en otras plataformas DeFi que agregan un riesgo adicional de contrato inteligente. We are choosing to work with platforms that have literally billions of dollars of assets under management and have made a reasonable efforts to ensure the security of their protocols. Sin embargo, no hay garantías de que las plataformas subyacentes continuarán funcionando según lo previsto, y cualquier falla en una estrategia subyacente probablemente conduciría a una pérdida de fondos para los holders de OUSD.

**Riesgos de la moneda estable**

Es importante comprender que OUSD es tan fuerte como las monedas estables que lo respaldan. Any loss of value to an underlying stablecoin asset will cause a similar loss to the value of OUSD. While OUSD is designed to maintain a 1:1 relationship between supply and number of backing stablecoins, it does not guarantee which stablecoins will make up that backing nor the value of those coins.

Es importante tener en cuenta que cada una de las monedas estables admitidas presenta un riesgo de contraparte no trivial. Tether, en particular, ha tenido problemas bancarios y problemas regulatorios bien documentados. Además, tanto USDT como USDC tienen puertas traseras que otorgan a sus emisores el poder de congelar dinero en las billeteras de sus titulares. While DAI does not have any direct backdoors, its assets can also be negatively impacted since USDC and USDT are accepted as collateral for minting DAI.

**Risk mitigation**

While it's impossible to guarantee our contracts are 100% safe, we have taken every step possible to mitigate the chance of losing funds:

We regularly have our work [audited ](audits.md)by the top auditors in the industry.

We've worked with the top two [DeFi insurance](insurance.md) providers to offer smart contract coverage as an optional add-on service for OUSD holders.

We have retained [Certora](https://www.certora.com/) to formally verify the various security properties of our contracts. They helped us establish automated verifications that will run anytime we update our contract code. We have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are incredibly rigorous. We require at least two engineers to review each change with a detailed checklist and we prioritize security reviews over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contracts' source code ourselves. We've observed that attackers often exploit the same fundamental vulnerability on multiple different projects. By reviewing other project's vulnerabilities, we force ourselves to stay up to date on the latest security threats in our industry and are constantly learning from their mistakes.

**Actions speak louder than words**

You should also know that many members of the Origin team, including both founders, are holding a significant portion of their personal wealth in OUSD. Origin Protocol's corporate treasury is also holding millions of dollars in OUSD. We have skin in the game and are willing to put our own money at risk with the code we have written.



