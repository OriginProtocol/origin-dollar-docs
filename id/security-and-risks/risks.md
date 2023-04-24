# Resiko

{% hint style="danger" %}
Gunakan dengan resiko Anda sendiri. Jangan menggunakan modal lebih dari yang Anda rela kehilangan.
{% endhint %}

Seperti halnya produk DeFi yang menghasilkan hasil, ada risiko terkait dengan memegang OUSD yang penting untuk dipahami. Risiko-risiko ini secara luas dapat diklasifikasikan menjadi 3 kategori:

* Risiko kontrak pintar OUSD
* Risiko platform pihak ketiga yang mendasari
* Risiko stablecoin yang mendasari

**Risiko kontrak pintar OUSD**

Kontrak cerdas kami telah [diaudit](audits.md) oleh beberapa perusahaan keamanan yang dihormati. Kontrak pintar kami belum diaudit, dan bahkan dengan audit formal, masih mungkin terjadi kesalahan logika yang akan menyebabkan hilangnya dana bagi para pemegang OUSD. Kontrak melibatkan matematika dan logika yang kompleks. Meskipun kami telah mengambil setiap tindakan pencegahan untuk memastikan keselamatan dan keamanan kontrak pintar kami, pengguna diingatkan untuk menggunakan dengan risiko mereka sendiri. Origin Protocol tidak akan bertanggung jawab atas hilangnya dana, terlepas dari siapa yang bersalah.

**Risiko platform pihak ketiga**

OUSD dibangun di atas platform DeFi lainnya seperti Aave, Compound, dan Curve yang menambahkan risiko kontrak pintar tambahan. We are choosing to work with platforms that have literally billions of dollars of assets under management and have made a reasonable efforts to ensure the security of their protocols. Namun, tidak ada jaminan bahwa platform yang mendasarinya akan terus berfungsi sebagaimana mestinya, dan kegagalan dalam strategi yang mendasarinya kemungkinan besar akan menyebabkan hilangnya dana bagi para pemegang OUSD.

**Risiko Stablecoin**

Penting untuk dipahami bahwa OUSD hanya sekuat stablecoin yang mendukungnya. Any loss of value to an underlying stablecoin asset will cause a similar loss to the value of OUSD. While OUSD is designed to maintain a 1:1 relationship between supply and number of backing stablecoins, it does not guarantee which stablecoins will make up that backing nor the value of those coins.

Penting untuk dicatat bahwa setiap stablecoin yang didukung ini menimbulkan risiko pihak lawan yang tidak sepele. Tether, khususnya, memiliki masalah perbankan yang terdokumentasi dengan baik dan tantangan regulasi. Selain itu, baik USDT dan USDC memiliki pintu belakang yang memberikan kuasa kepada penerbitnya untuk membekukan uang di dompet pemegangnya. While DAI does not have any direct backdoors, its assets can also be negatively impacted since USDC and USDT are accepted as collateral for minting DAI.

**Risk mitigation**

While it's impossible to guarantee our contracts are 100% safe, we have taken every step possible to mitigate the chance of losing funds:

We regularly have our work [audited ](audits.md)by the top auditors in the industry.

[DeFi insurance](insurance.md) is availble  to offer smart contract coverage as an optional add-on service for OUSD holders.

We have retained [Certora](https://www.certora.com) to formally verify the various security properties of our contracts. They helped us establish automated verifications that will run anytime we update our contract code. We have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are incredibly rigorous. We require at least two engineers to review each change with a detailed checklist and we prioritize security reviews over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contracts' source code ourselves. We've observed that attackers often exploit the same fundamental vulnerability on multiple different projects. By reviewing other project's vulnerabilities, we force ourselves to stay up to date on the latest security threats in our industry and are constantly learning from their mistakes.

**Actions speak louder than words**

You should also know that many members of the Origin team, including both founders, are holding a significant portion of their personal wealth in OUSD. Origin Protocol's corporate treasury is also holding millions of dollars in OUSD. We have skin in the game and are willing to put our own money at risk with the code we have written.

