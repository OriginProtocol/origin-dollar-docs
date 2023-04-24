# Visión General

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD se compone de una serie de contratos inteligentes. Cada uno de estos contratos está envuelto en un contrato de poder que se puede actualizar a través de los protocolos de gobernancia.

Internamente, la propiedad en el pool se rastrea mediante un sistema de créditos que representa el porcentaje de propiedad del grupo de liquidez para cada holder. El contrato ERC-20 maneja la conversión a términos en USD cuando se ve un saldo o se inicia una transferencia entre billeteras.

La Bóveda es responsable de acuñar y quemar OUSD. También aplica el porcentaje de activos que se implementan en cada una de las [Estrategias](../core-concepts/supported-strategies/) admitidas. Para optimizar los costos de GAS, la bóveda mantiene un búfer para permitir que la mayoría de los depósitos y reembolsos ocurran sin liquidar / deshacer los activos de las estrategias.



