# Katkı

**% 100 Açık kaynak**

OUSD tamamen açık kaynaklı bir projedir ve her türden katkıyı memnuniyetle karşılıyoruz. Sorunları bildirmekten, kodlara katkıda bulunmaktan ve topluluğumuzu geliştirmemize yardımcı olmaktan yardım etmenin birçok yolu vardır.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

We work in public and our company Discord is open to all. If you have questions or need help getting started, our [Discord OUSD channels](https://discord.gg/jyxpUSe) are the best place to get assistance from our team and community.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies. Various other developer tools can be found at [ousd.com/dashboard](https://ousd.com/dashboard).

#### Gelişme süreci

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. İlginç bir konu bulun ve iletişim kurun! Lütfen `#engineering` [Discord](https://discord.gg/jyxpUSe) kanalına ne üzerinde çalışmak istediğinizi bildirin.
2. Discord'da [çekirdek ekip üyesine](https://github.com/orgs/OriginProtocol/teams/core/members) üye ping atın ve [katılımcı ekibimize eklenmesini isteyin](https://github.com/orgs/OriginProtocol/teams/contributors). Aksi takdirde, ilgili depoyu çatallamanız ve özellik dallarını kendi çatalınıza itmeniz gerekir.
3. Soruna bir yorum ekleyin veya kendi kendinize atayın, böylece istemeden aynı görev üzerinde çalışan birden fazla katılımcımız olmasın.
4. `ana` dalıyla başlayın ve mevcut bir özelliğe katkıda bulunmadığınız sürece yeni bir özellik dalını kontrol edin.
5. Write some awesome code.
6. `ana` en son kaydetmeleri alın ve kodunuzun başladığınızdan beri birleştirilen diğer tüm çalışmalarda çalıştığını onaylayın.
7. Push your branch to the upstream repository (i.e. https://github.com/OriginProtocol/\[repo]) so that other contributors can easily work off of it if necessary.
8. Lütfen sağ sütundaki "İnceleyenler" in yanındaki dişli çark simgesini tıklayarak PR'da bir inceleme talep edin.

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Kodlama Stili

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io).

For Solidity, we use two-space indents.

#### Protokol Tasarımı

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature (RFCs, papers, etc)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Topluluk Rehberleri

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Sorunları Bildirme

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Güvenlik sorunları

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% content-ref url="../security-and-risks/bug-bounties.md" %}
[bug-bounties.md](../security-and-risks/bug-bounties.md)
{% endcontent-ref %}

#### **Topluluk İyileştirme**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `discussion` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Tam Zamanlı Pozisyonlar

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full-time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).

