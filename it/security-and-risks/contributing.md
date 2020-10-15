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

Se dovessi trovare una vulnerabilità legata alla sicurezza, per favore invia la tua segnalazione privatamente a [security@originprotocol.com](mailto:security@originprotocol.com) or invia un messaggio criptato a [@joshfraser su Keybase](https://keybase.io/joshfraser). Per favore NON presentare il problema in modo pubblico. Assicurati di rivedere le nostre linee guida per la divulgazione responsabile e per la tua eligibilità nella bug bounty.

{% page-ref page="bug-bounties.md" %}

#### **Miglioramento della community**

In Origin la community è tanto importante quanto la tecnologia.

Abbiamo costante bisogno di migliorare la nostra documentazione, sviluppare nuovi tools per interfacciarci con la nostra piattaforma, spargere la voce a nuovi utenti, aiutare i nuovi utenti a prepararsi e molto altro ancora.

Per favore mettiti in contatto con noi se hai il desiderio di aiutare. Per i volontari, il nostro canale `general` su [Discord](https://www.originprotocol.com/discord) è un ottimo posto di condivisione di idee e per aiutare.

#### Posizioni lavorative a tempo pieno

Origin occasionalmente assume sviluppatori per posizioni part-time o full-time.

Quando assumiamo, diamo preferenza a coloro che hanno già iniziato a contribuire al progetto. Se desideri una posizione a tempo pieno all'interno del nostro team, la soluzione migliore è impegnarti con il nostro team e iniziare a contribuire scrivendo codice. E' improbabile che ti offriamo posizioni full-time all'interno del nostro team di ingegneri, a meno che tu non abbia già mergiato qualche pull.

Se sei interessato, controlla [gli elenchi di lavoro di Origin Protocol](https://angel.co/originprotocol/jobs). Se desideri aiutare in altri modi, proponi le tue idee nel [nostro canale Discord](https://www.originprotocol.com/discord).



