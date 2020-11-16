# Harga Oracles

OUSD dirancang untuk tetap dipatok pada 1 USD dan didukung 1: 1 dengan stablecoin yang mendasarinya. Ini lebih rumit daripada kedengarannya karena stablecoin yang mendasari ini terus-menerus menyimpang dari pasak 1 USD yang mereka inginkan. Meskipun sebagian besar fluktuasi harian kecil, ada perubahan besar dalam harga yang telah terjadi di masa lalu dan kemungkinan besar akan terjadi lagi di masa mendatang.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Koin</th>
      <th style="text-align:left"><b>Rendah</b>
      </th>
      <th style="text-align:left"><b>Tinggi</b>
      </th>
      <th style="text-align:left"><b>Delta</b>
      </th>
      <th style="text-align:left"><b>Sumber</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0,929222</p>
        <p>13 Maret 2020</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,11</p>
        <p>15 Oktober 2018</p>
      </td>
      <td style="text-align:left">$ 0,180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$ 0,924188</p>
        <p>02 Agu 2020</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,17</p>
        <p>08 Mei 2019</p>
      </td>
      <td style="text-align:left">$ 0,245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$ 0,945505</p>
        <p>10 Mei 2020</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,11</p>
        <p>13 Maret 2020</p>
      </td>
      <td style="text-align:left">$ 0,164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$ 0,903243</p>
        <p>25 November 2019</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,22</p>
        <p>13 Maret 2020</p>
      </td>
      <td style="text-align:left">$ 0,316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0,849809</p>
        <p>02 Feb 2017</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,21</p>
        <p>27 Mei 2017</p>
      </td>
      <td style="text-align:left">$ 0,360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$ 0,572521</p>
        <p>02 Maret 2015</p>
      </td>
      <td style="text-align:left">
        <p>$ 1,32</p>
        <p>24 Juli 2018</p>
      </td>
      <td style="text-align:left">$ 0,747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

Fungsi rebasing memperlakukan 1 stablecoin sebagai 1 OUSD untuk kesederhanaan dan untuk melindungi saldo OUSD agar tidak terpengaruh oleh fluktuasi harian harga stablecoin yang mendasarinya. Karena fungsi rebase hanya menghitung koin, saldo OUSD seharusnya hanya bertambah.

Untuk membuat dan menebus sejumlah OUSD yang sesuai saat masuk dan keluar, kontrak pintar harus memberi harga yang akurat pada USDT, USDC, dan DAI yang masuk dan keluar dari sistem. Sebagai protokol terdesentralisasi, OUSD harus bergantung pada sumber non-sentralisasi untuk harga ini.

{% hint style="info" %}
OUSD fetches the price from multiple on-chain oracles and uses the exchange rate that is most advantageous for the vault when minting or redeeming.
{% endhint %}

In order to prevent malicious attacks and to encourage long-term investors over short-term speculators, the OUSD contract compares price feeds from multiple sources and will use whichever exchange rate benefits the entire vault over the individual. This mechanism protects the vault funds from arbitrageurs and prevents any individual from being able to take advantage of any temporary inefficiencies caused by mispriced oracles to deplete the shared pool of assets.

This protects the funds in the vault while rewarding long-term holders. Karena harga paling aman tergantung pada arah perdagangan, oracle Origin menghadapkan kedua `priceUSDMint ()` dan `priceUSDRedeem ()`.

Berikut adalah set oracle awal yang digunakan oleh OUSD:

{% embed url = "https://compound.finance/docs/prices" caption = ""%}

{% embed url = "https://feeds.chain.link/eth-usd" caption = ""%}

Oracle berikut telah diterapkan, tetapi saat ini tidak digunakan karena biaya gas:

{% embed url = "https://uniswap.org/docs/v2/core-concepts/oracles" caption = ""%}

{% tabs %}
{% tab title = "USDT / USD"%}
Oracle berikut digunakan untuk mengambil atau menghitung harga **DAI / USD:**

| Oracle           | Pasangan    | Kontrak                                      |
|:---------------- |:----------- |:-------------------------------------------- |
| Buka Umpan Harga | DAI / USD   | 0x922018674c12a7f0d394ebeef9b58f186cde13c1   |
| Chainlink        | DAI / USD   | 0xa7D38FBD325a6467894A13EeFD977aFE558bC1f0   |
| Chainlink        | DAI / ETH   | 0x037E8F2125bF532F3e228991e051c8A7253B642c   |
| _Uniswap v2_     | _DAI / ETH_ | _0xA478c2975Ab1Ea89e8196811F51A7B7Ade33eB11_ |
{% endtab %}

{% tab title = "USDT / USD"%}
Oracle berikut digunakan untuk mengambil atau menghitung harga **USDT / USD:**

| O**racle**       | Pasangan     | Kontrak                                      |
|:---------------- |:------------ |:-------------------------------------------- |
| Chainlink        | USDT / ETH   | 0xa874fe207DF445ff19E7482C746C4D3fD0CB9AcE   |
| Buka Umpan Harga | USDC / USD   | 0x922018674c12a7f0d394ebeef9b58f186cde13c1   |
| _Uniswap v2_     | _USDT / ETH_ | _0x0d4a11d5eeaac28ec3f61d100daf4d40471f1852_ |
{% endtab %}

{% tab title = "USDT / USD"%}
Oracle berikut digunakan untuk mengambil atau menghitung harga **USDC / USD:**

| O**racle**       | Pasangan     | Kontrak                                      |
|:---------------- |:------------ |:-------------------------------------------- |
| Chainlink        | USDC / ETH   | 0xdE54467873c3BCAA76421061036053e371721708   |
| Buka Umpan Harga | USDC / USD   | 0x922018674c12a7f0d394ebeef9b58f186cde13c1   |
| _Uniswap v2_     | _USDC / ETH_ | _0xb4e16d0168e52d35cacd2c6185b44281ec28c9dc_ |
{% endtab %}

{% tab title = "USDT / USD"%}
Karena tidak semua oracle memiliki pasangan USD langsung, protokol juga menetapkan harga untuk **ETH / USD** untuk menghitung harga USD menggunakan ETH. Sekali lagi, untuk amannya, protokol memilih dana yang paling menguntungkan daripada individu.

| Oracle           | Pasangan  | Kontrak                                    |
|:---------------- |:--------- |:------------------------------------------ |
| Buka Umpan Harga | ETH / USD | 0x922018674c12a7f0d394ebeef9b58f186cde13c1 |
| Chainlink        | ETH / USD | 0xF79D6aFBb6dA890132F9D7c355e3015f15F3406F |
{% endtab %}
{% endtabs %}

Ada kemungkinan bahwa oracle tambahan akan ditambahkan ke protokol dari waktu ke waktu. Dukungan juga dapat dihapus jika salah satu dari oracle ini menjadi tidak dapat diandalkan.

