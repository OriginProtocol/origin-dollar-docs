# Guía de Integración para Exchanges

Los exchanges centralizados jugarán un papel importante para ayudarnos a alcanzar nuestra meta de hacer que OUSD sea omnipresente. Nos complace ayudar a cualquier exchange que desee que OUSD esté disponible para sus usuarios. Creemos que OUSD será una gran adición a cualquier exchange que quiera ofrecer una moneda estable superior y una nueva oportunidad de alto rendimiento para sus usuarios.

Estos documentos son un excelente punto de partida para comprender cómo funciona OUSD. Aquí hay algunas preguntas importantes para los exchanges que deseen integrar OUSD para considerar:

**¿Quieres participar en el rendimiento que se genera?**&#x20;

¡Asumimos que la respuesta será sí y también lo alentamos a seguir! Sin embargo, puede haber algunos casos en los que prefiera moverse rápido y listar OUSD sin participar en el [rebase de OUSD](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md) ya que es la integración más rápida y simple. Para los exchanges que desean incluir OUSD, pero tienen pocos recursos de ingeniería, es posible que desee iniciar la versión sin reajuste primero mientras sus ingenieros realizan los cambios necesarios. Para que OUSD no rebase, puede llamar a `rebaseOptOut()` desde cada billetera EOA que contiene OUSD, o no hacer nada si está almacenando OUSD en contratos inteligentes. El OUSD sin rebase se comporta como cualquier otro token ERC-20.&#x20;

**¿Está almacenando saldos de clientes en contratos inteligentes (es decir, multi-firmas) o carteras EOA?**

Cualquier contrato inteligente que tenga OUSD debe optar manualmente para recibir el rendimiento llamando a `rebaseOptIn()`. Esto se debe a la [oferta elástica](../core-concepts/elastic-supply/) y la [naturaleza de rebase](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md). Muchos exchanges barren los fondos de los clientes en una billetera multi-sig para almacenamiento en frío. Si hace esto, querrá asegurarse de optar por el cambio de base para que siempre esté ganando.

**¿Está almacenando en caché los saldos de los usuarios?**

OUSD actualiza dinámicamente el valor devuelto por la función `balanceOf()` en nuestro contrato ERC20. Los saldos de los usuarios se actualizarán en momentos impredecibles a medida que el protocolo genere un nuevo rendimiento. Mientras no esté almacenando en caché este valor, los usuarios siempre verán la cantidad correcta de OUSD que tienen.

Es importante tener en cuenta que, si bien OUSD es un token de rebase, los saldos de los usuarios solo se reajustarán en una dirección positiva (su saldo nunca bajará). Esto hace que las cosas sean mucho más simples que la integración de otras monedas de rebase como AMPL u otros algo-estables.

**¿Está mezclando fondos de usuarios?**

Si está mezclando fondos, querrá asegurarse de que cada usuario obtenga su cantidad prorrateada del rendimiento que genera el protocolo. Probablemente la forma más fácil de hacer esto es rastrear el saldo de cada usuario como un porcentaje de un pool en lugar de como una cantidad fija.

**¿Está pensando en aportar liquidez?**

El equipo de Origin a menudo está dispuesto a proporcionar un creador de mercado y liquidez inicial para los intercambios que desean integrar OUSD. También hay 9 cifras de liquidez disponibles en intercambios descentralizados como [Curve](https://curve.fi/factory/9).&#x20;

Si está interesado en utilizar OUSD para impulsar su propio programa de staking o ganancias, probablemente querrá poder acceder a OUSD a pedido. OUSD siempre se puede acuñar o canjear utilizando la [DApp Origin Dollar](https://www.ousd.com), o directamente desde los [contratos inteligentes de OUSD ](../smart-contracts/registry.md). If you are planning on providing liquidity yourself, you should be aware that the exact amount of OUSD you will receive in exchange for your USDT, USDC, or DAI depends on the current exchange rates as determined by the [oracles.](../core-concepts/price-oracles.md) If you are planning on redeeming OUSD for the underlying stablecoins, you should know there is a 0.25% exit fee and OUSD will return a basket of stable coins in proportion to the backing stablecoins in the pool. We encourage exchanges to leverage existing pools of liquidity to avoid those fees. If possible, mints or redeems should be done in large batches for maximum efficiency.&#x20;

#### ¿Tiene otras preguntas?

La mejor manera de obtener ayuda tanto de nuestros equipos de ingeniería como de negocios es generalmente en [Discord](https://www.originprotocol.com/discord). &#x20;

