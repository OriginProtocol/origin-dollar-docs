# Bloqueo de Tiempo

{% hint style="danger" %}
El bloqueo de tiempo se agregará poco después de que se verifique que todo funciona. Hasta entonces, los contratos se regirán por el 5 de 8 multi-sig de Origin. Esto permite una respuesta más rápida si se descubre algún problema crítico.
{% endhint %}

El contrato de bloqueo de tiempo impone un período de espera de 48 horas antes de que se pueda ejecutar cualquier cambio en los contratos de OUSD. El bloqueo de tiempo puede ser llamado por nuestro multi-sig y es el propietario de nuestros contratos [ERC-20](erc-20.md), [Bóveda](vault.md) y [Estrategias](strategies.md). Las acciones administrativas que retrasan el tiempo les dan a los usuarios la oportunidad de salir de OUSD si sus administradores se vuelven maliciosos, se ven comprometidos o hacen un cambio que a los usuarios no les gusta.

{% hint style="info" %}
El bloqueo de tiempo es una medida de seguridad que les da a los holders de OUSD 48 horas para retirar sus fondos si tienen objeciones a las actualizaciones propuestas al protocolo.
{% endhint %}

OUSD is using a slightly modified version of the [Compound Timelock](https://compound.finance/docs/governance) which has been [audited by OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The 3 notable differences are:

1. OUSD will initially use a shorter wait period \(48 hours\) than Compound \(72 hours\) to allow for a faster response if any issues are discovered.
2. Once the 48 hours have passed, anyone is free to execute the call, not just the owner of the contract.
3. Deposits \(but not withdrawals or transfers\) can be immediately frozen without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





