---
description: >-
  保险库是协议的核心合约。 保险库负责铸造/兑现 OUSD 代币，在各种支持的策略之间重新平衡资金以及清算奖励代币。
---

# 保险库 （Vault）

## 方式

### mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**

Mints OUSD in exchange for a deposit of a certain `_amount` of stablecoin specified by the `_asset` parameter. 收到的 OUSD 数量将根据当时的 **汇率**。

| 参数名称       | 种类      | 描述                                                                                                                        |
|:---------- |:------- |:------------------------------------------------------------------------------------------------------------------------- |
| \_asset  | address | [支持](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) 的稳定币的地址 |
| \_amount | uint256 | 存入金额，以十进制单位表示                                                                                                             |

### mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**

Mints OUSD in exchange for a deposit of multiple stablecoins in a single call. Stablecoins are specified by the `_assets` array parameter and the amounts by the `_amounts` array parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| 参数名称        | 种类            | 描述                                                                                                                        |
|:----------- |:------------- |:------------------------------------------------------------------------------------------------------------------------- |
| \_assets  | address\[\] | [支持](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) 的稳定币的地址 |
| \_amounts | uint256\[\] | 存入金额，以十进制单位表示                                                                                                             |

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) are returned to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the vault.‌
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD specified by the `_amount` parameter is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

| 参数名称       | 种类      | 描述              |
|:---------- |:------- |:--------------- |
| \_amount | uint256 | 以十进制单位表示的OUSD金额 |

### redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**

将用户拥有的所有 OUSD 换取一种或多种受支持的稳定币。 收到的稳定币数量取决于 **汇率**。

### rebase\(\) <a id="rebase"></a>

**`function rebase()`**‌

Updates the balances for all users based on the value of the assets currently stored in the vault. Returns total value of the underlying assets and strategies represented by `uint256` type.‌

### allocate\(\) <a id="allocate"></a>

**`function allocate()`**‌

Moves the assets under management into their prescribed [Stategies](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) to maximize yield and diversify risk.‌

### totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**‌

Returns total value of underlying assets and strategies.

| `return` name | 种类      | 描述           |
|:------------- |:------- |:------------ |
| value         | uint256 | 底层资产和策略的总价值。 |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| 参数名称      | 种类      | 描述                                                                                                                        |
|:--------- |:------- |:------------------------------------------------------------------------------------------------------------------------- |
| \_asset | address | [支持](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) 的稳定币的地址 |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| 参数名称       | 种类      | 描述              |
|:---------- |:------- |:--------------- |
| \_amount | uint256 | 以十进制单位表示的OUSD金额 |

| `return` name | 种类            | 描述                                                                          |
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

| 参数名称      | 类型      | 描述    |
|:--------- |:------- |:----- |
| \_asset | address | 稳定币地址 |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 参数名称   | 种类     | 描述     |
|:------ |:------ |:------ |
| symbol | string | 稳定币的符号 |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 参数名称   | 种类     | 描述     |
|:------ |:------ |:------ |
| symbol | string | 稳定币的符号 |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 参数名称      | 种类      | 描述     |
|:--------- |:------- |:------ |
| \_asset | address | 稳定币地址‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 参数名称      | 种类      | 描述    |
|:--------- |:------- |:----- |
| \_asset | address | 稳定币地址 |

