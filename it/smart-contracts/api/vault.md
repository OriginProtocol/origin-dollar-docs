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

Calculate the mix of stablecoins that a `redeem` function would return when redeeming certain amount of OUSD specified by the `_amount` parameter. Returns an array of stablecoin values.

To attribute the stablecoin values to the correct stablecoin currency this call should be used in conjunction with `getAllAssets` function that returns an array of stablecoin addresses.

The index of an array that is returned by the `calculateRedeemOutputs` corresponds to the stablecoin address with the same index in an array returned by the `getAllAssets` function.

| Parameter Name | Type    | Description                               |
|:-------------- |:------- |:----------------------------------------- |
| \_amount     | uint256 | amount of OUSD expressed in decimal units |

| `return` name | Type          | Description                                                                 |
|:------------- |:------------- |:--------------------------------------------------------------------------- |
| outputs       | uint256\[\] | array of the amount of the stablecoin assets `redeem` function would return |

### getAssetCount\(\) <a id="getassetcount"></a>

**`function getAssetCount()`**‌

Return the number of supported stablecoin assets represented by `uint256` type.‌

### getAllAssets\(\) <a id="getallassets"></a>

**`function getAllAssets()`**‌

Return all assets addresses of supported stablecoin assets in order represented by `uint256` type.‌

### getStrategyCount\(\)‌ <a id="getstrategycount"></a>

**`function getStrategyCount()`**‌

Return the number of strategies active on the Vault represented by `uint256` type.‌

### getAPR\(\) <a id="getapr"></a>

**`function getAPR()`**‌

Return the total annual percentage yield \(APR\) of the Vault and all Strategies represented by `uint256` type. Resulting number has 18 decimal spaces.‌

### isSupportedAsset\(\) <a id="issupportedasset"></a>

**`function isSupportedAsset(address _asset)`**‌

Return the boolean that is true if the asset specified by the `_asset` parameter is supported by the Vault.

| Parameter Name | Type    | Description               |
|:-------------- |:------- |:------------------------- |
| \_asset      | address | Address of the stablecoin |

### priceUSDMint\(\) <a id="issupportedasset-1"></a>

**`function priceUSDMint(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type   | Description              |
|:-------------- |:------ |:------------------------ |
| symbol         | string | Symbol of the stablecoin |

### priceUSDRedeem\(\) <a id="issupportedasset-2"></a>

**`function priceUSDRedeem(string symbol)`**‌‌

Returns the exchange rate price of a stable coin specified by the `symbol` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type   | Description              |
|:-------------- |:------ |:------------------------ |
| symbol         | string | Symbol of the stablecoin |

### priceAssetUSDMint\(\)‌ <a id="issupportedasset-3"></a>

**`function priceAssetUSDMint(address _asset)`**‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when minting OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type    | Description                |
|:-------------- |:------- |:-------------------------- |
| \_asset      | address | Address of the stablecoin‌ |

### priceAssetUSDRedeem\(\)‌ <a id="issupportedasset-3-1"></a>

**`function priceAssetUSDRedeem(address _asset)`**‌‌‌

Returns the exchange rate price of a stable coin specified by the `_asset` parameters used when redeeming OUSD represented by `uint256` type. Resulting number has 18 decimal spaces.

| Parameter Name | Type    | Description               |
|:-------------- |:------- |:------------------------- |
| \_asset      | address | Address of the stablecoin |

