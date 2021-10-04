# Arquitectura

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD está compuesto por una serie de contratos inteligentes. Cada uno de estos contratos está envuelto en un contrato proxy que se puede actualizar a través de los protocolos de gobernanza.

Internamente, la propiedad en el pool se rastrea mediante un sistema de créditos que representa el porcentaje de propiedad del pool para cada holder. El contrato [ERC-20](api/erc-20-1.md) maneja la conversión a términos de USD cuando se visualiza un saldo o se inicia una transferencia entre billeteras.

La [Bóveda](api/vault.md) es responsable de acuñar y quemar OUSD. También aplica el porcentaje de activos que se implementan en cada una de las [Estrategias](../core-concepts/supported-strategies/)admitidas. Para optimizar los costos de Gas, la bóveda mantiene un búfer para permitir que la mayoría de los depósitos y reembolsos ocurran sin liquidar/deshacer los activos de las estrategias.

OUSD Swap, también conocido como "Flipper" es un contrato inteligente proporcionado por Origin para que los usuarios intercambien OUSD de forma económica por DAI, USDC o USDT a una tasa fija de 1: 1. Este contrato se utiliza como una forma alternativa de enrutar las transacciones de los usuarios que se originan en la aplicación web. Es importante tener en cuenta que este contrato puede quedarse sin fondos en un lado \(por ejemplo, tener 0 OUSD\) y, por lo tanto, a veces proporciona rutas de intercambio limitadas. Aunque tiene una funcionalidad limitada, Origin Swap usa alrededor de un 45% menos de gas que Uniswap v3 debido a su simplicidad.



