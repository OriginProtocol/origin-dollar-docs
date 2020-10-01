# Fiyat Oracle'ları

OUSD, 1 USD'de sabit kalacak ve temelindeki stabilcoinlerle 1: 1 desteklenecek şekilde tasarlanmıştır. Bu, göründüğünden daha zor çünkü bu temel sabit paralar, sürekli olarak kendi istenen 1 USD sabitlerinden sapıyor. Günlük dalgalanmaların çoğu küçük olsa da, geçmişte meydana gelen ve gelecekte tekrar ortaya çıkması muhtemel olan büyük fiyat dalgalanmaları olmuştur.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Coin</th>
      <th style="text-align:left"><b>Düşük</b>
      </th>
      <th style="text-align:left"><b>Yüksek</b>
      </th>
      <th style="text-align:left"><b>Delta</b>
      </th>
      <th style="text-align:left"><b>Kaynak</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0,929222 </p>
        <p>13 Mart 2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.11
</p>
        <p>15 Ekim 2018</p>
      </td>
      <td style="text-align:left">$0.180778
</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap
</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0.924188</p>
        <p>02 Ağu 2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.17
</p>
        <p>08 Mayıs 2019</p>
      </td>
      <td style="text-align:left">$0.245812
</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.945505
</p>
        <p>10 Mayıs 2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.11
</p>
        <p>13 Mart 2020</p>
      </td>
      <td style="text-align:left">$0.164495
</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap
</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p> $0.903243
</p>
        <p>Kasım 25, 2019</p>
      </td>
      <td style="text-align:left">
        <p>$1.22</p>
        <p>13 Mart 2020</p>
      </td>
      <td style="text-align:left">$0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.849809</p>
        <p>02 Şubat 2017</p>
      </td>
      <td style="text-align:left">
        <p>$1.21</p>
        <p>27 Mayıs 2017</p>
      </td>
      <td style="text-align:left">$0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.572521</p>
        <p>02 Mart 2015</p>
      </td>
      <td style="text-align:left">
        <p>$1.32</p>
        <p>24 Temmuz 2018</p>
      </td>
      <td style="text-align:left">$0.747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap
</a>
      </td>
    </tr>
  </tbody>
</table>

Giriş ve çıkışta uygun sayıda OUSD basmak ve yakmak için, akıllı sözleşmelerin sisteme giren ve çıkan USDT, USDC ve DAI'yi doğru bir şekilde fiyatlandırması gerekir. Ayrıca, kazanılan faizi dağıtmak için arzı genişletmenin güvenilir bir yoluna ya da temel varlıkların değerinde olumsuz bir değişiklik varsa arzı daraltmaya ihtiyaç duyar. Merkezi olmayan bir protokol olarak, OUSD bu fiyatlar için merkezi olmayan kaynaklara güvenmek zorundadır.

{% hint style="bilgi" %}
OUSD, fiyatı birden fazla zincir üzerindeki oracle'dan alır ve havuz için en avantajlı olan döviz kurunu kullanır.
{% endhint %}

Kötü niyetli saldırıları önlemek ve uzun vadeli yatırımcıları kısa vadeli spekülatörler üzerinden teşvik etmek için, OUSD sözleşmesi, birden fazla kaynaktan gelen fiyat beslemelerini karşılaştırır ve hangi döviz kurunun bireye göre tüm havuza fayda sağladığını kullanır. Bu mekanizma, havuzun fonlarını arbitrajcılardan korur ve herhangi bir bireyin, paylaşılan varlık havuzunu tüketmek için yanlış fiyatlandırılmış oracle'ların neden olduğu herhangi bir geçici verimsizlikten yararlanmasını engeller.

Bu, uzun vadeli sahiplerini ödüllendirirken havuzdaki fonları korur. En güvenli fiyat ticaretin yönüne bağlı olduğundan, Origin oracle hem `fiyatUSDMint ()` hem de `fiyatUSDRedeem ()`ortaya çıkarır. Yeniden ödeme işlevi tutarlılık için `priceUSDMint ()` kullanır.

İşte OUSD tarafından kullanılan ilk oracle dizisi:

{% embed url = "https://compound.finance/docs/prices" caption = ""%}

{% embed url = "https://feeds.chain.link/eth-usd" caption = ""%}

Aşağıdaki oracle'lar uygulandı, ancak şu anda gaz maliyetleri nedeniyle kullanılmıyor:

{% embed url = "https://uniswap.org/docs/v2/core-concepts/oracles" caption = ""%}

{% tabs %}
{% tab title = "DAI / USD"%}
Aşağıdaki oracle'lar **DAI / USD fiyatını almak veya hesaplamak için kullanılır:**

| Oracle          | Per       | Kontrakt                                     |
|:--------------- |:--------- |:-------------------------------------------- |
| Açık fiyat Feed | DAI/USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| Chainlink       | DAI/USD   | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0   |
| Chainlink       | DAI/ETH   | 0x037E8F2125bF532F3e228991e051c8A7253B642c   |
| _Uniswap v2_    | _DAI/ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title="USDT/USD" %}
Aşağıdaki oracle'lar **DAI / USD fiyatını almak veya hesaplamak için kullanılır:**

| Oracle          | Per        | Kontrakt                                     |
|:--------------- |:---------- |:-------------------------------------------- |
| Chainlink       | USDT/ETH   | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE   |
| Open Price Feed | USDC/USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| _Uniswap v2_    | _USDT/ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title="USDT/USD" %}
Aşağıdaki oracle'lar **DAI / USD fiyatını almak veya hesaplamak için kullanılır:**

| Oracle          | Per        | Kontrakt                                     |
|:--------------- |:---------- |:-------------------------------------------- |
| Chainlink       | USDT/ETH   | 0xdE54467873c3BCAA76421061036053e371721708   |
| Açık fiyat Feed | USDC/USD   | 0xc629c26dced4277419cde234012f8160a0278a79   |
| _Uniswap v2_    | _USDC/ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title = "DAI / USD"%}
Tüm oracle'ların doğrudan USD çiftleri olmadığından, protokol ayrıca ETH kullanarak USD fiyatlarını hesaplamak için **ETH / USD** fiyatlarını da getirir. Yine güvende olmak için protokol, birey yerine fon için en avantajlı olanı seçer.

| Oracle          | Per       | Kontrakt                                   |
|:--------------- |:--------- |:------------------------------------------ |
| Açık fiyat Feed | ETH / USD | 0xc629c26dced4277419cde234012f8160a0278a79 |
| Chainlink       | ETH / USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

Zamanla protokole ek stabilcoinlerin eklenmesi mümkündür. Bu oracle'lardan herhangi biri güvenilmez hale gelirse destek de kaldırılabilir.

