# Ước tính giá

OUSD được thiết kế để duy trì ở mức 1 USD và được hỗ trợ 1:1 bằng các stablecoin. Trên thực tế, việc duy trì tỉ lệ này phức tạp hơn nhiều vì giá của các stablecoin thường sẽ chênh lệch so với mức 1$. Thường thì những biến động trên khá nhỏ, tuy nhiên, không ngoại trừ trường hợp có thể có biến động lớn xảy ra như đã từng gặp trong quá khứ.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Coin</th>
      <th style="text-align:left"><b>Th&#x1EA5;p</b>
      </th>
      <th style="text-align:left"><b>Cao</b>
      </th>
      <th style="text-align:left"><b>Ch&#xEA;nh l&#x1EC7;ch</b>
      </th>
      <th style="text-align:left"><b>Ngu&#x1ED3;n</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>0,929222$</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">
        <p>1,11$</p>
        <p>15/10/2018</p>
      </td>
      <td style="text-align:left">0,180778$</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>0,924188$</p>
        <p>02/08/2020</p>
      </td>
      <td style="text-align:left">
        <p>1,17$</p>
        <p>08/05/2019</p>
      </td>
      <td style="text-align:left">0,245812$</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>0,945505$</p>
        <p>10/05/2020</p>
      </td>
      <td style="text-align:left">
        <p>1,11$</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">0,164495$</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>0,903243$</p>
        <p>25/11/2019</p>
      </td>
      <td style="text-align:left">
        <p>1,22$</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">0,316757$</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>0,849809$</p>
        <p>02/02/2017</p>
      </td>
      <td style="text-align:left">
        <p>1,21$</p>
        <p>27/05/2017</p>
      </td>
      <td style="text-align:left">0,360191$</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>0,572521$</p>
        <p>02/03/2015</p>
      </td>
      <td style="text-align:left">
        <p>1,32$</p>
        <p>24/07/2018</p>
      </td>
      <td style="text-align:left">0,747479$</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

Để tạo mới và đốt số lượng OUSD thích hợp, các hợp đồng thông minh cần định giá chính xác USDT, USDC và DAI đang được nạp vào và rút ra khỏi hệ thống. Ousd cũng cần có cơ chế tăng nguồn cung tin cậy tương xứng phần lãi kiếm được hoặc giảm cung nếu tài sản đảm bảo \(các stablecoin nạp vào\) giảm. Là một giao thức phi tập trung, OUSD phải dựa vào các nguồn phi tập trung để xác định các mức giá.

{% hint style="info" %}
Giá của OUSD được đối chiếu trên nhiều chuỗi và sử dụng tỉ giá có lợi nhất cho bể.
{% endhint %}

Để ngăn chặn các cuộc tấn công và khuyến khích các nhà đầu tư dài hạn thay vì các nhà đầu cơ ngắn hạn, hợp đồng OUSD so sánh các nguồn cấp giá từ nhiều nguồn và sẽ sử dụng tỷ giá hối đoái nào có lợi cho toàn bộ tài sản có trong bể. Cơ chế này bảo vệ quỹ của bể khỏi tình trạng kinh doanh ăn chênh lệch giá và ngăn chặn cá nhân lợi dụng bất kỳ sơ hở tạm thời nào gây ảnh hưởng tới tài sản trong bể.

Điều này bảo vệ các khoản tiền được giữ trong bể đồng thời khuyến khích mọi người nắm giữ lâu dài. Mức giá an toàn nhất phụ thuộc vào giao dịch mua bán trực tiếp, mức giá của Origin đối chiếu cả `priceUSDMint ()` và `priceUSDRedeem ()`. Chức năng nguồn cung linh hoạt sử dụng `priceUSDMint ()` để đảm bảo tính nhất quán.

Đây là tập hợp các oracle ban đầu đang được OUSD sử dụng:

{% embed url="https://compound.finance/docs/prices" caption="" %}

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

Các oracle sau đã được thử nhiệm nhưng không đưa vào sử dụng do tốn quá nhiều phí gas:

{% embed url="https://uniswap.org/docs/v2/core-concepts/oracles/" caption="" %}

{% tabs %}
{% tab title="DAI/USD" %}
Các oracle sau được sử dụng để tìm nạp hoặc tính giá cho **DAI/USD:**

| Oracle | Cặp | Hợp đồng |
| :--- | :--- | :--- |
| Nguồn giá mở | DAI/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink | DAI/USD | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0 |
| Chainlink | DAI/ETH | 0x037E8F2125bF532F3e228991e051c8A7253B642c |
| _Uniswap_ | _DAI/ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title="USDT/USD" %}
Các oracle sau được sử dụng để tìm nạp hoặc tính giá cho **USDT/USD:**

| O**racle** | Cặp | Hợp đồng |
| :--- | :--- | :--- |
| Chainlink | USDT/ETH | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE |
| Nguồn giá mở | USDC/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| _Uniswap v2_ | _USDT/ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title="USDC/USD" %}
Các oracle sau được sử dụng để tìm nạp hoặc tính giá cho **ETH/USD:**

| O**racle** | Cặp | Hợp đồng |
| :--- | :--- | :--- |
| Chainlink | USDC/ETH | 0xdE54467873c3BCAA76421061036053e371721708 |
| Nguồn giá mở | USDC/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| _Uniswap v2_ | _USDC/ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title="ETH/USD" %}
Vì không phải tất cả các oracles đều có các cặp USD trực tiếp, giao thức cũng lấy giá **ETH/USD** để tính giá USD bằng ETH. Một lần nữa, để đảm bảo tính an toàn, giao thức ưu tiên cho bể hơn là cho cá nhân.

| Oracle | Cặp | Hợp đồng |
| :--- | :--- | :--- |
| Nguồn giá mở | ETH/USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink | ETH/USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

Việc có các oracle mới bổ sung vào giao thức theo thời gian là hoàn toàn có thể. Các oracle hiện đang hỗ trợ cũng có thể bị loại bỏ nếu phị phát hiện thiếu tin cậy.

