# Arquitectura

![](../.gitbook/assets/ousd\_docs\_graphics\_3.png)

OUSD está compuesto por una serie de contratos inteligentes. Cada uno de estos contratos está envuelto en un contrato proxy que se puede actualizar a través de los protocolos de gobernanza.

Internamente, la propiedad en el pool se rastrea mediante un sistema de créditos que representa el porcentaje de propiedad del pool para cada holder. El contrato [ERC-20](api/erc-20-1.md) maneja la conversión a términos de USD cuando se visualiza un saldo o se inicia una transferencia entre billeteras.

La [Bóveda](api/vault.md) es responsable de acuñar y quemar OUSD. También aplica el porcentaje de activos que se implementan en cada una de las [Estrategias](../core-concepts/supported-strategies/)admitidas. To optimize gas costs, the vault may maintain a buffer to allow most deposits and redemptions to occur without winding/unwinding assets from strategies.

The Flipper is a smart contract for users to swap in and out of OUSD cheaply for any of DAI, USDC, or USDT at a fixed 1:1 rate. Este contrato se utiliza como una forma alternativa de enrutar las transacciones de los usuarios que se originan en la aplicación web. It's important to note that this contract may be empty on one side (e.g., contain 0 OUSD balance), and thus sometimes provides limited swap routes. While limited in functionality, Flipper uses around 45% less gas than Uniswap v3 due to its simplicity.

The Harvester contract collects reward tokens earned by the strategies, sells them, and sends the resulting stablecoins to the Dripper to be released to the vault. Anyone can call the harvest and earn 1% of the resulting USDT for doing so. This creates a self-incentivizing system that operates at a known fixed cost.

The Dripper contract buffers aproximately one week of reward token sales proceeds and makes it avaiable at a smooth rate to the vault. This keeps OUSD yield from being extremely spiky when harvests come in. The rate is recalculated at least once per day and is the rate that it would take to distribute the current dripper holdings out over a one week period.



