# Arquitectura

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD está compuesto por una serie de contratos inteligentes. Cada uno de estos contratos está envuelto en un contrato proxy que se puede actualizar a través de los protocolos de gobernanza.

Internally, ownership in the vault is tracked using a credits system that represents the percent ownership of the vault for each holder. El contrato [ERC-20](api/erc-20-1.md) maneja la conversión a términos de USD cuando se visualiza un saldo o se inicia una transferencia entre billeteras.

La [Bóveda](api/vault.md) es responsable de acuñar y quemar OUSD. También aplica el porcentaje de activos que se implementan en cada una de las [Estrategias](../core-concepts/supported-strategies/)admitidas. Para optimizar los costos de Gas, la bóveda mantiene un búfer para permitir que la mayoría de los depósitos y reembolsos ocurran sin liquidar/deshacer los activos de las estrategias.



