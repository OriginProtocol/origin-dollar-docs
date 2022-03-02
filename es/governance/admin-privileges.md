# Privilegios de Administrador

Los contratos inteligentes de OUSD están diseñados para que el propietario pueda actualizarlos. El equipo de Origin utiliza dos contratos de billetera multifirma Gnosis diferentes para realizar cambios en el protocolo. Estas carteras multifirma han sido [auditadas por OpenZeppelin](https://blog.openzeppelin.com/gnosis-multisig-wallet-audit-d702ff0e2b1e/), [ConsenSys Dilligence](https://blog.gnosis.pm/the-gnosis-multisig-wallet-and-our-commitment-to-security-ce9aca0d17f6), el equipo de Origin y otros. &#x20;

{% hint style="info" %}
Las acciones administrativas que retrasan el tiempo les dan a los usuarios la oportunidad de salir de OUSD si sus administradores se vuelven maliciosos, se ven comprometidos o hacen un cambio que a los usuarios no les gusta.
{% endhint %}

El administrador principal es un contrato multifirma 5 de 8 que se requiere para realizar cualquier cambio de código en el protocolo. OUSD solo se puede actualizar desde esta billetera multi-sig de 5 de 8. Las claves de este multi-sig están en manos de personas con vínculos estrechos con la empresa, y ni siquiera los fundadores de Origin que actúan juntos tienen suficiente control para ejecutar las funciones de propietario por su cuenta. In addition, the OUSD contracts are owned by the [timelock](../smart-contracts/api/timelock.md) which allows the Origin team to continue making changes to the protocol, but only after a time delay.&#x20;

Algunas funciones, como reequilibrar fondos entre estrategias o pausar depósitos, se pueden activar sin el bloqueo de tiempo y con muchos menos firmantes. Esto permite que el equipo de Origin reaccione más rápidamente ante las condiciones del mercado o las amenazas a la seguridad. These signers, known as Strategists,  have the ability to execute a limited number of functions __ with only 2 of 9 signers.

Tener privilegios de administrador es necesario en los primeros días para garantizar que el protocolo sea seguro y esté optimizado para obtener rendimientos y minimizar los riesgos. Esperamos lanzar múltiples iteraciones de nuestros contratos inteligentes en los primeros meses de existencia del protocolo.

Una vez que se hayan completado varios ciclos de actualización, tenemos la intención de transferir la propiedad del control de nuestra empresa a un contrato de gobernanza descentralizado, permitiendo así que la comunidad vote y participe en futuras actualizaciones de protocolo.
