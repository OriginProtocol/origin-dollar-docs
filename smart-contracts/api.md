# API

## Vault

The vault is the main contract of the the protocol. The vault is responsible for minting/redeeming OUSD tokens, rebalancing funds between the various supported strategies, and liquidating rewards tokens.

### Methods

#### mint\(\)

**`function mint(address _asset, uint256 _amount)`**

Mints OUSD in exchange for a deposit of a certain `_amount` of stablecoin specified by the `_asset` parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| Parameter Name | Type | Description |
| :--- | :--- | :--- |
| \_asset | address | Address of the [supported](../core-concepts/supported-assets/) stablecoin  |
| \_amount | uint256 | amount deposited, expressed in decimal units |

#### 

#### mintMultiple\(\)

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**

Mints OUSD in exchange for a deposit of multiple stablecoins in a single call. Stablecoins are specified by the `_assets` array parameter and the amounts by the `_amounts` array parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| Parameter Name | Type | Description |
| :--- | :--- | :--- |
| \_assets | address\[\] | Addresses of the [supported](../core-concepts/supported-assets/) stablecoins  |
| \_amounts | uint256\[\] | amounts deposited, expressed in decimal units |

#### redeem\(\)

**`function redeem(uint256 _amount)`**

OUSD specified by the `_amount` parameter is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

| Parameter Name | Type | Description |
| :--- | :--- | :--- |
| \_amount | uint256 | amount of OUSD expressed in decimal units  |

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) are returned to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.
{% endhint %}

#### redeemAll\(\)

**`function redeemAll()`**

All OUSD in user's possession is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) are returned to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.
{% endhint %}

### rebase\(\)

**`function rebase()`**

Updates the balances for all users based on the value of the assets currently stored in the pool. Returns total value of the underlying assets and strategies of `uint256` type.

### allocate\(\)

**`function allocate()`**

Moves the assets under management into their prescribed [Stategies](../architecture/strategies.md) to maximize yield and diversify risk.

### totalValue\(\)

**`function totalValue()`**

Returns total value of underlying assets and strategies.

| `return` name | Type | Description |
| :--- | :--- | :--- |
| value | uint256 | total value of underlying assets and strategies. |

### checkBalance\(\)

**`function checkBalance(address _asset)`**

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies of `uint256` type.

| Parameter Name | Type | Description |
| :--- | :--- | :--- |
| \_asset | address | Address of the [supported](../core-concepts/supported-assets/) stablecoin  |

### calculateRedeemOutputs\(\)

**`function calculateRedeemOutputs(uint256 _amount)`**

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount`  parameter. Returns an array of stablecoin values. 

{% hint style="info" %}
To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses. 

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.  
{% endhint %}

| Parameter Name | Type | Description |
| :--- | :--- | :--- |
| \_amount | uint256 | amount of OUSD expressed in decimal units  |

| `return` name | Type | Description |
| :--- | :--- | :--- |
| outputs | uint256\[\] | array of the amount of the stablecoin assets `redeem` function would return |

### getAssetCount\(\)

**`function getAssetCount()`**

Return the number of supported stablecoin assets of `uint256` type.

### getAllAssets\(\)

**`function getAllAssets()`**

Return all assets addresses of supported stablecoin assets in order of `uint256` type.

### getStrategyCount\(\)

**`function getStrategyCount()`**

Return the number of strategies active on the Vault of uint.

