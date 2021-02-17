---
description: >-
  Vault - это главный контракт протокола. Vault отвечает за создание и выкуп токенов OUSD, перебалансировку средств между различными поддерживаемыми стратегиями и ликвидацию токенов вознаграждения.
---

# Хранилище (Vault)

## Units

Все суммы OUSD, переданные или возвращенные методами Vault, являются 18-ти разрядными. К примеру, 1 OUSD выражается как 1000000000000000000.

Разрядность других стейблкоинов отличается. DAI использует 18 знаков после запятой, в то время как USDC и USDT имеют только 6 разрядов.

## Методы‌

### mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**‌

Создает новые токены OUSD в обмен на определенное количество `__amount` стейблкоинов, указанных параметром `_asset`. Вызывающий функцию получает определенное количество OUSD в зависимости от **обменного курса**.

| Имя параметра         | Тип     | Описание                                                                                                                                         |
|:--------------------- |:------- |:------------------------------------------------------------------------------------------------------------------------------------------------ |
| \_asset             | адрес   | Адрес [поддерживаемого](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) стейблкоина |
| \_amount            | uint256 | Amount deposited, expressed in decimal units                                                                                                     |
| \_minimumOusdAmount | uint256 | Minimum amount of OUSD the caller is willing to receive. The call to mint\(\) reverts if the minimum is not met.                               |

### mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts, uint256 _minimumOusdAmount)`**

Создает новые токены OUSD в обмен на определенное количество разных стейблкоинов за один вызов функции. Стейблкоины указываются параметром массива `_assets` а суммы - параметром массива `_amounts`. Вызывающий функцию получает определенное количество OUSD в зависимости от **обменного курса**.

| Имя параметра         | Тип           | Описание                                                                                                                                                         |
|:--------------------- |:------------- |:---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets            | address\[\] | Адреса [поддерживаемых](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) стейблкоинов                |
| \_amounts           | uint256\[\] | Amounts deposited, expressed in decimal units                                                                                                                    |
| \_minimumOusdAmount | uint256       | Минимальное количество OUSD, получаемое в процессе вызова функции. Вызов функции mint\(\) отменяется, если количество создаваемых токенов меньше минимального. |

{% hint style="warning" %}
Во время выкупа именно протоколом, а не пользователем, принимается решение о том, какой (-ие) стейблкоин (-ы) возвращаются пользователю. Решение о том, какую монету (-ы) возвратить, основывается на внутренних соотношениях активов в хранилище.‌
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD specified by the `_amount` parameter is redeemed in exchange for one or multiple supported stablecoins. Количество полученных стейблкоинов зависит от **обменного курса**.

| Имя параметра | Тип     | Описание                                          |
|:------------- |:------- |:------------------------------------------------- |
| \_amount    | uint256 | количество OUSD, выраженное в десятичных единицах |

### redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**‌

All OUSD in user's possession is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

### rebase\(\) <a id="rebase"></a>

**`function rebase()`**‌

Updates the balances for all users based on the value of the assets currently stored in the vault. Returns total value of the underlying assets and strategies represented by `uint256` type.‌

### allocate\(\) <a id="allocate"></a>

**`function allocate()`**‌

Moves the assets under management into their prescribed [Stategies](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) to maximize yield and diversify risk.‌

### totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**‌

Returns total value of underlying assets and strategies.

| Имя параметра | Тип     | Описание                                     |
|:------------- |:------- |:-------------------------------------------- |
| value         | uint256 | общая стоимость базовых активов и стратегий. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| Имя параметра | Тип   | Описание                                                                                                                                         |
|:------------- |:----- |:------------------------------------------------------------------------------------------------------------------------------------------------ |
| \_asset     | адрес | Адрес [поддерживаемого](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) стейблкоина |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| Имя параметра | Тип     | Описание                                     |
|:------------- |:------- |:-------------------------------------------- |
| \_amount    | uint256 | сумма OUSD, выраженная в десятичных единицах |

| `Возврат` имени | Тип           | Описание                                                  |
|:--------------- |:------------- |:--------------------------------------------------------- |
| outputs         | uint256\[\] | массив суммы активов стейблкоина `redeem`, функция вернет |

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

Return the total annual percentage yield \(APR\) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal places.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Имя параметра | Тип   | Описание          |
|:------------- |:----- |:----------------- |
| \_asset     | адрес | Адрес стейблкоина |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Имя параметра | Тип    | Описание           |
|:------------- |:------ |:------------------ |
| символ        | строка | Символ стейблкоина |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Имя параметра | Тип    | Описание           |
|:------------- |:------ |:------------------ |
| символ        | строка | Символ стейблкоина |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Имя параметра | Тип   | Описание           |
|:------------- |:----- |:------------------ |
| \_asset     | адрес | Адрес стейблкоина‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal places.

| Имя параметра | Тип   | Описание          |
|:------------- |:----- |:----------------- |
| \_asset     | адрес | Адрес стейблкоина |

