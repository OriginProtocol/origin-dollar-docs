# Contribuire

**100% Open source**

OUSD è un progetto interamente open source e accogliamo con piacere contributi di ogni tipo. Ci sono molti modi per aiutare, segnalando problemi, contribuendo allo sviluppo di codice, e aiutandoci a migliorare la nostra community.

Noi lavoriamo pubblicamente e la nostra azienda è su Discord ed è aperta a tutti. Se hai domande o hai bisogno di aiuto per iniziare, i nostri canali OUSD su Discord sono il posto migliore per ricevere assistenza dal nostro team e dalla nostra community.

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

Il branch `master` è bloccato in modo tale che solo i membri del [core team](https://github.com/orgs/OriginProtocol/teams/core) possano essere in grado di fare il merge delle tue pull requests. Le pull request che vengono sottoposte alla revisione da altri collaboratori verificati, saranno accelerate e mergiate più velocemente! Controlla nel canale Discord `#engineering` per revisori appropriati.

#### Stile del codice

Nei nostri repository noi usiamo svariati linguaggi di programmazione. Se contribuisci, segui le convenzioni già esistenti e fai riferimento al file CONTRIBUTING.md nel repository stesso, se esiste.

Per JavaScript, utilizziamo [lo stile NPM](https://docs.npmjs.com/misc/coding-style), che viene applicato automaticamente via [ prettier](https://prettier.io/).

Per Solidity, utiliziamo l'indentazione con due spazi.

#### Progettazione del Protocollo

A proposito delle proposte di progettazione di protocollo o di implementazione, ci aspettiamo:

* Una descrizione del problema che questa proposta risolverebbe
* Discussione dei trade-off coinvolti
* Revisione delle altre soluzioni esistenti
* Link alla letteratura pertinente \ (RFC, documenti, ecc \)
* Discussione della soluzione proposta

Si noti che la progettazione del protocollo è un lavoro duro e meticoloso. Potresti aver bisogno di rivedere la letteratura esistente e riflettere su casi d'uso generalizzati.

#### Linee guida della community

Vogliamo mantenere la community di Origin fantastica, in crescita e collaborativa. Abbiamo bisogno del tuo aiuto per mantenerla così. Per aiutare in questo, abbiamo elaborato alcune linee guida generali per la community nel suo insieme:

* Sii gentile: sii cortese, rispettoso ed educato con gli altri membri della community: non saranno tollerati insulti su area geografica, raziali, di genere o di altra natura. Ci piacciono le brave persone molto più di quelle cattive!
* Incoraggia la diversità e la partecipazione: fai sentire tutti i benvenuti nella nostra community, indipendentemente dal loro background e dalla quantità dei loro contributi, e fai il possibile per incoraggiare la partecipazione nella nostra community.
* Mantienila legale: non mettere nessuno nei guai. Condividi solo i contenuti di tua proprietà, non condividere informazioni private o sensibili e non infrangere le leggi.
* Rimani in tema: assicurati di pubblicare sul canale corretto ed evita discussioni fuori tema. Ricorda che quando aggiorni un problema o rispondi a un'e-mai, stai potenzialmente interagendo con un gran numero di persone. Quindi per favore considera questo prima di fare l'aggiornamento. Ricorda anche che a nessuno piace lo spam.

#### Segnalazione di problemi

Se trovi bug, errori o incongruenze nel codice o nei documenti di Origin, faccelo sapere segnalando un problema su GitHub. Nessun problema è troppo piccolo. Aiutaci a sistemare anche erori di batitura!

#### Problemi di sicurezza

OUSD è ancora in fase di sviluppo iniziale, il che significa che potrebbero esserci problemi con il protocollo o nelle nostre implementazioni. Prendiamo molto seriamente le vulnerabilità sulla sicurezza. Se dovessi scoprire un problema di sicurezza, ti preghiamo di portarlo subito alla nostra attenzione!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **Community Improvement**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Full-Time Positions

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



