# Mulai

Dokumen ini dimaksudkan untuk menjelaskan cara kerja OUSD, mengkomunikasikan potensi risiko dan manfaat, dan memberikan panduan bagi pengembang yang ingin berkontribusi pada basis kode kami atau mengintegrasikan OUSD ke dalam produk mereka. Berikut ini beberapa cara bagi Anda untuk menyelami dan memulai.

**Mint atau Redeem**

OUSD Mint memungkinkan siapa saja untuk membuat atau memperdagangkan token OUSD menggunakan [DApp](www.ousd.com) dan dompet cryptocurrency yang mendukung web-3 seperti [Metamask](https://www.metamask.io). Ini adalah cara asli untuk mendapatkan OUSD, terutama jika Anda menginginkan jumlah besar yang dapat berisiko menggerakkan pasar di bursa lain.

**Beli di Bursa**

Untuk jumlah kecil, cara termudah untuk mulai mendapatkan penghasilan dengan OUSD adalah dengan membelinya di bursa terdesentralisasi. Kami mengantisipasi bahwa OUSD akan segera tersedia secara luas di bursa yang terdesentralisasi dan terpusat.

Bursa Terdesentralisasi:

* [Beli OUSD di 1inch](https://app.1inch.io/#/1/swap/USDT/OUSD)
* [Beli OUSD di Curve Swaps](https://crv.to/) \([alternatif UI](https://crv.finance/)\)
* [Beli OUSD di Uniswap v3](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86)
* [Beli OUSD di Uniswap v2](https://app.uniswap.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86&use=v2)
* [Beli OUSD di Sushiswap](https://exchange.sushiswapclassic.org/#/swap?inputCurrency=0xdac17f958d2ee523a2206206994597c13d831ec7&outputCurrency=0x2a8e1e676ec238d8a992307b495b45b3feaa5e86)

Bursa Terpusat:

* Beli OUSD di KuCoin
  * [OUSD/USDT](https://trade.kucoin.com/OUSD-USDT)
  * [OUSD/BTC](https://trade.kucoin.com/OUSD-BTC)
* Beli OUSD di Virgox
  * [OUSD/USDT](https://virgox.com/exchange/141)
* [Beli OUSD di Aplikasi Dharma](https://www.dharma.io/) \(Khusus AS\)

**Menambahkan OUSD ke Dompet Anda**

{% hint style="success" %}
Alamat utama ERC20 untuk Origin Dollar \(OUSD\) adalah:   
**0x2A8e1E676Ec238d8A992307B495b45B3fEAa5e86**
{% endhint %}

Jika OUSD Anda tidak muncul secara otomatis di dompet Anda, Anda dapat menambahkannya secara manual menggunakan alamat di atas. Jika Anda berencana untuk [menyimpan OUSD Anda di dompet multi-sig](core-concepts/elastic-supply/rebasing-and-smart-contracts.md), pastikan untuk memilih untuk menerima hasil. Kami ingin OUSD didukung oleh sebanyak mungkin dompet dan dimasukkan ke dalam semua daftar token terkenal. Kami sangat menghargai bantuan yang dapat Anda tawarkan di bidang ini.

**Mengintegrasikan OUSD**

OUSD adalah token ERC-20 non-standar yang memerlukan integrasi kustom untuk sebagian besar aplikasi yang ingin mendukungnya. Secara khusus, penting bagi pengembang untuk memahami cara kerja pasokan elastis kami karena hal ini dapat dengan mudah menyebabkan perilaku yang tidak terduga.

Jika Anda adalah penyedia dompet atau bursa kripto yang tertarik untuk mendukung OUSD, silakan lihat panduan berikut ini:

{% page-ref page="core-concepts/elastic-supply/rebasing-and-smart-contracts.md" %}

{% page-ref page = "smart-contract / architecture.md"%}

{% page-ref page = "smart-contract / api /"%}

**Analisis Pengembang**

Dasbor pengembang internal kami tersedia di [analytics.ousd.com](https://analytics.ousd.com). Dasbor menunjukkan pasokan yang beredar saat ini, aset yang dikelola di vault, dan alokasi saat ini antara masing-masing stablecoin dan strategi.

**Mendapatkan bantuan**

Silakan bergabung dengan ruang Origin Dollar \ #engineering di server [Discord](www.originprotocol.com/discord) Origin.  Tim kami dan anggota komunitas kami berharap dapat membantu Anda membangun. Pertanyaan Anda membantu kami dalam peningkatan, jadi jangan ragu untuk bertanya jika Anda tidak dapat menemukan apa yang Anda cari di sini.

