# Cofre

O cofre está no núcleo do protocolo. O cofre é responsável pela emissão/resgate de tokens OUSD, pelo reequilibrio de fundos entre as várias estratégias suportadas, e pela liquidação de tokens de recompensa.

As funções mais importantes do Cofre que podem ser chamadas publicamente são:

* `mint()`permite que uma única stablecoin suportada seja convertida para OUSD
* `mintMultiple()`permite que múltiplas stablecoims suportadas sejam convertidas para OUSD numa única chamada
* `redeem()`permite que um determinado montante de ousd seja resgatado por outras stablecoins suportadas.
* `redeemAll()`permite que um usuário resgate todo o seu saldo de OUSD por outras stablecoins suportadas. Isto é particularmente útil, visto que os saldos dos usuários estão em constante crescimento à medida que o rendimento é acumulado.
* `rebase()`atualiza os saldos de todos os usuários com base no valor dos ativos atualmente armazenados na pool.
* `allocate()`moves the assets under management into their prescribed [Stategies](strategies.md) to maximize yield and diversify risk.

On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) to return to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.



