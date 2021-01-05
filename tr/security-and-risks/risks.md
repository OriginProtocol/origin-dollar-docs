# Riskler

{% hint style="tehlike" %}
Use at your own risk. Do not deploy more capital than you are willing to lose.
{% endhint %}

Faiz getiren herhangi bir enstrümanda olduğu gibi. OUSD tutmanın anlaşılması önemli olan ilişkili riskler vardır. Bu riskler genel olarak 3 kategoriye ayrılabilir:

* Akıllı sözleşme riski
* Temel platform riski
* Stabilcoin riskinin altında yatan

**Akıllı sözleşme riski**

Our smart contracts have been [audited](audits.md) by multiple, well-respected security firms. However, it is important to note that even with formal audits, it is still possible for there to be logic errors that could lead to the loss of funds for OUSD holders. The contracts involve complex math and logic that may or may not be correct. Origin Protocol will not be held responsible for any loss of funds, regardless of who is at fault.

**Platform riski**

OUSD, ek akıllı sözleşme riski ekleyen diğer DeFi platformlarının üzerine inşa edilmiştir. Yüz milyonlarca dolarlık varlığın yönetildiği ve protokollerinin doğruluğunu sağlamak için makul bir çaba gösteren platformlarla çalışmayı seçiyoruz. Ancak, temel platformların amaçlandığı gibi çalışmaya devam edeceğine dair hiçbir garanti yoktur ve temelde yatan bir stratejideki herhangi bir başarısızlık, muhtemelen OUSD sahipleri için fon kaybına yol açacaktır.

**Stablecoin riskleri**

OUSD'nin yalnızca onu destekleyen stabilcoinler kadar güçlü olduğunu anlamak önemlidir. Dayanak varlıklardaki herhangi bir kayıp, OUSD değerinde benzer bir kayba neden olacaktır.

Tüm bu stablecoin'lerin önemsiz olmayan karşı taraf riski oluşturduğuna dikkat etmek önemlidir. Özellikle Tether, iyi belgelenmiş bankacılık sorunları ve yasal zorluklar yaşadı. Ek olarak, hem USDT hem de USDC, ihraççılarına sahiplerinin cüzdanlarında para dondurma yetkisi veren arka kapılara sahiptir. DAI'nin herhangi bir doğrudan arka kapısı bulunmamakla birlikte, USDC'nin DAI basımı için teminat olarak kabul edilmesi nedeniyle varlıkları da olumsuz etkilenebilir.

_**In summary, OUSD is beta software. Use at your own risk. Do not deploy more capital than you are willing to lose.**_

**Risk Mitigation**

We are actively working with multiple DeFi insurance providers and will soon be announcing our initial coverage plans to further secure the protocol. Despite our plan to offer insurance coverage and our recent [audits](audits.md), we have taken extensive measures to improve our internal processes so that we do everything possible to avoid an exploit.

We have retained [Certora](https://www.certora.com/) to begin formally verifying the various security properties of our contracts. They will help us establish automated verifications that will run anytime we update our contract code. We now also have automated checking for common errors with [Slither](https://github.com/crytic/slither) and [Echidna](https://github.com/crytic/echidna) tests. Together, these alert our team to common security issues in addition to our own test suite.

Code reviews involving our smart contracts are now more rigorous than before. We require two engineers to review each change with a detailed checklist and we prioritize this over new feature development.

Finally, we have formalized an engineering [rotation](https://github.com/OriginProtocol/security/blob/master/incidents/ROTATION.md) for reviewing [attacks on other projects](https://github.com/OriginProtocol/security/tree/master/incidents) as well as ensuring we deep dive into each of these reviews, including reviewing the affected contract’s source code ourselves.







