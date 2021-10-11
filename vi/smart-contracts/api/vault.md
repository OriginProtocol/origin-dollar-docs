---
description: >-
  Vault (kho tiền) là điểm cốt lõi của giao thức. Kho tiền chịu trách nhiệm khai tác / hoàn trả OUSD, cân bằng lại quỹ giữa các chiến lược được hỗ trợ khác nhau và thanh lý token thưởng.
---

# Vault

## Đơn vị

Tất cả OUSD được chuyển hoặc trả về theo phương thức Vault đều sử dụng 18 chữ số thập phân. Ví dụ: 1 OUSD được hiển thị 1000000000000000000.

Các đồng stablecoin khác nhau sẽ có số thập phân hiển thị khác nhau. DAI sử dụng 18 chữ số thập phân trong khi USDC và USDT chỉ sử dụng 6.

Các nỗ lực [đang được thực hiện](https://github.com/OriginProtocol/origin-dollar/issues/590) để tăng tính chính xác của các phép tính từ 18 số thập phân lên 27 số thập phân. Bản thân token OUSD sẽ vẫn giữ độ chính xác 18 số thập phân và số dư của người dùng sẽ không thay đổi.

## Phương pháp‌

### mint() <a href="mint" id="mint"></a>

**`function mint(address _asset, uint256 _amount, uint256 _minimumOusdAmount)`**‌

Khai thác OUSD từ một khoản tiền gửi bằng `_mount` nhất định của stablecoin được chỉ định bởi tham số `_asset`. Người gọi lệnh nhận được một lượng OUSD nhất định tùy thuộc vào **tỷ giá hối đoái**.

| Tên thông số          | Loại    | Mô tả                                                                                                                                                |
| --------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset             | địa chỉ | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |
| \_amount            | uint256 | Số tiền gửi, được biểu thị bằng đơn vị thập phân                                                                                                     |
| \_minimumOusdAmount | uint256 | Số OUSD tối thiểu mà người gọi lệnh chấp nhận. The call to mint() reverts if the minimum is not met.                                                 |

### mintMultiple() <a href="mintmultiple" id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts, uint256 _minimumOusdAmount)`**‌

Mint OUSD để đổi lấy một khoản tiền gửi chứa nhiều stablecoin trong 1 lần gọi lệnh. Stablecoin được chỉ định bởi tham số mảng `_assets` và số tiền bằng tham số mảng `_amounts`. Người gọi lệnh nhận được một lượng OUSD nhất định tùy thuộc vào **tỷ giá hối đoái**.

| Tên thông số          | Loại        | Mô tả                                                                                                                                                   |
| --------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets            | address\[] | Addresses of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoins |
| \_amounts           | uint256\[] | Số tiền gửi, được biểu thị bằng đơn vị thập phân                                                                                                        |
| \_minimumOusdAmount | uint256     | Số OUSD tối thiểu mà người gọi lệnh chấp nhận. The call to mint() reverts if the minimum is not met.                                                    |

{% hint style="warning" %}
On redemptions, it is the protocol and not the user that decides which stablecoin(s) are returned to the user. This decision of which coin(s) to return is based on the internal ratios of the assets that are being held in the vault.‌
{% endhint %}

### redeem() <a href="redeem" id="redeem"></a>

**`function redeem(uint256 _amount)`**‌

OUSD được chỉ định bởi thông số `_amount` được quy đổi để đổi lấy một hoặc nhiều stablecoin được hỗ trợ. Số lượng stablecoin nhận được phụ thuộc vào **tỷ giá hối đoái**.

| Tên thông số | Loại    | Mô tả                                |
| ------------ | ------- | ------------------------------------ |
| \_amount   | uint256 | lượng OUSD tính tới đơn vị thập phân |

### redeemAll()‌ <a href="redeemall" id="redeemall"></a>

**`function redeemAll()`**‌

Tất cả OUSD mà người dùng sở hữu đều được đổi lấy một hoặc nhiều stablecoin được hỗ trợ. Số lượng stablecoin nhận được phụ thuộc vào **tỷ giá hối đoái**.

### rebase() <a href="rebase" id="rebase"></a>

**`function rebase()`**‌

Cập nhật số dư cho tất cả người dùng dựa trên giá trị của tài sản hiện đang được lưu trữ trong vault. Trả về tổng giá trị của các tài sản đảm bảo và chiến lược cơ bản được đại diện bằng `uint256` loại.‌

### allocate() <a href="allocate" id="allocate"></a>

**`function allocate()`**‌

Moves the assets under management into their prescribed [Stategies](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies) to maximize yield and diversify risk.‌

### totalValue() <a href="totalvalue" id="totalvalue"></a>

**`function totalValue()`**‌

Trả về tổng giá trị của các tài sản và chiến lược cơ bản.

| `return` Tên | Loại    | Mô tả                                                     |
| ------------ | ------- | --------------------------------------------------------- |
| giá trị      | uint256 | trả về tổng giá trị của các tài sản và chiến lược cơ bản. |

### checkBalance() <a href="checkbalance" id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Trả về số dư của nội dung được chỉ định bởi tham số`_asset` được giữ trong Vault và tất cả các chiến lược được thể hiện bằng loại `uint256`.

| Tên thông số | Loại    | Mô tả                                                                                                                                                |
| ------------ | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset    | địa chỉ | Address of the [supported](https://app.gitbook.com/@originprotocol/s/ousd/\~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) stablecoin |

### calculateRedeemOutputs() <a href="calculateredeemoutputs" id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Tính toán kết hợp các stablecoin mà chức năng `redeem` sẽ trả lại khi người dùng muốn rút 1 số lượng OUSD nhất định được chỉ định bởi thông số `_amount`. Trả về tổng hợp giá trị các stablecoin.

Để phân bổ các giá trị stablecoin cho đúng đơn vị tiền tệ stablecoin, lệnh gọi này nên được sử dụng cùng với hàm `getAllAssets` để trả về một mảng địa chỉ stablecoin.

Chỉ số của một mảng được trả về bởi `calculateRedeemOutputs` tương ứng với địa chỉ stablecoin với chỉ số tương tự trong một mảng trả về bởi hàm `getAllAssets`.

| Tên thông số | Loại    | Mô tả                                |
| ------------ | ------- | ------------------------------------ |
| \_amount   | uint256 | lượng OUSD tính tới đơn vị thập phân |

| `return` Tên | Loại        | Mô tả                                                   |
| ------------ | ----------- | ------------------------------------------------------- |
| đầu ra       | uint256\[] | mảng số lượng tài sản stablecoin mà hàm `redeem` trả về |

### getAssetCount() <a href="getassetcount" id="getassetcount"></a>

**`function getAssetCount()`**‌

Trả về số lượng tài sản stablecoin được hỗ trợ được biểu thị bằng loại `uint256`.‌

### getAllAssets() <a href="getallassets" id="getallassets"></a>

**`function getAllAssets()`**‌

Trả về địa chỉ tài sản được hỗ trợ được theo thứ tự được biểu thị bằng loại `uint256`.‌

### getStrategyCount()‌ <a href="getstrategycount" id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Trả về số lượng chiến lược đang được sử dụng trong Vault biểu thị bằng loại `uint256`.‌

### getAPR() <a href="getapr" id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield (APR) of the Vault and all Strategies represented by `uint256` type. Kết quả là số có 18 ký tự.‌

### isSupportedAsset() <a href="issupportedasset" id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Trả về kết quả boolean true nếu nội dung được chỉ định bởi tham số `_asset` được Vault hỗ trợ.

| Tên thông số | Loại    | Mô tả                  |
| ------------ | ------- | ---------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin |

### priceUSDMint() <a href="issupportedasset-1" id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Trả về giá tỷ giá hối đoái của đồng stablecoin được chỉ định bởi các tham số `symbol` được sử dụng khi mint OUSD được đại diện bởi `uint256`. Kết quả là số có 18 ký tự.

| Tên thông số | Loại  | Mô tả                  |
| ------------ | ----- | ---------------------- |
| ký hiệu      | chuỗi | Địa chỉ của stablecoin |

### priceUSDRedeem() <a href="issupportedasset-2" id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Trả về tỷ giá hối đoái của stablecoin được chỉ định bởi các tham số `_asset` sử dụng khi đổi OUSD sang stablecoin khác được đại diện bằng loại `uint256`. Kết quả là số có 18 ký tự.

| Tên thông số | Loại  | Mô tả                  |
| ------------ | ----- | ---------------------- |
| ký hiệu      | chuỗi | Địa chỉ của stablecoin |

### priceAssetUSDMint()‌ <a href="issupportedasset-3" id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Trả về tỷ giá hối đoái của stablecoin được chỉ định bởi các tham số `_asset` được sử dụng khi khai thác OUSD được đại diện bằng loại `uint256`. Kết quả là số có 18 ký tự.

| Tên thông số | Loại    | Mô tả                   |
| ------------ | ------- | ----------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin‌ |

### priceAssetUSDRedeem()‌ <a href="issupportedasset-3-1" id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Trả về tỷ giá hối đoái của stablecoin được chỉ định bởi các tham số `_asset` sử dụng khi đổi OUSD sang stablecoin khác được đại diện bằng loại `uint256`. Kết quả là số có 18 ký tự.

| Tên thông số | Loại    | Mô tả                  |
| ------------ | ------- | ---------------------- |
| \_asset    | địa chỉ | Địa chỉ của stablecoin |
