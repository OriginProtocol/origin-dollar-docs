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

OUSD se basa en otras plataformas DeFi que agregan un riesgo adicional de contrato inteligente. Estamos eligiendo trabajar con plataformas que tienen cientos de millones de dólares en activos bajo su administración y han hecho un esfuerzo razonable para garantizar la exactitud de sus protocolos. Sin embargo, no hay garantías de que las plataformas subyacentes continuarán funcionando según lo previsto, y cualquier falla en una estrategia subyacente probablemente conduciría a una pérdida de fondos para los holders de OUSD.

**Riesgos de la moneda estable**

Es importante comprender que OUSD es tan fuerte como las monedas estables que lo respaldan. Cualquier pérdida de valor en un activo de moneda estable subyacente causará una pérdida similar al valor de OUSD. Si bien OUSD está diseñado para mantener una relación uno a uno entre el suministro y la cantidad de monedas estables de respaldo, no garantiza qué monedas estables conformarán ese respaldo ni el valor de esas monedas.

Es importante tener en cuenta que cada una de las monedas estables admitidas presenta un riesgo de contraparte no trivial. Tether, en particular, ha tenido problemas bancarios y problemas regulatorios bien documentados. Además, tanto USDT como USDC tienen puertas traseras que otorgan a sus emisores el poder de congelar dinero en las billeteras de sus titulares. Si bien DAI no tiene puertas traseras directas, sus activos también pueden verse afectados negativamente ya que el USDC se acepta como garantía para acuñar DAI.

_**En resumen, OUSD es un software beta. Úselo bajo su propio riesgo. No gaste más capital del que está dispuesto a perder.**_

**Mitigación de riesgos**

Estamos trabajando activamente con múltiples proveedores de seguros DeFi y pronto anunciaremos nuestros planes de cobertura iniciales para asegurar aún más el protocolo. Además de nuestro plan para ofrecer cobertura de seguros y nuestras recientes [auditorías](audits.md), hemos tomado amplias medidas para mejorar nuestros procesos internos para que hagamos todo lo posible para evitar un exploit.

Hemos contratado [Certora](https://www.certora.com/) para comenzar a verificar formalmente las diversas propiedades de seguridad de nuestros contratos. Nos ayudarán a establecer verificaciones automatizadas que se ejecutarán cada vez que actualicemos nuestro código de contrato. Ahora también tenemos la verificación automática de errores comunes con las pruebas [Slither](https://github.com/crytic/slither) y [Echidna](https://github.com/crytic/echidna) Juntos, alertan a nuestro equipo sobre problemas de seguridad comunes, además de nuestro propio conjunto de pruebas.

Las revisiones de código que involucran nuestros contratos inteligentes ahora son más rigurosas que antes. Requerimos que dos ingenieros revisen cada cambio con una lista de verificación detallada y le damos prioridad al desarrollo de nuevas funciones.

Finalmente, hemos formalizado una </a>rotación para revisar [ataques a otros proyectos](https://github.com/OriginProtocol/security/tree/master/incidents), así como para asegurarnos de que profundicemos en cada una de estas revisiones, incluida la revisión del código fuente de los contratos afectados nosotros mismos.</p>







