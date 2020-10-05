---
description: >-
  Vault - это главный контракт протокола. Vault отвечает за создание и выкуп токенов OUSD, перебалансировку средств между различными поддерживаемыми стратегиями и ликвидацию токенов вознаграждения.
---

# Хранилище (Vault)

## Методы‌

### mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**‌

Создает OUSD в обмен на депозит определенного количества `__amount` стейблкоинов, указанных параметром `_asset`. Вызывающий функцию получает определенную сумму OUSD в зависимости от **курса обмена**.

| Имя параметра | Тип     | Описание                                                                                                                                           |
|:------------- |:------- |:-------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset     | address | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |
| \_amount    | uint256 | amount deposited, expressed in decimal units                                                                                                       |

### mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**‌

Mints OUSD in exchange for a deposit of multiple stablecoins in a single call. Stablecoins are specified by the `_assets` array parameter and the amounts by the `_amounts` array parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| Parameter Name | Type          | Description                                                                                                                                           |
|:-------------- |:------------- |:----------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets     | address\[\] | Addresses of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |
| \_amounts    | uint256\[\] | amounts deposited, expressed in decimal units                                                                                                         |

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) are returned to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the vault.‌
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD specified by the `_amount` parameter is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

| Parameter Name | Type    | Description                               |
|:-------------- |:------- |:----------------------------------------- |
| \_amount     | uint256 | amount of OUSD expressed in decimal units |

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

| `return` name | Type    | Description                                      |
|:------------- |:------- |:------------------------------------------------ |
| value         | uint256 | total value of underlying assets and strategies. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| Parameter Name | Type    | Description                                                                                                                                        |
|:-------------- |:------- |:-------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset      | address | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Возвращает массив значений стейблкоинов.

Чтобы соотносить стоимость стейблкоина с правильным курсом стейблкоина, этот вызов функции следует использовать вместе с функцией `getAllAssets`, которая возвращает массив адресов стейблкоина.

Индекс массива, возвращаемый функцией `calculateRedeemOutputs` соответствует адресу стейблкоина с таким же индексом в массиве, возвращаемым функцией `getAllAssets`.

| Имя параметра | Тип     | Описание                                     |
|:------------- |:------- |:-------------------------------------------- |
| \_amount    | uint256 | сумма OUSD, выраженная в десятичных единицах |

| `return` name | Тип           | Описание                                                  |
|:------------- |:------------- |:--------------------------------------------------------- |
| outputs       | uint256\[\] | массив суммы активов стейблкоина `redeem`, функция вернет |

### getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Возвращает количество поддерживаемых активов стейблкоина, представленное типом `uint256`

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

Возвращает адреса балансов всех поддерживаемых стейблкоинов, представленных типом `uint256`

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Возвращает количество активных стратегий Хранилища (Vault), представленных типом `uint256`

### getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**

Возвращает общую годовую процентную доходность \(APR\) Хранилища (Vault) и всех стратегий, представленных типом `uint256`. Полученное число состоит из 18 десятичных знаков.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**

Возвращает двоичное значение, которое является истиной, если актив, указанный параметром `_asset` поддерживается Хранилищем (Vault).

| Имя параметра | Тип   | Описание          |
|:------------- |:----- |:----------------- |
| \_asset     | адрес | Адрес стейблкоина |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**

Возвращает обменный курс стейблкоина, заданный параметрами `symbol` используемыми при производстве OUSD, представленных типом `uint256`. Полученное число состоит из 18 десятичных знаков.

| Имя параметра | Тип    | Описание           |
|:------------- |:------ |:------------------ |
| символ        | строка | Символ стейблкоина |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**

Возвращает обменный курс стейблкоина, заданный параметрами `symbol` используемыми при выкупе OUSD, представленных типом `uint256`. Полученное число состоит из 18 десятичных знаков.

| Имя параметра | Тип    | Описание           |
|:------------- |:------ |:------------------ |
| символ        | строка | Символ стейблкоина |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Возвращает курс обмена стейблкоина, заданный параметрами `_asset` используемыми при производстве OUSD, представленных типом `uint256`. Полученное число состоит из 18 десятичных знаков.

| Имя параметра | Тип   | Описание           |
|:------------- |:----- |:------------------ |
| \_asset     | адрес | Адрес стейблкоина‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Возвращает курс обмена стейблкоина, заданный параметрами `_asset` используемыми при выкупе OUSD, представленных типом `uint256`. Полученное число состоит из 18 десятичных знаков.

| Имя параметра | Тип   | Описание          |
|:------------- |:----- |:----------------- |
| \_asset     | адрес | Адрес стейблкоина |

