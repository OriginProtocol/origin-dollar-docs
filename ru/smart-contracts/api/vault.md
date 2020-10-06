---
description: >-
  Vault - это главный контракт протокола. Vault отвечает за создание и выкуп токенов OUSD, перебалансировку средств между различными поддерживаемыми стратегиями и ликвидацию токенов вознаграждения.
---

# Хранилище (Vault)

## Методы‌

### mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**‌

Создает OUSD в обмен на депозит определенного количества `__amount` стейблкоинов, указанных параметром `_asset`. Вызывающий функцию получает определенную сумму OUSD в зависимости от **курса обмена**.

| Имя параметра | Тип     | Описание                                                                                                                                         |
|:------------- |:------- |:------------------------------------------------------------------------------------------------------------------------------------------------ |
| \_asset     | адрес   | Адрес [поддерживаемого](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) стейблкоина |
| \_amount    | uint256 | сумма депозита, выраженная в десятичных единицах                                                                                                 |

### mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**

Создает OUSD в обмен на депозит определенного количества разных стейблкоинов за один вызов функции. Стейблкоины указываются параметром массива `_assets` а суммы - параметром массива `_amounts`. Вызывающий функцию получает определенную сумму OUSD в зависимости от **курса обмена**.

| Имя параметра | Тип           | Описание                                                                                                                                          |
|:------------- |:------------- |:------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets    | address\[\] | Адреса [поддерживаемых](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) стейблкоинов |
| \_amounts   | uint256\[\] | сумма депозита, выраженная в десятичных единицах                                                                                                  |

{% hint style="warning" %}
Во время выкупа именно протоколом, а не пользователем, принимается решение о том, какой (-ие) стейблкоин (-ы) возвращаются пользователю. Решение о том, какую монету (-ы) возвратить, основывается на внутренних соотношениях активов, которые хранятся в пуле.‌
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**

OUSD, указанный в параметре `_amount`, выкупается в обмен на один или несколько поддерживаемых стейблкоинов. Количество полученных стейблкоинов зависит от **обменного курса**.

| Имя параметра | Тип     | Описание                                          |
|:------------- |:------- |:------------------------------------------------- |
| \_amount    | uint256 | количество OUSD, выраженное в десятичных единицах |

### redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**

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

| `return` name | Тип     | Описание                                         |
|:------------- |:------- |:------------------------------------------------ |
| value         | uint256 | total value of underlying assets and strategies. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| Имя параметра | Тип   | Описание                                                                                                                                         |
|:------------- |:----- |:------------------------------------------------------------------------------------------------------------------------------------------------ |
| \_asset     | адрес | Адрес [поддерживаемого](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) стейблкоина |

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

