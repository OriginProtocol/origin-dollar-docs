# Маркет-мейкинг

**Владейте долей на децентрализованных биржах**

Автоматизированные маркет-мейкеры \(AMM\) быстро стали предпочтительной формой децентрализованного бирж в сети Ethereum. Частично это связано со сложностью поддержки стакана заявок в DEXах на Ethereum 1.0, который может конкурировать с быстрой работой и низким проскальзыванием на централизованных биржах. Кроме того, такие AMM, как Uniswap, относительно понятны в использовании и экономят больше газа.

AMM могут открывать новые рынки только тогда, когда поставщики ликвидности предоставляют ликвидность (например, несколько токенов для данных торговых пар или пулов). В обмен на предоставление ликвидности, поставщики ликвидности вознаграждаются торговыми комиссиями, когда другие пользователи обменивают токены. Например, когда трейдеры обменивают USDT на USDC на Uniswap, в настоящее время с них взимается 0,3% сверх платы за газ. Эти комиссии распределяются пропорционально между поставщиками ликвидности по паре USDT-USDC на основе процента от общей ликвидности, которую они предоставили.

{% hint style="info" %}
[Impermanent loss](https://medium.com/@pintail/uniswap-a-good-deal-for-liquidity-providers-104c0b6816f2) is an important risk factor to understand, but this concern is largely mitigated by OUSD only providing liquidity for stablecoins of approximately equal value.
{% endhint %}

The OUSD protocol routes USDT, USDC, and DAI to highly-performing liquidity pools as determined by trading volume and rewards tokens \(e.g. Balancer rewards BAL tokens to liquidity providers\). Yields are then passed on to OUSD holders.

We intend to integrate directly with at least the following automated market makers:

{% page-ref page="../supported-strategies/uniswap.md" %}

{% page-ref page="../supported-strategies/curve.md" %}

{% page-ref page="../supported-strategies/balancer.md" %}





