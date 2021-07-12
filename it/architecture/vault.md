# Vault

Il Vault è il cuore del protocollo. Il vaulta è il responsabile del conio/riscatto dei token OUSD, del ribilanciamento dei fondi tra le varie strategie supportate, e della liquidazione dei token di ricompensa.

Le più importanti funzioni richiamabili pubblicamente del Vault sono:

* `mint()`, che consente di convertire in OUSD una singola stablecoin supportata
* `mintMultiple()` che consente di convertire in OUSD più stablecoin supportate, facendo una singola chiamata
* `redeem()` che consente di riscattare una quantità specificata di OUSD in cambio di altre stablecoin supportate.
* ` redeemAll()` che consente all'utente di riscattare il suo intero saldo OUSD in cambio delle altre stablecoin supportate. Questo è particolarmente utile poiche i saldi degli utenti crescono costantemente al crescere del rendimento.
* `rebase()` che aggiorna i saldi di tutti gli utenti sulla base del valore degli asset custoditi in quel momento nella pool.
* ` allocate()` sposta gli asset sotto la gestione delle [Strategie](strategies.md) prescritte, per massimizzare il rendimento e diversificare il rischio.

Riguardo le redemption, non è l'utente che decide quale o quali stablecoin vengono restituite all'utente, ma è il protocollo stesso. Questa decisione su quale o quali coin vengono restituite, è basata sui cambi interni degli asset che sono custoditi all'interno del vault.



