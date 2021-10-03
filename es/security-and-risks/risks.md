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

OUSD se basa en otras plataformas DeFi que agregan un riesgo adicional de contrato inteligente. Estamos eligiendo trabajar con plataformas que tienen literalmente miles de millones de dólares en activos bajo administración y han realizado esfuerzos razonables para garantizar la seguridad de sus protocolos. Sin embargo, no hay garantías de que las plataformas subyacentes continuarán funcionando según lo previsto, y cualquier falla en una estrategia subyacente probablemente conduciría a una pérdida de fondos para los holders de OUSD.

**Riesgos de la moneda estable**

Es importante comprender que OUSD es tan fuerte como las monedas estables que lo respaldan. Cualquier pérdida de valor de un activo de moneda estable subyacente provocará una pérdida similar al valor de OUSD. Si bien OUSD está diseñado para mantener una relación 1:1 entre el suministro y la cantidad de monedas estables de respaldo, no garantiza qué monedas estables conformarán ese respaldo ni el valor de esas monedas.

Es importante tener en cuenta que cada una de las monedas estables admitidas presenta un riesgo de contraparte no trivial. Tether, en particular, ha tenido problemas bancarios y problemas regulatorios bien documentados. Además, tanto USDT como USDC tienen puertas traseras que otorgan a sus emisores el poder de congelar dinero en las billeteras de sus titulares. Si bien DAI no tiene puertas traseras directas, sus activos también pueden verse afectados negativamente, ya que el USDC y el USDT se aceptan como garantía para la acuñación de DAI.

**Mitigación de riesgos**

Si bien es imposible garantizar que nuestros contratos sean 100% seguros, hemos tomado todas las medidas posibles para mitigar la posibilidad de perder fondos:

Regularmente tenemos nuestro trabajo [auditado](audits.md) por los mejores auditores de la industria.

Hemos trabajado con los dos principales [proveedores de seguros](insurance.md) para ofrecer cobertura de contrato inteligente como un servicio adicional opcional para los holders de OUSD.

Hemos contratado [Certora](https://www.certora.com/) para comenzar a verificar formalmente las diversas propiedades de seguridad de nuestros contratos. Nos ayudaron a establecer verificaciones automatizadas que se ejecutarán cada vez que actualicemos nuestro código de contrato. Hemos automatizado la comprobación de errores comunes con las pruebas [Slither](https://github.com/crytic/slither) y [Echidna](https://github.com/crytic/echidna) Juntos, alertan a nuestro equipo sobre problemas de seguridad comunes, además de nuestro propio conjunto de pruebas.

Las revisiones de código que involucran nuestros contratos inteligentes son increíblemente rigurosas. Requerimos que al menos dos ingenieros revisen cada cambio con una lista de verificación detallada y damos prioridad a las revisiones de seguridad sobre el desarrollo de nuevas funciones.

Finalmente, hemos formalizado una rotación</a>

para revisar [ataques en otros proyectos](https://github.com/OriginProtocol/security/tree/master/incidents) , así como para asegurarnos de profundizar en cada una de estas revisiones, incluida la revisión del código fuente de los contratos afectados nosotros mismos. Hemos observado que los atacantes a menudo aprovechan la misma vulnerabilidad fundamental en varios proyectos diferentes. Al revisar las vulnerabilidades de otros proyectos, nos obligamos a estar al día sobre las últimas amenazas de seguridad en nuestra industria y aprendemos constantemente de sus errores.</p> 

**Las acciones hablan más que las palabras**

También debe saber que muchos miembros del equipo de Origin, incluidos ambos fundadores, poseen una parte significativa de su patrimonio personal en OUSD. La tesorería corporativa de Origin Protocol también tiene millones de dólares en OUSD. Tenemos cuero en juego y estamos dispuestos a arriesgar nuestro propio dinero con el código que hemos escrito.



