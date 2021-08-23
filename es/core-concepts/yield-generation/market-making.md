# Creación de Mercado

**Sea dueño de su participación en exchanges descentralizados**

Los Creadores de Mercado Automatizados \(AMMs\) se han convertido rápidamente en la forma preferida de plataforma de intercambio descentralizado en la red de Ethereum. Esto se debe en parte a la dificultad de admitir libros de pedidos en los DEX en la red de Ethereum 1.0 que pueden rivalizar con las experiencias instantáneas y de bajo deslizamiento de los exchanges centralizados. Además, los AMM como Uniswap son relativamente fáciles de usar y de uso eficiente del gas.

Los AMM solo pueden habilitar nuevos mercados cuando los proveedores de liquidez brindan liquidez \ (por ejemplo, múltiples tokens para pares o grupos de liquidez de trading determinados\). A cambio de proporcionar liquidez, los proveedores de liquidez son recompensados con comisiones de trading cuando otros usuarios intercambian tokens. For example, when traders swap two tokens on Uniswap v3, they are currently charged anywhere between 0.05% and 1% on top of the gas fees. These fees are distributed pro-rata to liquidity providers of the pair based on the percentage of total liquidity that they have provided.

{% hint style="info" %}
[Pérdida impermanente](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) es un factor de riesgo importante de comprender, pero esta preocupación se mitiga en gran medida porque OUSD solo proporciona liquidez para monedas estables de aproximadamente el mismo valor.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens \(e.g. Curve rewards CRV tokens to liquidity providers\). Luego, los rendimientos se transfieren a los holders de OUSD.

Actualmente estamos integrados con el siguiente creador de mercado automatizado:

{% page-ref page="../supported-Strategies/curve.md"%}





