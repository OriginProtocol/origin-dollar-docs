# Market Making

**Custodisci il tuo stake negli Exchanges Decentralizzati**

I market maker automatizzati \(AMMs\) sono cresciuti rapidamente come forma preferita di scambio decentralizzato sul network di Ethereum. Ciò in parte è dovuto alla difficoltà di supportare gli order book DEX su Ethereum 1.0 che possano competere con gli attuali exchange centralizzati, istantanei e a basso slippage. Inoltre, gli AMM come Uniswap sono relativamente user-friendly ed efficienti dal punto di vista del gas.

Gli AMM possono abilitare nuovi mercati solo quando i liquidity providers forniscono liquidità \(ad esempio più token per determinati pair o pool \). In cambio per fornire liquidità, i liquidity providers sono ricompensati con le commissioni di trading quando altri utenti swappano i token. Per esempio, quando i trader swappano USDT per USDC su Uniswap, vengono attualmente addebitati di un 0.3% al netto delle commissioni del gas. Queste commissioni vengono distribuite proporzionalmente ai liquidity providers del pair USDT-USDC, in base alla percentuale della liquidità totale che è stata fornita.

{% hint style="info" %}
[Impermanent loss](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) è un fattore di rischio importante da capire, ma questa preoccupazione è altamente mitigata dal fatto che OUSD fornisce liquidità solo per stablecoin che hanno approssimatamente egual valore.
{% endhint %}

Il protocollo OUSD indirizza USDT, USDC e DAI in pool altamente performanti determinati dal volume degli scambi e dai token di ricompensa \(ad esempio Balancer ricompensa con token DAI i suoi liquidity provider\). Gli Yields vengono quindi trasferiti ai detentori di OUSD.

We are currently integrated with the following automated market maker:

{% page-ref page="../supported-strategies/curve.md" %}

We are intending to integrate with the following automated market makers:





