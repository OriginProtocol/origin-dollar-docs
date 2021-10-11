# Contribuire

**100% Open source**

OUSD è un progetto interamente open source e accogliamo con piacere contributi di ogni tipo. Ci sono molti modi per aiutare, segnalando problemi, contribuendo allo sviluppo di codice, e aiutandoci a migliorare la nostra community.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

We work in public and our company Discord is open to all. If you have questions or need help getting started, our [Discord OUSD channels](https://discord.gg/jyxpUSe) are the best place to get assistance from our team and community.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies. Various other developer tools can be found at [ousd.com/dashboard](https://ousd.com/dashboard).

#### Processo di sviluppo

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. Trova un problema interessante e comunicalo! Informa il canale `#engineering` su [Discord](https://discord.gg/jyxpUSe) su ciò cui tu vuoi lavorare.
2. Informa un membro del [core team](https://github.com/orgs/OriginProtocol/teams/core/members) su Discord e chiedigli di essere aggiunto al nostro [contributors team](https://github.com/orgs/OriginProtocol/teams/contributors). Altrimenti, avrai bisogno di forkare il repository pertinente e pushare i branch di riferimento al tuo fork personale.
3. Aggiungi un commento al problema o autoassegnatelo in modo tale da non avere più collaboratori che lavorano sulla stessa attività senza saperlo.
4. Inizia con il branch `master` e fai check out di un nuovo feature branch a meno che tu non stia contribuendo già ad una feature esistente.
5. Write some awesome code.
6. Fai pull degli ultimi commit dal `master`, e assicurati che il tuo codice funzioni dopo aver fatto il merge.
7. Push your branch to the upstream repository (i.e. https://github.com/OriginProtocol/\[repo]) so that other contributors can easily work off of it if necessary.
8. Richiedi una revisione nel PR cliccando sull'icona con l'ingranaggio vicino alla scritta "Reviewers" nella colonna di destra.

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Stile del codice

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io).

For Solidity, we use two-space indents.

#### Progettazione del Protocollo

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature (RFCs, papers, etc)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Linee guida della community

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Segnalazione di problemi

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Problemi di sicurezza

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% content-ref url="../security-and-risks/bug-bounties.md" %}
[bug-bounties.md](../security-and-risks/bug-bounties.md)
{% endcontent-ref %}

#### **Miglioramento della community**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `discussion` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Posizioni lavorative a tempo pieno

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full-time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).

