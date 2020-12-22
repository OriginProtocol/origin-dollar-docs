# Bloqueo de Tiempo

{% hint style="danger" %}
The timelock has been added but is currently set to 1 minute. This allows for a faster response if any critical issues are discovered. The timelock is governed by Origin's 5 of 8 multi-sig.
{% endhint %}

El contrato de bloqueo de tiempo impone un período de espera de 48 horas antes de que se pueda ejecutar cualquier cambio en los contratos de OUSD. El bloqueo de tiempo puede ser llamado por nuestro multi-sig y es el propietario de nuestros contratos [ERC-20](../architecture.md), [Bóveda](vault.md) y [Estrategias](strategies.md). Las acciones administrativas que retrasan el tiempo les dan a los usuarios la oportunidad de salir de OUSD si sus administradores se vuelven maliciosos, se ven comprometidos o hacen un cambio que a los usuarios no les gusta.

{% hint style="info" %}
El bloqueo de tiempo es una medida de seguridad que les da a los holders de OUSD 48 horas para retirar sus fondos si tienen objeciones a las actualizaciones propuestas al protocolo.
{% endhint %}

OUSD está utilizando una versión ligeramente modificada del [Tiempo de Bloqueo de Compound](https://compound.finance/docs/governance) que ha sido [auditado por OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). The two notable differences are:

1. OUSD inicialmente utilizará un período de espera más corto \(48 horas\) que Compound \(72 horas\) para permitir una respuesta más rápida si se descubre algún problema.
2. Some actions, such a reallocating funds between existing strategies and freezing deposits can be called immediately without requiring the 48 waiting period. This is in case a major vulnerability is discovered.





