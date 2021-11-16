---
description: >-
  La bóveda es el contrato principal del protocolo. La bóveda es responsable de acuñar/canjear tokens OUSD, reequilibrar fondos entre las diversas estrategias compatibles y liquidar tokens de recompensa.
---

# Bóveda

## Unidades

Todas las cantidades de OUSD aprobadas o devueltas por los métodos de Vault utilizan 18 lugares decimales. Por ejemplo, 1 OUSD se expresa como 1000000000000000000.

Para otras monedas estables, el número de decimales varía. DAI usa 18 lugares decimales, mientras que USDC y USDT usan solo 6.

The protocol was updated in November  are [currently underway](https://github.com/OriginProtocol/origin-dollar/issues/590) to increase the resolution of rebasing calculations from 18 decimals to 27 decimals. El token de OUSD en sí mismo conservará 18 decimales de precisión y los saldos de los usuarios no deberían cambiar.

## Métodos

### mint() <a href="mint" id="mint"></a>

**`function mint(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**

Acuñar OUSD a cambio de un depósito de un determinado `_amount` de moneda estable especificado por el `_asset` parámetro. La persona que llama recibe una cierta cantidad de OUSD dependiendo del **tipo de cambio**.

| Nombre del parámetro  | Tipo      | Descripción                                                                                                                                          |
| --------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset             | dirección | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |
| \_amount            | uint256   | Cantidad depositada, expresada en unidades decimales                                                                                                 |
| \_minimumOusdAmount | uint256   | Cantidad mínima de OUSD que la persona que llama está dispuesta a recibir. The call to mint() reverts if the minimum is not met.                     |

### mintMultiple() <a href="mintmultiple" id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts, uint256 _minimumOusdAmount)`**‌

Acuñar OUSD a cambio de un depósito de múltiples monedas estables en una sola llamada. Las monedas estables se especifican mediante el parámetro de matriz `_assets` y las cantidades mediante el parámetro de matriz `_amounts`. La persona que llama recibe una cierta cantidad de OUSD dependiendo del **tipo de cambio**.

| Nombre del parámetro  | Tipo        | Descripción                                                                                                                                             |
| --------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets            | address\[] | Addresses of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |
| \_amounts           | uint256\[] | Cantidades depositadas, expresadas en unidades decimales                                                                                                |
| \_minimumOusdAmount | uint256     | Cantidad mínima de OUSD que la persona que llama está dispuesta a recibir. The call to mint() reverts if the minimum is not met.                        |

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin(s) are returned to the user. This decision of which coin(s) to return is based on the internal ratios of the assets that are being held in the vault.‌
{% endhint %}

### redeem() <a href="redeem" id="redeem"></a>

**`function redeem(uint256 _amount)`**

El OUSD especificado parámetro `_amount` canjea a cambio de una o varias monedas estables admitidas. La cantidad de monedas estables recibidas depende del **tipo de cambio**.

| Nombre del parámetro | Tipo    | Descripción                                      |
| -------------------- | ------- | ------------------------------------------------ |
| \_amount           | uint256 | cantidad de OUSD expresada en unidades decimales |

### redeemAll()‌ <a href="redeemall" id="redeemall"></a>

**`function redeemAll()`**

Todo el OUSD en posesión del usuario se canjea a cambio de una o varias monedas estables compatibles. La cantidad de monedas estables recibidas depende del **tipo de cambio**.

### rebase() <a href="rebase" id="rebase"></a>

**`function rebase()`**

Actualiza los saldos de todos los usuarios según el valor de los activos almacenados actualmente en la bóveda. Devuelve el valor total de los activos y estrategias subyacentes representados por el tipo `uint256`.

### allocate() <a href="allocate" id="allocate"></a>

**`function allocate()`**

Moves the assets under management into their prescribed [Stategies](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) to maximize yield and diversify risk.‌

### totalValue() <a href="totalvalue" id="totalvalue"></a>

**`function totalValue()`**

Devuelve el valor total de los activos y estrategias subyacentes.

| `return` nombre | Tipo    | Descripción                                           |
| --------------- | ------- | ----------------------------------------------------- |
| valor           | uint256 | valor total de los activos y estrategias subyacentes. |

### checkBalance() <a href="checkbalance" id="checkbalance"></a>

**`function checkBalance(address _asset)`**

Devuelve el saldo de un activo especificado por el parámetro`_asset` contenido en la Bóveda y todas las estrategias representadas por el tipo `uint256`.

| Nombre del parámetro | Tipo      | Descripción                                                                                                                                          |
| -------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset            | dirección | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs() <a href="calculateredeemoutputs" id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**

Calcule la combinación de monedas estables que una función `redeem` devolvería al canjear cierta cantidad de OUSD especificada por el parámetro `_amount`. Devuelve una matriz de valores de monedas estables.

Para atribuir los valores de la moneda estable a la moneda de la moneda estable correcta, esta llamada debe usarse junto con la función `getAllAssets` que devuelve una matriz de direcciones de la moneda estable.

El índice de una matriz que devuelve `calculateRedeemOutputs` corresponde a la dirección de la moneda estable con el mismo índice en una matriz devuelta por la función `getAllAssets`.

| Nombre del parámetro | Tipo    | Descripción                                      |
| -------------------- | ------- | ------------------------------------------------ |
| \_amount           | uint256 | cantidad de OUSD expresada en unidades decimales |

| `return` nombre | Tipo        | Descripción                                                                    |
| --------------- | ----------- | ------------------------------------------------------------------------------ |
| salidas         | uint256\[] | matriz de la cantidad de activos de moneda estable `redeem` función devolvería |

### getAssetCount() <a href="getassetcount" id="getassetcount"></a>

**`function getAssetCount()`**

Devuelve el número de activos de stablecoin admitidos representados por el tipo `uint256`.

### getAllAssets() <a href="getallassets" id="getallassets"></a>

**`function getAllAssets()`**

Devuelve el número de activos de moneda estable admitidos representados por el tipo `uint256`.

### getStrategyCount()‌ <a href="getstrategycount" id="getstrategycount"></a>

**`function getStrategyCount()`**

Devuelve el número de estrategias activas en la Bóveda representado por `uint256` tipo.

### getAPR() <a href="getapr" id="getapr"></a>

**`function getAPR ()`**

Return the total annual percentage yield (APR) of the Vault and all Strategies represented by `uint256` type. El número resultante tiene 18 espacios decimales.

### isSupportedAsset() <a href="issupportedasset" id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**

Devuelve el valor booleano verdadero si el activo especificado por el parámetro `_asset` es compatible con la Bóveda.

| Nombre del parámetro | Tipo      | Descripción                    |
| -------------------- | --------- | ------------------------------ |
| \_asset            | dirección | Dirección de la moneda estable |

### priceUSDMint() <a href="issupportedasset-1" id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**

Devuelve el precio del tipo de cambio de una moneda estable especificado por los parámetros del `symbol` utilizados al acuñar OUSD representado por el tipo `uint256`. El número resultante tiene 18 decimales.

| Nombre del parámetro | Tipo   | Descripción                  |
| -------------------- | ------ | ---------------------------- |
| symbol               | string | Símbolo de la moneda estable |

### priceUSDRedeem() <a href="issupportedasset-2" id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**

Devuelve el precio del tipo de cambio de una moneda estable especificado por los parámetros del `symbol` utilizados al canjear OUSD representado por el tipo `uint256`. El número resultante tiene 18 decimales.

| Nombre del parámetro | Tipo   | Descripción                  |
| -------------------- | ------ | ---------------------------- |
| symbol               | string | Símbolo de la moneda estable |

### priceAssetUSDMint()‌ <a href="issupportedasset-3" id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**

Devuelve el precio del tipo de cambio de una moneda estable especificado por los parámetros `_asset` utilizados al acuñar OUSD representado por el tipo `uint256`. El número resultante tiene 18 decimales.

| Nombre del parámetro | Tipo      | Descripción                     |
| -------------------- | --------- | ------------------------------- |
| \_asset            | dirección | Dirección de la moneda estable‌ |

### priceAssetUSDRedeem()‌ <a href="issupportedasset-3-1" id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**

Devuelve el precio de tipo de cambio de una moneda estable especificado por los parámetros `_asset` utilizados al canjear OUSD representado por el tipo `uint256`. El número resultante tiene 18 decimales.

| Nombre del parámetro | Tipo      | Descripción                    |
| -------------------- | --------- | ------------------------------ |
| \_asset            | dirección | Dirección de la moneda estable |
