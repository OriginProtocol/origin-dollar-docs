---
description: >-
  Vault là điểm cốt lõi của giao thức. Kho tiền chịu trách nhiệm khai tác / hoàn trả OUSD, cân bằng lại quỹ giữa các chiến lược được hỗ trợ khác nhau và thanh lý token thưởng.
---

# Vault

## Phương pháp‌

### mint () <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**

Khai thác OUSD để đổi lấy một khoản tiền gửi bằng `_mount` nhất định của stablecoin được chỉ định bởi tham số `_asset`. Người gọi lệnh nhận được một lượng OUSD nhất định tùy thuộc vào **tỷ giá hối đoái**.

| Tên thông số | Loại    | Mô tả                                                                                                                                             |
|:------------ |:------- |:------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin [được hỗ trợ](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) |
| \_amount   | uint256 | Số tiền gửi, được biểu thị bằng đơn vị thập phân                                                                                                  |

### mintMultiple () <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**

Khai thác OUSD để đổi lấy một khoản tiền gửi chứa nhiều stablecoin trong lần gọi lệnh. Stablecoin được chỉ định bởi tham số mảng `_assets` và số tiền bằng tham số mảng `_amounts`. Người gọi lệnh nhận được một lượng OUSD nhất định tùy thuộc vào **tỷ giá hối đoái**.

| Tên thông số | Loại       | Mô tả                                                                                                                                             |
|:------------ |:---------- |:------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets   | địa chỉ [] | Địa chỉ của [stablecoin được hỗ trợ](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) |
| \_amounts  | uint256 [] | Số tiền gửi, được biểu thị bằng đơn vị thập phân                                                                                                  |

{% hint style="warning" %}
Khi hoàn lại tiền, chính giao thức sẽ quyết định stablecoin nào sẽ được trả lại cho người dùng. Việc lựa chọn đồng coin nào sẽ được trả sẽ dựa trên tỷ lệ nội bộ của tài sản đang được giữ trong vault.‌
{% endhint %}

### redeem () <a id="redeem"></a>

**`function redeem(uint256 _amount)`**

OUSD được chỉ định bởi thông số `_amount` được quy đổi để đổi lấy một hoặc nhiều stablecoin được hỗ trợ. Số lượng stablecoin nhận được phụ thuộc vào **tỷ giá hối đoái**.

| Tên thông số | Loại    | Mô tả                                |
|:------------ |:------- |:------------------------------------ |
| \_amount   | uint256 | lượng OUSD tính tới đơn vị thập phân |

### redeemAll ()‌ <a id="redeemall"></a>

**`function redeemAll()`**

Tất cả OUSD mà người dùng sở hữu đều được đổi lấy một hoặc nhiều stablecoin được hỗ trợ. Số lượng stablecoin nhận được phụ thuộc vào **tỷ giá hối đoái**.

### rebase () <a id="rebase"></a>

**`function rebase()`**

Cập nhật số dư cho tất cả người dùng dựa trên giá trị của tài sản hiện đang được lưu trữ trong vault. Trả về tổng giá trị của các tài sản đảm bảo và chiến lược cơ bản được đại diện bằng `uint256` loại.‌

### allocate () <a id="allocate"></a>

**`function allocate()`**

Di chuyển các tài sản thuộc quyền quản lý tới [các chiến lược](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) để tối đa hóa năng suất và đa dạng hoá rủi ro

### totalValue () <a id="totalvalue"></a>

**`function totalValue()`**

Trả về tổng giá trị của các tài sản và chiến lược cơ bản.

| `return` Tên | Loại    | Mô tả                                                     |
|:------------ |:------- |:--------------------------------------------------------- |
| giá trị      | uint256 | trả về tổng giá trị của các tài sản và chiến lược cơ bản. |

### checkBalance () <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Returns the balance of an asset specified by the`_asset` parameter held in Vault and all strategies represented by `uint256` type.

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

### priceUSDRedeem () <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**

Trả về giá tỷ giá hối đoái của đồng xu ổn định được chỉ định bởi các tham số `symbol` được sử dụng khi quy đổi OUSD được đại diện bằng `uint256`. Số kết quả có 18 ký tự.

| Tên thông số | Loại  | Mô tả                  |
|:------------ |:----- |:---------------------- |
| ký hiệu      | chuỗi | Địa chỉ của stablecoin |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Trả về tỷ giá hối đoái của stablecoin được chỉ định bởi các tham số `_asset` được sử dụng khi khai thác OUSD được đại diện bằng loại `uint256`. Số kết quả có 18 ký tự.

| Tên thông số | Loại    | Mô tả                   |
|:------------ |:------- |:----------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin‌ |

### priceAssetUSDRedeem ()‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Trả về tỷ giá hối đoái của stablecoin được chỉ định bởi các tham số `_asset` được sử dụng khi đổi OUSD được đại diện bằng loại `uint256`. Số kết quả có 18 ký tự.

| Tên thông số | Loại    | Mô tả                  |
|:------------ |:------- |:---------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin |

