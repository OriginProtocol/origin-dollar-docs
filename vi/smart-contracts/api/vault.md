---
description: >-
  Vault (kho tiền) là điểm cốt lõi của giao thức. Kho tiền chịu trách nhiệm khai tác / hoàn trả OUSD, cân bằng lại quỹ giữa các chiến lược được hỗ trợ khác nhau và thanh lý token thưởng.
---

# Vault

## Đơn vị

Tất cả OUSD được chuyển hoặc trả về theo phương thức Vault đều sử dụng 18 chữ số thập phân. Ví dụ: 1 OUSD được hiển thị 1000000000000000000.

Các đồng stablecoin khác nhau sẽ có số thập phân hiển thị khác nhau. DAI sử dụng 18 chữ số thập phân trong khi USDC và USDT chỉ sử dụng 6.

## Phương pháp‌

### mint () <a id="mint"></a>

**`function mint(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**‌

Mua OUSD để đổi lấy một khoản tiền gửi bằng `_mount` stablecoin nhất định được chỉ định bởi tham số `_asset`. Người gọi lệnh nhận được một lượng OUSD nhất định tùy thuộc vào **tỷ giá hối đoái**.

| Tên thông số          | Loại    | Mô tả                                                                                                                                              |
|:--------------------- |:------- |:-------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset             | địa chỉ | Địa chỉ của stablecoin [được hỗ trợ](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)  |
| \_amount            | uint256 | Số tiền gửi, được biểu thị bằng đơn vị thập phân                                                                                                   |
| \_minimumOusdAmount | uint256 | Số OUSD tối thiểu mà người gọi lệnh chấp nhận. Lệnh gọi mua\(\) sẽ được trả lại nếu số lượng tạo ra ít hơn số lượng mà người gọi lệnh chấp nhận. |

### mintMultiple () <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts, uint256 _minimumOusdAmount)`**‌

Mint OUSD để đổi lấy một khoản tiền gửi chứa nhiều stablecoin trong 1 lần gọi lệnh. Stablecoin được chỉ định bởi tham số `_assets` và số tiền bằng tham số `_amounts`. Người gọi lệnh nhận được một lượng OUSD nhất định tùy thuộc vào **tỷ giá hối đoái**.

| Tên thông số          | Loại       | Mô tả                                                                                                                                              |
|:--------------------- |:---------- |:-------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets            | địa chỉ [] | Địa chỉ của [stablecoin được hỗ trợ](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets)  |
| \_amounts           | uint256 [] | Số tiền gửi, được biểu thị bằng đơn vị thập phân                                                                                                   |
| \_minimumOusdAmount | uint256    | Số OUSD tối thiểu mà người gọi lệnh chấp nhận. Lệnh gọi mua\(\) sẽ được trả lại nếu số lượng tạo ra ít hơn số lượng mà người gọi lệnh chấp nhận. |

{% hint style="warning" %}
Khi hoàn lại tiền, chính giao thức sẽ quyết định stablecoin nào sẽ được trả lại cho người dùng. Việc lựa chọn đồng coin nào sẽ được trả sẽ dựa trên tỷ lệ nội bộ của tài sản đang được giữ trong vault.‌
{% endhint %}

### redeem () <a id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD được chỉ định bởi thông số `_amount` được quy đổi để đổi lấy một hoặc nhiều stablecoin được hỗ trợ. Số lượng stablecoin nhận được phụ thuộc vào **tỷ giá hối đoái**.

| Tên thông số | Loại    | Mô tả                                |
|:------------ |:------- |:------------------------------------ |
| \_amount   | uint256 | lượng OUSD tính tới đơn vị thập phân |

### redeemAll ()‌ <a id="redeemall"></a>

**`function redeemAll()`**

Tất cả OUSD mà người dùng sở hữu đều được đổi lấy một hoặc nhiều stablecoin được hỗ trợ. Số lượng stablecoin nhận được phụ thuộc vào **tỷ giá hối đoái**.

### rebase () <a id="rebase"></a>

**`function rebase()`**‌

Cập nhật số dư cho tất cả người dùng dựa trên giá trị của tài sản hiện đang được lưu trữ trong vault. Trả về tổng giá trị của các tài sản đảm bảo và chiến lược cơ bản được đại diện bằng `uint256` loại.‌

### allocate () <a id="allocate"></a>

**`function allocate()`**‌

Di chuyển các tài sản thuộc quyền quản lý tới [các chiến lược](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) để tối đa hóa năng suất và đa dạng hoá rủi ro.

### totalValue () <a id="totalvalue"></a>

**`function totalValue()`**‌

Trả về tổng giá trị của các tài sản và chiến lược cơ bản.

| `return` Tên | Loại    | Mô tả                                                     |
|:------------ |:------- |:--------------------------------------------------------- |
| giá trị      | uint256 | trả về tổng giá trị của các tài sản và chiến lược cơ bản. |

### checkBalance () <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Trả về số dư của nội dung được chỉ định bởi tham số`_asset` được giữ trong Vault và tất cả các chiến lược được thể hiện bằng loại `uint256`.

| Tên thông số | Loại    | Mô tả                                                                                                                                             |
|:------------ |:------- |:------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin [được hỗ trợ](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) |

### calculateRedeemOutputs () <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Tính toán kết hợp các stablecoin mà chức năng `redeem` sẽ trả lại khi người dùng muốn rút 1 số lượng OUSD nhất định được chỉ định bởi thông số `_amount`. Trả về tổng hợp giá trị các stablecoin.

Để phân bổ các giá trị stablecoin cho từng loại stablecoin, lệnh gọi này nên được sử dụng cùng với hàm `getAllAssets` trả về 1 tổ hợp địa chỉ stablecoin.

Chỉ số được trả về bởi `calculateRedeemOutputs` tương ứng với địa chỉ stablecoin trả về bởi hàm `getAllAssets`.

| Tên thông số | Loại    | Mô tả                                |
|:------------ |:------- |:------------------------------------ |
| \_amount   | uint256 | lượng OUSD tính tới đơn vị thập phân |

| `return` Tên | Loại       | Mô tả                                                   |
|:------------ |:---------- |:------------------------------------------------------- |
| đầu ra       | uint256 [] | mảng số lượng tài sản stablecoin mà hàm `redeem` trả về |

### getAssetCount () <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Trả về số lượng tài sản stablecoin hỗ trợ được đại diện bằng loại `uint256`.‌

### getAllAssets () <a id="getallassets"></a>

**`function getAllAssets()`**‌

Trả về địa chỉ tài sản hỗ trợ theo thứ tự được đại diện bằng loại `uint256`.‌

### getStrategyCount () <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Trả về số lượng chiến lược đang được sử dụng trong Vault đại điện bằng loại `uint256`.‌

### getAPR () <a id="getapr"></a>

**`function getAPR()`**‌

Trả về tổng lợi nhuận phần trăm hàng năm (APR) của Vault và tất cả các Chiến lược được đại diện bằng loại `uint256`. Kết quả là số có 18 ký tự.‌

### isSupportedAsset (\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Trả về kết quả boolean true nếu nội dung được chỉ định bởi tham số `_asset` được Vault hỗ trợ.

| Tên thông số | Loại    | Mô tả                  |
|:------------ |:------- |:---------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin |

### priceUSDMint () <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Trả về giá tỷ giá hối đoái của đồng xu ổn định được chỉ định bởi các tham số `symbol` được sử dụng trả lại OUSD được đại diện bằng `uint256`. Số kết quả có 18 ký tự.

| Tên thông số | Loại  | Mô tả                  |
|:------------ |:----- |:---------------------- |
| ký hiệu      | chuỗi | Địa chỉ của stablecoin |

### priceUSDRedeem () <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

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
