# Oracoli di Prezzo

OUSD è progettato per rimanere ancorato ad 1 USD e può essere supportato 1:1 con le sue stablecoin sottostanti. Questo è più complicato di quanto sembri perché queste stablecoin sottostanti si discostano costantemente dall'ancoraggio desiderato di 1 USD. Sebbene la maggior parte delle fluttuazioni giornalieri sono irrilevanti, ci sono state in passato oscillazioni di prezzo di grande importanza e si potrebbero verificare nuovamente anche in futuro.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Coin</th>
      <th style="text-align:left"><b>Low</b>
      </th>
      <th style="text-align:left"><b>High</b>
      </th>
      <th style="text-align:left"><b>Delta</b>
      </th>
      <th style="text-align:left"><b>Fonte</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0.929222</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.11</p>
        <p>15/10/2018</p>
      </td>
      <td style="text-align:left">$0.180778</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/usd-coin/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDC</td>
      <td style="text-align:left">
        <p>$0.924188</p>
        <p>02/08/2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.17</p>
        <p>08/05/2019</p>
      </td>
      <td style="text-align:left">$0.245812</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/usd-coin">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.945505</p>
        <p>10/05/2020</p>
      </td>
      <td style="text-align:left">
        <p>$1.11</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">$0.164495</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/multi-collateral-dai/">CoinMarketCap</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DAI</td>
      <td style="text-align:left">
        <p>$0.903243</p>
        <p>25/11/2019</p>
      </td>
      <td style="text-align:left">
        <p>$1.22</p>
        <p>13/03/2020</p>
      </td>
      <td style="text-align:left">$0.316757</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/dai">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.849809</p>
        <p>02/02/2017</p>
      </td>
      <td style="text-align:left">
        <p>$1.21</p>
        <p>27/05/2017</p>
      </td>
      <td style="text-align:left">$0.360191</td>
      <td style="text-align:left"><a href="https://www.coingecko.com/en/coins/tether">CoinGecko</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">USDT</td>
      <td style="text-align:left">
        <p>$0.572521</p>
        <p>02/03/2015</p>
      </td>
      <td style="text-align:left">
        <p>$1.32</p>
        <p>24/07/2018</p>
      </td>
      <td style="text-align:left">$0.747479</td>
      <td style="text-align:left"><a href="https://coinmarketcap.com/currencies/tether/">CoinMarketCap</a>
      </td>
    </tr>
  </tbody>
</table>

La funzione di ribasamento tratta 1 stablecoin come fosse 1 OUSD per semplicità e per proteggere il saldo OUSD dalle fluttuazioni del prezzo delle stablecoin sottostanti. Poiché la funzione di rebase conta solo le monete, il saldo OUSD dovrebbe solo crescere.

Per coniare e riscuotere l'appropriato numero di OUSD in entrata e uscita, gli smart contract hanno bisogno di prezzare accuratamente gli USDT, USDC e DAI che entrano ed escono dal sistema. In qualità di protocollo decentralizzato, OUSD deve riferirsi a sorgenti non centralizzate per questi prezzi.

{% hint style="info" %}
OUSD recupera il prezzo da molteplici oracoli on-chain e utilizza i tassi di cambio che sono più vantaggiosi per il vault al momento della coniazione o del riscatto.
{% endhint %}

Al fine di prevenire attacchi malevoli e per incoraggiare investitori di lungo periodo invece di speculatori di breve periodo, lo smart contract OUSD confronta i feed di prezzo da molteplici fonti e utilizzerà il tasso di cambio a vantaggio dell'intero vault rispetto al singolo. Questo meccanismo protegge i fondi della pool dagli arbitraggi e impedisce a qualsiasi individuo di essere in grado di trarre vantaggio da eventuali inefficienze temporanee causate da errori di prezzo provenienti dagli oracoli, per depredare gli asset dal vault condiviso.

Ciò protegge i fondi nel vault e allo stesso tempo premia gli holder di lungo termine. Poiché il prezzo più sicuro dipende dalla direzione del trade, lo smart contract dell'oracolo Origin espone sia la funzione `priceUSDMint()`, sia la funzione ` priceUSDRedeem()`.

OUSD uses Chainlink as oracle for DAI, USDC and USDT.

{% embed url="https://feeds.chain.link/eth-usd" caption="" %}

The specific smart contract address for each oracle being used are listed on our [registry](../../smart-contracts/registry.md) page.

It is possible that additional oracles will be added to the protocol over time. Support may also be removed if any of these oracles become unreliable.

