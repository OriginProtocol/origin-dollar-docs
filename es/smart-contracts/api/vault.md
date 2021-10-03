---
description: >-
  La bóveda es el contrato principal del protocolo. La bóveda es responsable de acuñar/canjear tokens OUSD, reequilibrar fondos entre las diversas estrategias compatibles y liquidar tokens de recompensa.
---

# Bóveda

## Unidades

Todas las cantidades de OUSD aprobadas o devueltas por los métodos de Vault utilizan 18 lugares decimales. Por ejemplo, 1 OUSD se expresa como 1000000000000000000.

Para otras monedas estables, el número de decimales varía. DAI usa 18 lugares decimales, mientras que USDC y USDT usan solo 6.

Los esfuerzos están [actualmente en marcha](https://github.com/OriginProtocol/origin-dollar/issues/590) para aumentar la resolución de cálculos de cambio de base a partir de 18 decimales a 27 decimales. El token de OUSD en sí mismo conservará 18 decimales de precisión y los saldos de los usuarios no deberían cambiar.

## Métodos

### mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**

Acuñar OUSD a cambio de un depósito de un determinado `_amount` de moneda estable especificado por el `_asset` parámetro. La persona que llama recibe una cierta cantidad de OUSD dependiendo del **tipo de cambio**.

| Nombre del parámetro  | Tipo      | Descripción                                                                                                                                             |
|:--------------------- |:--------- |:------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset             | dirección | Dirección de la moneda estable [admitida](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets). |
| \_amount            | uint256   | Cantidad depositada, expresada en unidades decimales                                                                                                    |
| \_minimumOusdAmount | uint256   | Cantidad mínima de OUSD que la persona que llama está dispuesta a recibir. La llamada a mint\(\) se revierte si no se cumple el mínimo.               |

### mintMultiple \ (\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts, uint256 _minimumOusdAmount)`**‌

Acuñar OUSD a cambio de un depósito de múltiples monedas estables en una sola llamada. Las monedas estables se especifican mediante el parámetro de matriz `_assets` y las cantidades mediante el parámetro de matriz `_amounts`. La persona que llama recibe una cierta cantidad de OUSD dependiendo del **tipo de cambio**.

| Nombre del parámetro  | Tipo            | Descripción                                                                                                                                                   |
|:--------------------- |:--------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets            | dirección\[\] | Direcciones de las monedas estables [admitidas](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets). |
| \_amounts           | uint256\[\]   | Cantidades depositadas, expresadas en unidades decimales                                                                                                      |
| \_minimumOusdAmount | uint256         | Cantidad mínima de OUSD que la persona que llama está dispuesta a recibir. La llamada a mint\(\) se revierte si no se cumple el mínimo.                     |

{% hint style="warning" %}
En los canjes, es el protocolo y no el usuario el que decide qué monedas estables\(s\) se devuelven al usuario. Esta decisión de qué moneda \(s\) devolver se basa en las relaciones internas de los activos que se mantienen en la bóveda.
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**

El OUSD especificado parámetro `_amount` canjea a cambio de una o varias monedas estables admitidas. La cantidad de monedas estables recibidas depende del **tipo de cambio**.

| Nombre del parámetro | Tipo    | Descripción                                      |
|:-------------------- |:------- |:------------------------------------------------ |
| \_amount           | uint256 | cantidad de OUSD expresada en unidades decimales |

### redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**

Todo el OUSD en posesión del usuario se canjea a cambio de una o varias monedas estables compatibles. La cantidad de monedas estables recibidas depende del **tipo de cambio**.

### rebase\(\) <a id="rebase"></a>

**`function rebase()`**

Actualiza los saldos de todos los usuarios según el valor de los activos almacenados actualmente en la bóveda. Devuelve el valor total de los activos y estrategias subyacentes representados por el tipo `uint256`.

### allocate\(\) <a id="allocate"></a>

**`function allocate()`**

Mueve los activos bajo administración a sus [estrategias](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) prescritas para maximizar el rendimiento y diversificar el riesgo.

### totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**

Devuelve el valor total de los activos y estrategias subyacentes.

| `return` nombre | Tipo    | Descripción                                           |
|:--------------- |:------- |:----------------------------------------------------- |
| valor           | uint256 | valor total de los activos y estrategias subyacentes. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**

Devuelve el saldo de un activo especificado por el parámetro`_asset` contenido en la Bóveda y todas las estrategias representadas por el tipo `uint256`.

| Nombre del parámetro | Tipo      | Descripción                                                                                                                                             |
|:-------------------- |:--------- |:------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset            | dirección | Dirección de la moneda estable [admitida](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets). |

### calculateRedeemOutputs\(\)<a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**

Calcule la combinación de monedas estables que una función `redeem` devolvería al canjear cierta cantidad de OUSD especificada por el parámetro `_amount`. Devuelve una matriz de valores de monedas estables.

Para atribuir los valores de la moneda estable a la moneda de la moneda estable correcta, esta llamada debe usarse junto con la función `getAllAssets` que devuelve una matriz de direcciones de la moneda estable.

El índice de una matriz que devuelve `calculateRedeemOutputs` corresponde a la dirección de la moneda estable con el mismo índice en una matriz devuelta por la función `getAllAssets`.

| Nombre del parámetro | Tipo    | Descripción                                      |
|:-------------------- |:------- |:------------------------------------------------ |
| \_amount           | uint256 | cantidad de OUSD expresada en unidades decimales |

| `return` nombre | Tipo          | Descripción                                                                    |
|:--------------- |:------------- |:------------------------------------------------------------------------------ |
| salidas         | uint256\[\] | matriz de la cantidad de activos de moneda estable `redeem` función devolvería |

### getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**

Return the number of supported stablecoin assets represented by `uint256` type.‌

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

Return all assets addresses of supported stablecoin assets in order represented by `uint256` type.‌

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Return the number of strategies active on the Vault represented by `uint256` type.‌

### getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield \(APR\) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal places.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Nombre del parámetro | Tipo      | Descripción                    |
|:-------------------- |:--------- |:------------------------------ |
| \_asset            | dirección | Dirección de la moneda estable |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nombre del parámetro | Tipo   | Descripción                  |
|:-------------------- |:------ |:---------------------------- |
| symbol               | string | Símbolo de la moneda estable |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nombre del parámetro | Tipo   | Descripción                  |
|:-------------------- |:------ |:---------------------------- |
| symbol               | string | Símbolo de la moneda estable |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nombre del parámetro | Tipo      | Descripción                     |
|:-------------------- |:--------- |:------------------------------- |
| \_asset            | dirección | Dirección de la moneda estable‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Nombre del parámetro | Tipo      | Descripción                    |
|:-------------------- |:--------- |:------------------------------ |
| \_asset            | dirección | Dirección de la moneda estable |

