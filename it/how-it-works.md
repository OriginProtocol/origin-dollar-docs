# Come Funziona

#### 100% garantito e stabile

Origin Dollar \(OUSD\) è un token conforme ERC-20 per la rete Ethereum.

OUSD è una stable coin che è garantita in proporzione 1:1 con altre stable coin come USDT, USDC e DAI. Di conseguenza, il valore di 1 OUSD dovrebbe esser sempre molto vicino a quello di 1 USD.

{% hint style="success" %}
1 OUSD = 1 USD
{% endhint %}

#### Coniare OUSD

Gli utenti convertono le loro stable coins \(attualmente USDT, USDC e DAI\) in OUSD tramite la [DApp Origin Dollar](www.ousd.com) ufficiale. Gli OUSD emessi cominciano immediatamente ad accumulare il rendimento composto.

**Riscattare OUSD**

Gli utenti possono riconvertire indietro in altre stablecoins i loro OUSD in qualsiasi momento utilizzando la [DApp Origin Dollar](www.ousd.com). Verrà applicata una commissione di uscita pari allo 0.5% e sarà distribuita come rendimento aggiuntivo per i partecipanti rimanenti al vault. The fee serves as a security feature to make it difficult for attackers to take advantage of lagging oracles, preventing them from siphoning stablecoins from the vault in the event of mispriced underlying assets. La commissione esiste per incentivare gli holders di lungo periodo contro gli speculatori di breve periodo.

Al momento del riscatto, lo smart contract determinrà quale o quali stablecoin restituirà all'utente. Nell'implementazione corrente, il vault restituirà le coin con la stessa proporzione di quelle che sono detenute al momento. Questa mancanza di opzioni, lato utente, protegge il vault nel caso in cui una delle qualsiasi stablecoin supportate dovesse perdere il suo ancoraggio al dollaro.

{% hint style="warning" %}
E' prevista una commissione di uscita dello **0.5%** è l'utente non può scegliere quale stablecoin riceverà.
{% endhint %}

#### **Automated Yield Farming**

OUSD generates yields by deploying the underlying stablecoins that were deposited to the OUSD smart contract to other DeFi protocols such as Compound, Aave, and Curve. There may be new diversified strategies added to the vault in the future. Gli interessi maturati, le commissioni di trading, e i token di ricompensa vengono raccolti e convertiti in stablecoin per produrre rendimenti in OUSD. Nel tempo, il protocollo sposterà assets dentro e fuori diversi pool di liquidità al fine di fornire il miglior rendimento ai detentori di OUSD.

#### **Elastic Supply**

I rendimenti generati vengono trasferiti ai detentori di OUSD tramite il rebasing costante del rifornimento della moneta. OUSD risistema costantemente il rifornimento di moneta in risposta al rendimento generato dal protocollo. Questo permette al prezzo di OUSD di rimanere ancorato a 1$, mentre i saldi dei wallet dei detentori del token si aggiustano in tempo reale per rispecchiare i rendimenti guadagnati dal protocollo.

Il risultato finale è una stablecoin facilmente spendibile, che guadagna rendimenti fuori misura in automatico, ed è più desiderabile da holdare rispetto alle altre stablecoin attualmente esistenti.
