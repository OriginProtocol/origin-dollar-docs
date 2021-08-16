# Oracle Harga

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

Untuk membuat dan menebus sejumlah OUSD yang sesuai saat masuk dan keluar, kontrak pintar harus memberi harga yang akurat pada USDT, USDC, dan DAI yang masuk dan keluar dari sistem.

Sebagai tindakan pencegahan tambahan, OUSD tidak pernah membayar lebih dari satu dolar untuk stablecoin. Ini mencegah protokol diserang melalui oracle yang salah harga. Setiap keuntungan tambahan yang dikumpulkan sebagai hasil dari stablecoin yang terlepas dari pasaknya didistribusikan kembali ke pemegang OUSD yang tersisa dalam bentuk hasil tambahan.

Sebagai protokol terdesentralisasi, OUSD harus bergantung pada sumber non-sentralisasi untuk harga ini. OUSD menggunakan Chainlink sebagai oracle untuk DAI, USDC, dan USDT. Anda dapat membaca lebih lanjut tentang [keputusan kami untuk bekerja dengan Chainlink](https://blog.originprotocol.com/how-origin-uses-chainlink-oracles-to-secure-ousd-bff5601e840e) di blog kami. Berikut adalah oracle Chainlink yang saat ini kami gunakan:

{% embed url="https://data.chain.link/usdt-usd" %}

{% embed url="https://data.chain.link/usdc-usd" %}

{% embed url="https://data.chain.link/dai-usd" %}

Alamat kontrak pintar khusus untuk setiap oracle yang digunakan tercantum di halaman [registry](../smart-contracts/registry.md). Ada kemungkinan bahwa oracle tambahan akan ditambahkan ke protokol dari waktu ke waktu. Dukungan juga dapat dihapus jika salah satu dari oracle ini menjadi tidak dapat diandalkan.

