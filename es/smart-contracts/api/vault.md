---
description: >-
  La bóveda es el contrato principal del protocolo. La bóveda es responsable de acuñar/canjear tokens OUSD, reequilibrar fondos entre las diversas estrategias compatibles y liquidar tokens de recompensa.
---

# Bóveda

## Métodos

### mint\(\) <a id="mint"></a>

**`función mint (dirección _asset, uint256 _amount)`**

Acuñar OUSD a cambio de un depósito de un determinado `_amount` de moneda estable especificado por el `_asset` parámetro. La persona que llama recibe una cierta cantidad de OUSD dependiendo del **tipo de cambio**.

| Nombre del parámetro | Tipo      | Descripción                                                                                                                                             |
|:-------------------- |:--------- |:------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset            | dirección | Dirección de la moneda estable [admitida](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets). |
| \_amount           | uint256   | cantidad depositada, expresada en unidades decimales                                                                                                    |

### mintMultiple \ (\) <a id="mintmultiple"></a>

**`función mint (dirección _asset, uint256 _amount)`**

Acuñar OUSD a cambio de un depósito de múltiples monedas estables en una sola llamada. Las monedas estables se especifican mediante el parámetro de matriz `_assets` y las cantidades mediante el parámetro de matriz `_amounts`. La persona que llama recibe una cierta cantidad de OUSD dependiendo del **tipo de cambio**.

| Nombre del parámetro | Tipo            | Descripción                                                                                                                                                   |
|:-------------------- |:--------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets           | dirección\[\] | Direcciones de las monedas estables [admitidas](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets). |
| \_amounts          | uint256\[\]   | cantidades depositadas, expresadas en unidades decimales                                                                                                      |

{% hint style="warning" %}
En los canjes, es el protocolo y no el usuario el que decide qué moneda estable \(s\) devolver al usuario. Esta decisión de qué moneda \(s\) devolver se basa en las relaciones internas de los activos que se mantienen en la bóveda.
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`función redeem(uint256 _amount)`**

El OUSD especificado parámetro `_amount` canjea a cambio de una o varias monedas estables admitidas. La cantidad de monedas estables recibidas depende del **tipo de cambio**.

| Nombre del parámetro | Tipo    | Descripción                                      |
|:-------------------- |:------- |:------------------------------------------------ |
| \_amount           | uint256 | cantidad de OUSD expresada en unidades decimales |

### redeemAll\(\)‌ <a id="redeemall"></a>

**`función redeemAll()`**

Todo el OUSD en posesión del usuario se canjea a cambio de una o varias monedas estables compatibles. La cantidad de monedas estables recibidas depende del **tipo de cambio**.

### rebase\(\) <a id="rebase"></a>

**`función rebase()`**

Actualiza los saldos de todos los usuarios según el valor de los activos almacenados actualmente en la bóveda. Devuelve el valor total de los activos y estrategias subyacentes representados por el tipo `uint256`.

### allocate\(\) <a id="allocate"></a>

**`función allocate()`**

Mueve los activos bajo administración a sus [estrategias](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) prescritas para maximizar el rendimiento y diversificar el riesgo.

### totalValue\(\) <a id="totalvalue"></a>

**`función totalValue()`**

Devuelve el valor total de los activos y estrategias subyacentes.

| `return` nombre | Tipo    | Descripción                                           |
|:--------------- |:------- |:----------------------------------------------------- |
| valor           | uint256 | valor total de los activos y estrategias subyacentes. |

### checkBalance\(\) <a id="checkbalance"></a>

**`función checkBalance()`**

Devuelve el saldo de un activo especificado por el parámetro`_asset` contenido en la Bóveda y todas las estrategias representadas por el tipo `uint256`.

| Parameter Name | Type    | Description                                                                                                                                        |
|:-------------- |:------- |:-------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset      | address | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| Parameter Name | Type    | Description                               |
|:-------------- |:------- |:----------------------------------------- |
| \_amount     | uint256 | amount of OUSD expressed in decimal units |

| `return` name | Type          | Description                                                                 |
|:------------- |:------------- |:--------------------------------------------------------------------------- |
| outputs       | uint256\[\] | array of the amount of the stablecoin assets `redeem` function would return |

### getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Return the number of supported stablecoin assets represented by `uint256` type.‌

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

Return all assets addresses of supported stablecoin assets in order represented by `uint256` type.‌

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Return the number of strategies active on the Vault represented by `uint256` type.‌

### getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield \(APR\) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal spaces.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Parameter Name | Type    | Description               |
|:-------------- |:------- |:------------------------- |
| \_asset      | address | Address of the stablecoin |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type   | Description              |
|:-------------- |:------ |:------------------------ |
| symbol         | string | Symbol of the stablecoin |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type   | Description              |
|:-------------- |:------ |:------------------------ |
| symbol         | string | Symbol of the stablecoin |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type    | Description                |
|:-------------- |:------- |:-------------------------- |
| \_asset      | address | Address of the stablecoin‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type    | Description               |
|:-------------- |:------- |:------------------------- |
| \_asset      | address | Address of the stablecoin |

