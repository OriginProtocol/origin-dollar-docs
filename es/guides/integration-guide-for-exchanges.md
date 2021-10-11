# Guía de Integración para Exchanges

Los exchanges centralizados jugarán un papel importante para ayudarnos a alcanzar nuestra meta de hacer que OUSD sea omnipresente. Nos complace ayudar a cualquier exchange que desee que OUSD esté disponible para sus usuarios. Creemos que OUSD será una gran adición a cualquier exchange que quiera ofrecer una moneda estable superior y una nueva oportunidad de alto rendimiento para sus usuarios.

Estos documentos son un excelente punto de partida para comprender cómo funciona OUSD. Aquí hay algunas preguntas importantes para los exchanges que deseen integrar OUSD para considerar:

**¿Quieres participar del rendimiento que se genera?**

¡Asumimos que la respuesta será sí y también lo alentamos a seguir! Sin embargo, puede haber algunos casos en los que prefiera moverse rápido y listar OUSD sin participar en el [rebase de OUSD](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md) ya que es la integración más rápida y simple. Para los exchanges que desean incluir OUSD, pero tienen pocos recursos de ingeniería, es posible que desee iniciar la versión sin reajuste primero mientras sus ingenieros realizan los cambios necesarios. Para que OUSD no rebase, puede llamar a `rebaseOptOut()` desde cada billetera EOA que contiene OUSD, o no hacer nada si está almacenando OUSD en contratos inteligentes. El OUSD sin rebasar se comporta como cualquier otro token ERC-20.

**Are you storing customer balances on smart contracts (ie. multi-sigs) or EOA wallets?**

Cualquier contrato inteligente que tenga OUSD debe optar manualmente para recibir el rendimiento llamando a `rebaseOptIn()`. Esto se debe a la [oferta elástica](../core-concepts/elastic-supply/) y la [naturaleza de rebase](../core-concepts/elastic-supply/rebasing-and-smart-contracts.md). Muchos exchanges barren los fondos de los clientes en una billetera multi-sig para almacenamiento en frío. Si hace esto, querrá asegurarse de optar por el cambio de base para que siempre esté ganando.

**¿Está almacenando en caché los saldos de los usuarios?**

OUSD actualiza dinámicamente el valor devuelto por la función `balanceOf()` en nuestro contrato ERC20. Los saldos de los usuarios se actualizarán en momentos impredecibles a medida que el protocolo genere un nuevo rendimiento. Mientras no esté almacenando en caché este valor, los usuarios siempre verán la cantidad correcta de OUSD que tienen.

**¿Está mezclando fondos de usuario?**

Si está reuniendo fondos, querrá asegurarse de que cada usuario obtenga su cantidad prorrateada del rendimiento que genera el protocolo. Probablemente la forma más fácil de hacer esto es rastrear el saldo de cada usuario como un porcentaje de un grupo en lugar de como una cantidad fija.

**¿Cuál es su plan de liquidez?**

OUSD se puede acuñar o canjear en cualquier momento utilizando [Origin Dollar DApp](https://www.ousd.com), o directamente desde nuestros contratos inteligentes. Si planea proporcionar liquidez usted mismo, debe tener en cuenta que la cantidad exacta de OUSD que recibirá a cambio de su USDT, USDC o DAI depende de los tipos de cambio actuales según lo determinado por los [oráculos](../smart-contracts/api/oracle.md). Si planea canjear OUSD por las monedas estables subyacentes, debe saber que hay una tarifa de salida del 0.5% y OUSD devolverá una canasta de monedas estables en proporción a las monedas estables de respaldo en el grupo. Alentamos a los intercambios a aprovechar otros grupos de liquidez, como Uniswap o Curve para evitar esas tarifas. Si es posible, las acuñaciones o canjeos deben hacerse en lotes grandes para una máxima eficiencia. 

