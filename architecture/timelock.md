# Bloqueo de Tiempo

{% hint style="danger" %}
El bloqueo de tiempo se agregará poco después de que se verifique que todo funciona. Hasta entonces, los contratos se regirán por el 5 de 8 multi-sig de Origin. Esto permite una respuesta más rápida si se descubre algún problema crítico.
{% endhint %}

El contrato de bloqueo de tiempo impone un período de espera de 48 horas antes de que se pueda ejecutar cualquier cambio en los contratos de OUSD. El bloqueo de tiempo puede ser llamado por nuestro multi-sig y es el propietario de nuestros contratos [ERC-20](erc-20.md), [Bóveda](vault.md) y [Estrategias](strategies.md). Las acciones administrativas que retrasan el tiempo les dan a los usuarios la oportunidad de salir de OUSD si sus administradores se vuelven maliciosos, se ven comprometidos o hacen un cambio que a los usuarios no les gusta.

{% hint style="info" %}
El bloqueo de tiempo es una medida de seguridad que les da a los holders de OUSD 48 horas para retirar sus fondos si tienen objeciones a las actualizaciones propuestas al protocolo.
{% endhint %}

OUSD está utilizando una versión ligeramente modificada del [Tiempo de Bloqueo de Compound](https://compound.finance/docs/governance) que ha sido [auditado por OpenZeppelin](https://blog.openzeppelin.com/compound-finance-patch-audit/). Las 3 diferencias notables son:

1. OUSD inicialmente utilizará un período de espera más corto \(48 horas\) que Compound \(72 horas\) para permitir una respuesta más rápida si se descubre algún problema.
2. Una vez transcurridas las 48 horas, cualquiera es libre de ejecutar la llamada, no sólo el dueño del contrato.
3. Los depósitos \(pero no los retiros\) se pueden congelar inmediatamente sin requerir el período de espera de 48. Esto es en caso de que se descubra una vulnerabilidad importante.





