# Resiko

{% hint style="danger" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

Seperti halnya instrumen berbunga lainnya. Ada resiko terkait dengan memegang OUSD yang penting untuk dipahami. Risiko-risiko ini secara luas dapat diklasifikasikan menjadi 3 kategori:

* Risiko kontrak pintar
* Risiko platform yang mendasari
* Risiko stablecoin yang mendasari

**Risiko kontrak pintar**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Risiko platform**

OUSD dibangun di atas platform DeFi lain yang menambah risiko kontrak pintar tambahan. Kami memilih untuk bekerja dengan platform yang memiliki aset ratusan juta dolar di bawah manajemen dan telah melakukan upaya yang wajar untuk memastikan kebenaran protokol mereka. Namun, tidak ada jaminan bahwa platform yang mendasarinya akan terus berfungsi sebagaimana mestinya, dan kegagalan dalam strategi yang mendasarinya kemungkinan besar akan menyebabkan hilangnya dana bagi para pemegang OUSD.

**Risiko Stablecoin**

Penting untuk dipahami bahwa OUSD hanya sekuat stablecoin yang mendukungnya. Setiap kerugian aset yang mendasarinya akan menyebabkan kerugian yang serupa dengan nilai OUSD.

Penting untuk dicatat bahwa setiap stablecoin yang didukung ini menimbulkan risiko pihak lawan yang tidak sepele. Tether, khususnya, memiliki masalah perbankan yang terdokumentasi dengan baik dan tantangan regulasi. Selain itu, baik USDT dan USDC memiliki pintu belakang yang memberikan kuasa kepada penerbitnya untuk membekukan uang di dompet pemegangnya. Meskipun DAI tidak memiliki pintu belakang langsung, asetnya juga dapat terkena dampak negatif karena USDC diterima sebagai jaminan untuk pembuatan DAI.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







