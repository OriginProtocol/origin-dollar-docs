# Ước tính giá

OUSD được thiết kế để duy trì ở mức 1 USD và được hỗ trợ 1:1 bằng các stablecoin. Trên thực tế, việc duy trì tỉ lệ này phức tạp hơn nhiều vì giá của các stablecoin thường sẽ chênh lệch so với mức 1$. Thường thì những biến động trên khá nhỏ, tuy nhiên, không ngoại trừ trường hợp có thể có biến động lớn xảy ra như đã từng gặp trong quá khứ.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Coin</th>
      <th style="text-align:left"><b>Thấp</b>
      </th>
      <th style="text-align:left"><b>Cao</b>
      </th>
      <th style="text-align:left"><b>Chênh lệch</b>
      </th>
      <th style="text-align:left"><b>Nguồn</b>
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

Chức năng rebase coi 1 stablecoin là 1 OUSD để đơn giản hóa và để bảo vệ số dư OUSD khỏi bị ảnh hưởng bởi những biến động hàng ngày về giá của các stablecoin cơ bản. Vì chức năng rebase chỉ tính số đồng, số dư OUSD chỉ nên tăng lên.

Để mint và redeem số lượng OUSD thích hợp, các hợp đồng thông minh cần định giá chính xác USDT, USDC và DAI đang được nạp vào và rút ra khỏi hệ thống. Là một giao thức phi tập trung, OUSD phải dựa vào các nguồn phi tập trung để xác định các mức giá.

{% hint style="info" %}
Giá của OUSD được đối chiếu trên nhiều chuỗi và sử dụng tỉ giá có lợi nhất cho kho tiền khi mint hoặc redeem.
{% endhint %}

Để ngăn chặn các cuộc tấn công và khuyến khích các nhà đầu tư dài hạn thay vì các nhà đầu cơ ngắn hạn, hợp đồng OUSD so sánh các nguồn cấp giá từ nhiều nguồn và sẽ sử dụng tỷ giá hối đoái nào có lợi cho toàn bộ tài sản có trong kho tiền. Cơ chế này bảo vệ quỹ của bể khỏi tình trạng kinh doanh ăn chênh lệch giá và ngăn chặn cá nhân lợi dụng bất kỳ sơ hở tạm thời nào gây ảnh hưởng tới tài sản trong kho tiền.

Điều này bảo vệ các khoản tiền được giữ trong kho tiền đồng thời khuyến khích mọi người nắm giữ lâu dài. Mức giá an toàn nhất phụ thuộc vào giao dịch mua bán trực tiếp, mức giá của Origin đối chiếu cả `priceUSDMint ()` và `priceUSDRedeem ()`.

OUSD sử dụng oracle Chainlink cho DAI, USDC và USDT.

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

Địa chỉ hợp đồng thông minh cụ thể cho mỗi oracle đang được sử dụng được liệt kê tại [trang đăng ký](../../smart-contracts/registry.md).

Việc có các oracle mới bổ sung vào giao thức theo thời gian là hoàn toàn có thể. Các oracle hiện đang hỗ trợ cũng có thể bị loại bỏ nếu phị phát hiện thiếu tin cậy.

