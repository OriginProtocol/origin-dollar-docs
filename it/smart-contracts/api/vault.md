---
description: >-
  Il vault è il contratto principale del protocollo. Il vault è responsabile del conio / riscatto dei token OUSD, del ribilanciamento dei fondi tra le varie strategie supportate e della liquidazione dei token ricompensa.
---

# Vault

## Metodi

### mint\(\) <a id="mint"></a>

**`function mint(address _asset, uint256 _amount)`**

Genera OUSD in cambio di un deposito di un certo ` _amount` di stable coin specificata dal parametro ` _asset`. Il chiamante riceve un certo numero di OUSD dipendentemente dal **exchange rate**.

| Nome del Parametro | Tipo    | Descrizione                                                                                                                                          |
|:------------------ |:------- |:---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset          | address | Indirizzo della stablecoin [supportata](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) |
| \_amount         | uint256 | cifra depositata, espressa in unità decimali                                                                                                         |

### mintMultiple\(\) <a id="mintmultiple"></a>

**`function mintMultiple(address[] _assets, uint256[] _amounts)`**

Conia OUSD in cambio di un deposito di più stablecoin in una singola chiamata. Le stablecoin sono specificate dal parametro array `_assets` e gli importi dal parametro array `_amounts`. Il chiamante riceve un certo numero di OUSD dipendentemente dal **tasso di cambio**.

| Nome del parametro | Tipo          | Descrizione                                                                                                                                          |
|:------------------ |:------------- |:---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_assets         | address\[\] | Indirizzi delle stablecoin [supportate](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) |
| \_amounts        | uint256\[\] | importi depositati, espressi in unità decimali                                                                                                       |

{% hint style="warning" %}
Riguardo le redemption, non è l'utente che decide quale o quali stablecoin vengono restituite all'utente, ma è il protocollo stesso. Questa decisione su quale o quali coin vengono restituite, è basata sui cambi interni degli asset che sono custoditi all'interno del vault
{% endhint %}

### redeem\(\) <a id="redeem"></a>

**`function redeem(uint256 _amount)`**

Gli OUSD specificati dal parametro` _amount` viene riscattato in cambio di una o più stablecoin tra quelle supportate. La quantità di stablecoin ricevute dipende dal **tasso di cambio**.

| Nome del Parametro | Tipo    | Descrizione                                 |
|:------------------ |:------- |:------------------------------------------- |
| \_amount         | uint256 | quantità di OUSD espressa in unità decimali |

### redeemAll\(\)‌ <a id="redeemall"></a>

**`function redeemAll()`**‌

Tutti gli OUSD in possesso dell'utente, vengono riscattati in cambio di una o più stablecoin supportate. La quantità di stablecoin ricevute dipende dal **tasso di cambio**.

### rebase\(\) <a id="rebase"></a>

**`function rebase()`**‌

Aggiorna i saldi di tutti gli utenti, sulla base del valore degli asset attualmente custoditi nel vault. Restituisce il valore totale delle attività e delle strategie sottostanti rappresentate dal tipo ` uint256`

### allocate\(\) <a id="allocate"></a>

**`function allocate()`**‌

Sposta gli asset sotto la gestione delle rispettive [Strategie](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/architecture/strategies), per massimizzare i rendimenti e diversificare il rischio

### totalValue\(\) <a id="totalvalue"></a>

**`function totalValue()`**‌

Restituisce il valore totale degli asset e delle strategie sottostanti.

| `return` name | Tipo    | Descrizione                                              |
|:------------- |:------- |:-------------------------------------------------------- |
| value         | uint256 | valore totale degli asset e delle strategie sottostanti. |

### checkBalance\(\) <a id="checkbalance"></a>

**`function checkBalance(address _asset)`**‌

Restituisce il saldo di un asset detenuto nel Vault, specificato dal parametro ` _asset` e tutte le strategie rappresentate dal tipo ` uint256`.

| Nome del parametro | Tipo    | Descrizione                                                                                                                                          |
|:------------------ |:------- |:---------------------------------------------------------------------------------------------------------------------------------------------------- |
| \_asset          | address | Indirizzo della stablecoin [supportata](https://app.gitbook.com/@originprotocol/s/ousd/~/drafts/-MHSojsgAcBjyg6RCmpF/core-concepts/supported-assets) |

### calculateRedeemOutputs\(\) <a id="calculateredeemoutputs"></a>

**`function calculateRedeemOutputs(uint256 _amount)`**‌

Calcola il mix delle stablecoin che la funzione `redeem` restituirebbe nel momento in cui si sta riscattando un certo numero di OUSD specificato dal parametro `_amount`. Restituisce un array di valori di stablecoin.

Per attribuire i valori delle stablecoin alla corretta valuta della stablecoin, questa chiamata dovrebbe essere utilizzata in congiunzione alla funzione ` getAllAssets` che restituisce l'array con gli indirizzi delle stablecoin.

L'indice dell'array restituito dalla funzione `calculateRedeemOutputs`, corrisponde all'indirizzo della stablecoin avente lo stesso indice nell'array restituito dalla funzione `getAllAssets`.

| Nome del parametro | Tipo    | Descrizione                                 |
|:------------------ |:------- |:------------------------------------------- |
| \_amount         | uint256 | quantità di OUSD espressa in unità decimali |

| `return` name | Tipo          | Descrizione                                                          |
|:------------- |:------------- |:-------------------------------------------------------------------- |
| outputs       | uint256\[\] | array con il numero di stablecoin restituito dalla funzione `redeem` |

### getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Restituisce il numero di stablecoin supportate rappresentate dal tipo `uint256`

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**

Restituisce, in ordine, tutti gli indirizzi delle stablecoin supportate, ed è rappresentato dal tipo ` uint256`

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**

Restituisce il numero delle strategie attive nel Vault, ed è rappresentato dal tipo ` uint256`

### getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**

Restituisce il rendimento totale annuo \(APR\) del Vault e di tutte le strategie, ed è rappresentato dal tipo ` uint256`. Resulting number has 18 decimal spaces.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Restituisce il valore boolean true se l'asset specificato dal parametro `_asset` è supportato dal Vault.

| Nome del Parametro | Tipo    | Descrizione                |
|:------------------ |:------- |:-------------------------- |
| \_asset          | address | Indirizzo della stablecoin |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Restituisce il prezzo del tasso di cambio della stablecoin specificata dal parametro `symbol`, che viene utilizzata per coniare gli OUSD, ed è rappresentato dal tipo ` uint256`. Il numero risultante ha 18 cifre decimali.

| Nome del Parametro | Tipo   | Descrizione              |
|:------------------ |:------ |:------------------------ |
| symbol             | string | Simbolo della stablecoin |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Restituisce il prezzo del tasso di cambio della stablecoin specificata dal parametro `symbol`, che viene utilizzata per riscattare gli OUSD, ed è rappresentato dal tipo ` uint256`. Il numero risultante ha 18 cifre decimali.

| Nome del Parametro | Tipo   | Descrizione              |
|:------------------ |:------ |:------------------------ |
| symbol             | string | Simbolo della stablecoin |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Restituisce il prezzo del tasso di cambio della stablecoin specificata dal parametro ` _asset `, che viene utilizzata per coniare gli OUSD, ed è rappresentato dal tipo ` uint256`. Il numero risultante ha 18 cifre decimali.

| Nome del Parametro | Tipo    | Descrizione                 |
|:------------------ |:------- |:--------------------------- |
| \_asset          | address | Indirizzo della stablecoin‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Restituisce il prezzo del tasso di cambio della stablecoin specificata dal parametro ` _asset `, che viene utilizzata per riscattare gli OUSD, ed è rappresentato dal tipo ` uint256`. Il numero risultante ha 18 cifre decimali.

| Nome del Parametro | Tipo    | Descrizione                |
|:------------------ |:------- |:-------------------------- |
| \_asset          | address | Indirizzo della stablecoin |

