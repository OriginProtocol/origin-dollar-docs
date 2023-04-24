# Contribuire

**100% Open source**

OUSD è un progetto interamente open source e accogliamo con piacere contributi di ogni tipo. Ci sono molti modi per aiutare, segnalando problemi, contribuendo allo sviluppo di codice, e aiutandoci a migliorare la nostra community.

Noi lavoriamo pubblicamente e la nostra azienda è su Discord ed è aperta a tutti. Se hai domande o hai bisogno di aiuto per iniziare, i nostri canali OUSD su Discord sono il posto migliore per ricevere assistenza dal nostro team e dalla nostra community.

**Analytics per sviluppatori**

La nostra dashboard interna per sviluppatori è disponibile all'URL [analytics.ousd.com](https://analytics.ousd.com). La nostra dashboard mostra l'attuale offerta circolante, gli asset gestiti all'interno del vault e le attuali allocazioni tra ogni stablecoin e le strategie.

#### Processo di sviluppo

La nostra strategia di branching è simile a quella di [ GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), ma noi sviluppiamo completamente nel branch `master` e utilizziamo il branch `stable` per il codice che viene rilasciato.

Il tuo flusso di sviluppo dovrebbe assomigliare a:

1. Trova un problema interessante e comunicalo! Informa il canale `#engineering` su [Discord](https://discord.gg/jyxpUSe) su ciò cui tu vuoi lavorare.
2. Informa un membro del [core team](https://github.com/orgs/OriginProtocol/teams/core/members) su Discord e chiedigli di essere aggiunto al nostro [contributors team](https://github.com/orgs/OriginProtocol/teams/contributors). Altrimenti, avrai bisogno di forkare il repository pertinente e pushare i branch di riferimento al tuo fork personale.
3. Aggiungi un commento al problema o autoassegnatelo in modo tale da non avere più collaboratori che lavorano sulla stessa attività senza saperlo.
4. Inizia con il branch `master` e fai check out di un nuovo feature branch a meno che tu non stia contribuendo già ad una feature esistente.
5. Segui lo [stile di codice](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) già esistente e scrivi codice magnifico.
6. Fai pull degli ultimi commit dal `master`, e assicurati che il tuo codice funzioni dopo aver fatto il merge.
7. Pusha il tuo branch sull'upstream repository \(i.e. https://github.com/OriginProtocol/\[repo\]\) in modo tale che gli altri collaboratori possano lavorarci facilmente, se necessario.
8. Richiedi una revisione nel PR cliccando sull'icona con l'ingranaggio vicino alla scritta "Reviewers" nella colonna di destra.

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Stile del codice

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### Progettazione del Protocollo

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature \(RFCs, papers, etc\)
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

{% page-ref page="bug-bounties.md" %}

#### **Miglioramento della community**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Posizioni lavorative a tempo pieno

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



