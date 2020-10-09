---
description: >-
  금고(vault) 는 프로토콜의 핵심입니다. 금고는 OUSD 토큰의 채굴 / 교환, 다양한 지원 전략 간의 자금 재조정, 보상 토큰 청산을
  담당합니다.
---

# 금고\(Vault\)

## 방법

### 발행/mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**

`_asset` 매개변수로 지정된 일정 `_amount` 의 스테이블 코인을 예치하는 대가로 OUSD를 채굴합니다. 통화자는 **환율\(exchange rate\)**에 따라 일정 금액의 OUSD를 받습니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | address | 지원되는\([supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)\) 스테이블 코인 주 |
| \_amount | uint256 | 입금된 금액은 소수 단위로 표시 |

### 다중발행/mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**‌

한 번의 통화로 여러 개의 스테이블 코인을 예약하는 보상으로 OUSD를 발행합니다. 스테이블 코인 `assets` 어레이 매게 변수와 `amounts` 어레이 매게 변수에 의해 지정됩니다. 통화자는 **환율\(exchange rate\)**에 따라 일정 금액의 OUSD를 받게 됩니다. 

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_assets | address | 지원되는\([supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)\) 스테이블 코인 주소 |
| \_amounts | uint256 | 입금된 금액은 소수 단위로 표시 |

{% hint style="warning" %}
재할당 시 사용자에게 반환되는 스테이블 코인을 결정하는 것은 프로토콜이 아니라 사용자입니다. 이러한 코인 반환 결정은 금고에 보관 중인 자산의 내부 비율을 기반으로 합니다.‌
{% endhint %}

### 상환/redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

`_amount`매개변수로 지정된 OUSD는 하나 이상의 지원되는 스테이블 코인에 대한 교환으로 사용됩니다. 스테이블코인 수령량은 **환율\(exchange rate\)**에 따라 다릅니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_amount | uint256 | OUSD 금액은 소수 단위로 표시  |

### 전액 상환/redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**‌

사용자 소유의 모든 OUSD는 하나 이상의 지원되는 스테이블 코인과 교환됩니다. 스테이블코인 수령량은 **환율**\(**exchange rate\)**에 따라 다릅니다.

### 리베이스/rebase\(\) <a id="rebase"></a>

**`function rebase()`**‌

금고\(Valut\)에 현재 저장된 자산의 값을 기준으로 모든 사용자의 잔액을 업데이트합니다. `uint256` 유형으로 표시되는 기본 자산 및 전략의 총 값을 반환합니다.‌

### 할당/allocate\(\) <a id="allocate"></a>

**`function allocate()`**‌

수율을 극대화하고 리스크를 다양화하기 위해 관리 대상 자산을 규정된 전략\([Stategies](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies)\) 으로 이동합니다.‌

### 총액 가치/totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**‌

기본 자산 및 전략의 총 가치를 반환합니다.

| `return` 이 | 유형 | 설명 |
| :--- | :--- | :--- |
| 가치\(value\) | uint256 | 기본 자산 및 전략의 총 가치입니다. |

### 잔액 체크/checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

금고\(Vault\)에 저장된`_asset`매개 변수로 지정된 자산과 `uint256` 유형으로 표시되는 모든 전략의 균형을 반환합니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | address | 지원되는\([supported](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)\) 스테이블 코인 주소 |

### 상환 결과 계산/calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

`_amount` 매개변수로 지정된 일정량의 OUSD를 상환할 때 `redeem`함수가 반환할 스테이블 코인을 혼합하여 계산합니다. 스테이블 코인 값의 배열을 반환합니다.

스테이블코인 값을 올바른 스테이블코인 통화로 지정하려면 이 호출을 스테이블코인 주소 배열을 반환하는`getAllAssets` 기능과 함께 사용해야 합니다.

`calculateRedeemOutputs`에서 반환되는 배열의 인덱스입니다.출력은 `getAllAssets`함수에 의해 반환되는 배열에서 동일한 인덱스를 가진 스테이블 코인 주소에 해당합니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_금액\(amount\) | uint256 | 소수 단위로 표시된 OUSD의 양입니다. |

| `return` 이 | 유형 | 설명 |
| :--- | :--- | :--- |
| 생산\(outputs\) | uint256 | 스테이블코인 자산 상환 함수의 배열이 반환됩니다. |

### 자산 얻/getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

`uint256` 유형으로 표시된 지원되는 스테이블코인 자산 수를 반환합니다.‌

### 자산 전액 얻기/getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

지원되는 스테이블코인 자산의 모든 자산 주소를 `uint256` 유형으로 표시된 순서대로 반환합니다.‌

### 전략 수 얻기/getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

`uint256` 유형으로 표시된 금고\(Vault\)에서 활성 전략 수를 반환합니다.‌

### 총 연간 수익률 얻기/getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**‌

금고\(Vault\)의 총 연간 수익률\(APR\)과 `uint256`유형으로 표시된 모든 전략을 반환합니다. 결과 숫자는 소수점 18개를 가집니다.‌

### 지원 자산/isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

 `_asset` 매개 변수로 지정된 자산이 금고\(Vault\)에서 지원되는 경우 True인 부분을 반환합니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | 주소 | 스테이블 코인 주소 |

### USD 발행 가/priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

`uint256`유형으로 표시된 OUSD를 채굴할 때 사용되는 `symbol` 파라미터로 지정된 스테이블 코인의 환율 가격을 반환합니다. 결과 숫자는 소수점 18개를 가집니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| symbol | string | 스테이블 코인 상 |

### USD 상환 가격/priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

`uint256` 유형으로 표시된 OUSD를 상환할 때 사용되는 `symbol` 파라미터로 지정된 스테이블 코인의 환율 가격을 반환합니다. 결과 숫자는 소수점 18개를 가집니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| symbol | string | 스테이블 코인 상 |

### 자산 USD 발행 가격/priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

`uint256` 유형으로 표시된 OUSD를 채굴할 때 사용되는 `_asset`  매개변수로 지정된 스테이블 코인의 환율 가격을 반환합니다. 결과 숫자는 소수점 18개를 가집니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | 주소 | 스테이블 코인 주 |

### 자산 USD 상환 가격/priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

`uint256`유형으로 표시된 OUSD를 상환할 때 사용되는 `_asset` 매개변수로 지정된 스테이블 코인의 환율 가격을 반환합니다. 결과 숫자는 소수점 18개를 가집니다.

| 매개 변수 이름 | 유형 | 설명 |
| :--- | :--- | :--- |
| \_asset | 주소 | 스테이블 코인 주소 |

