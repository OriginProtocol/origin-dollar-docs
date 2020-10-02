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

| Nombre del parámetro | Tipo      | Descripción                                                                                                                                             |
|:-------------------- |:--------- |:------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset            | dirección | Dirección de la moneda estable [admitida](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets). |

### calculateRedeemOutputs\(\)<a id="calculateredeemoutputs"></a>

**`función calculateRedeemOutputs(uint256 _amount)`**

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

**`función getAssetCount()`**

Devuelve el número de activos de stablecoin admitidos representados por el tipo `uint256`.

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**

Devuelve el número de activos de moneda estable admitidos representados por el tipo `uint256`.

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount ()`**

Devuelve el número de estrategias activas en la Bóveda representado por `uint256` tipo.

### getAPR\(\) <a id="getapr"></a>

**`function getAPR ()`**

Devuelve el rendimiento porcentual anual total \ (APR \) de la Bóveda y todas las estrategias representadas por el tipo `uint256`. El número resultante tiene 18 espacios decimales.

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**

Devuelve el valor booleano verdadero si el activo especificado por el parámetro `_asset` es compatible con la Bóveda.

| Nombre del parámetro | Tipo      | Descripción                    |
|:-------------------- |:--------- |:------------------------------ |
| \_asset            | dirección | Dirección de la moneda estable |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**

Devuelve el precio del tipo de cambio de una moneda estable especificado por los parámetros del `symbol` utilizados al acuñar OUSD representado por el tipo `uint256`. El número resultante tiene 18 espacios decimales.

| Nombre del parámetro | Tipo   | Descripción                  |
|:-------------------- |:------ |:---------------------------- |
| symbol               | string | Símbolo de la moneda estable |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**

Devuelve el precio del tipo de cambio de una moneda estable especificado por los parámetros del `symbol` utilizados al canjear OUSD representado por el tipo `uint256`. El número resultante tiene 18 espacios decimales.

| Nombre del parámetro | Tipo   | Descripción                  |
|:-------------------- |:------ |:---------------------------- |
| symbol               | string | Símbolo de la moneda estable |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**

Devuelve el precio del tipo de cambio de una moneda estable especificado por los parámetros `_asset` utilizados al acuñar OUSD representado por el tipo `uint256`. El número resultante tiene 18 espacios decimales.

| Nombre del parámetro | Tipo      | Descripción                     |
|:-------------------- |:--------- |:------------------------------- |
| \_asset            | dirección | Dirección de la moneda estable‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**

Devuelve el precio de tipo de cambio de una moneda estable especificado por los parámetros `_asset` utilizados al canjear OUSD representado por el tipo `uint256`. El número resultante tiene 18 espacios decimales.

| Nombre del parámetro | Tipo      | Descripción                    |
|:-------------------- |:--------- |:------------------------------ |
| \_asset            | dirección | Dirección de la moneda estable |

