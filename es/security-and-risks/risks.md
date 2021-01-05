# Riesgos

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

Como con cualquier instrumento que devenga intereses. existen riesgos asociados con al hacer hold de OUSD que son importante comprender. Estos riesgos se pueden clasificar ampliamente en 3 categorías:

* Riesgo de contrato inteligente
* Riesgo de plataforma subyacente
* Riesgo de moneda estable subyacente

**Riesgo de contrato inteligente**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Riesgo de plataforma**

OUSD se basa en otras plataformas DeFi que agregan un riesgo adicional de contrato inteligente. Estamos eligiendo trabajar con plataformas que tienen cientos de millones de dólares en activos bajo su administración y han hecho un esfuerzo razonable para garantizar la exactitud de sus protocolos. Sin embargo, no hay garantías de que las plataformas subyacentes continuarán funcionando según lo previsto, y cualquier falla en una estrategia subyacente probablemente conduciría a una pérdida de fondos para los holders de OUSD.

**Riesgos de la moneda estable**

Es importante comprender que OUSD es tan fuerte como las monedas estables que lo respaldan. Cualquier pérdida de los activos subyacentes provocará una pérdida similar al valor de OUSD.

Es importante tener en cuenta que cada una de las monedas estables admitidas presenta un riesgo de contraparte no trivial. Tether, en particular, ha tenido problemas bancarios y problemas regulatorios bien documentados. Además, tanto USDT como USDC tienen puertas traseras que otorgan a sus emisores el poder de congelar dinero en las billeteras de sus titulares. Si bien DAI no tiene puertas traseras directas, sus activos también pueden verse afectados negativamente ya que el USDC se acepta como garantía para acuñar DAI.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







