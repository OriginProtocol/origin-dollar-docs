---
description: >-
  금고(vault) 는 프로토콜의 핵심입니다. 금고는 OUSD 토큰의 채굴 / 교환, 다양한 지원 전략 간의 자금 재조정, 보상 토큰 청산을
  담당합니다.
---

# 금고\(Vault\)

## 방법

### 발행\(mint\)\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**

Mints OUSD in exchange for a deposit of a certain `_amount` of stablecoin specified by the `_asset` parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | address | 지원되는\( [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)\) 스테이블 코인 주 |
| \_amount | uint256 | 입금된 금액은 소수 단위로 표시 |

### mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**‌

Mints OUSD in exchange for a deposit of multiple stablecoins in a single call. Stablecoins are specified by the `_assets` array parameter and the amounts by the `_amounts` array parameter. The caller receives a certain amount of OUSD depending on the **exchange rate**.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_assets | address\[\] | 지원되는\( [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)\) 스테이블 코인 주 |
| \_amounts | uint256\[\] | 입금된 금액은 소수 단위로 표시 |

{% hint style="warning" %}
재할당 시 사용자에게 반환되는 스테이블 코인을 결정하는 것은 프로토콜이 아니라 사용자입니다. 이러한 코인 반환 결정은 금고에 보관 중인 자산의 내부 비율을 기반으로 합니다.‌
{% endhint %}

### 상환/redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD specified by the `_amount` parameter is redeemed in exchange for one or multiple supported stablecoins. Amount of stablecoins received depends on the **exchange rate**.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_amount | uint256 | amount of OUSD expressed in decimal units |

### 전액상환/redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**‌

사용자 소유의 모든 OUSD는 하나 이상의 지원되는 스테이블 코인과 교환됩니다. 스테이블코인 수령량은 **환율**\(**exchange rate\)**에 따라 다릅니다.

### 리베이스/rebase\(\) <a id="rebase"></a>

**`function rebase()`**‌

금고\(Valut\)에 현재 저장된 자산의 값을 기준으로 모든 사용자의 잔액을 업데이트합니다. `uint256` 유형으로 표시되는 기본 자산 및 전략의 총 값을 반환합니다.‌

### 할당/allocate\(\) <a id="allocate"></a>

**`function allocate()`**‌

수율을 극대화하고 리스크를 다양화하기 위해 관리 대상 자산을 규정된 전략\([Stategies](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies)\) 으로 이동합니다.‌

### 총액가치/totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**‌

기본 자산 및 전략의 총 가치를 반환합니다.

| `return` 이 | 유형 | 설명 |
| :--- | :--- | :--- |
| 가치\(value\) | uint256 | 기본 자산 및 전략의 총 가치입니다. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | address | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_금액\(amount\) | uint256 | 소수 단위로 표시된 OUSD의 양입니다. |

| `return` 이 | 유형 | 설명 |
| :--- | :--- | :--- |
| 생산\(outputs\) | uint256\[\] | 스테이블코인 자산 상환 함수의 배열이 반환됩니다. |

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

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | 주소 | 스테이블 코인 주소 |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| symbol | string | 스테이블 코인 상 |

### USD 상환 가격/priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| symbol | string | 스테이블 코인 상 |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | 주소 | 스테이블 코인 주 |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | 주소 | 스테이블 코인 주소 |

