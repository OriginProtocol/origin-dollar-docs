# Creación de Mercado

**Sea dueño de su participación en exchanges descentralizados**

Los Creadores de Mercado Automatizados \(AMMs\) se han convertido rápidamente en la forma preferida de plataforma de intercambio descentralizado en la red de Ethereum. Esto se debe en parte a la dificultad de admitir libros de pedidos en los DEX en la red de Ethereum 1.0 que pueden rivalizar con las experiencias instantáneas y de bajo deslizamiento de los exchanges centralizados. Además, los AMM como Uniswap son relativamente fáciles de usar y de uso eficiente del gas.

Los AMM solo pueden habilitar nuevos mercados cuando los proveedores de liquidez brindan liquidez \ (por ejemplo, múltiples tokens para pares o grupos de liquidez de trading determinados\). A cambio de proporcionar liquidez, los proveedores de liquidez son recompensados con comisiones de trading cuando otros usuarios intercambian tokens. Por ejemplo, cuando los comerciantes intercambian dos tokens en Uniswap v3, actualmente se les cobra entre el 0,05% y el 1% además de las tarifas del gas. Estas tarifas se distribuyen proporcionalmente a los proveedores de liquidez del par en función del porcentaje de liquidez total que hayan proporcionado.

{% hint style="info" %}
[Pérdida impermanente](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) es un factor de riesgo importante de comprender, pero esta preocupación se mitiga en gran medida porque OUSD solo proporciona liquidez para monedas estables de aproximadamente el mismo valor.
{% endhint %}

El protocolo de OUSD enruta USDT, USDC y DAI a grupos de liquidez de alto rendimiento según lo determinado por el volumen de negociación y recompensa tokens \(por ejemplo, Curve recompensa tokens CRV a proveedores de liquidez\). Luego, los rendimientos se transfieren a los holders de OUSD.

Actualmente estamos integrados con el siguiente creador de mercado automatizado:

{% page-ref page="../supported-Strategies/curve.md"%}





