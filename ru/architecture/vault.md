# Хранилище (Vault)

Vault лежит в основе протокола. Vault отвечает за создание/выкуп токенов OUSD, перебалансировку средств между различными поддерживаемыми стратегиями и ликвидацию токенов вознаграждения.

Наиболее важными общедоступными функциями в Vault являются:

* `mint ()`позволяет конвертировать один поддерживаемый стейблкоин в OUSD
* `mintMultiple ()`позволяет конвертировать несколько поддерживаемых стейблкоинов в OUSD за один вызов функции
* `redeem ()`позволяет выкупить определенное количество OUSD за другие поддерживаемые стейблкоины.
* `redeemAll ()`позволяет пользователю обменять весь свой баланс в OUSD на другие поддерживаемые стейблкоины. This is particularly useful since user balances are constantly growing as yield is accrued.
* `rebase()`updates the balances for all users based on the value of the assets currently stored in the pool.
* `allocate()`moves the assets under management into their prescribed [Stategies](strategies.md) to maximize yield and diversify risk.

On redemptions, it is the protocol and not the user that decides which stablecoin\(s\) to return to the user. This decision of which coin\(s\) to return is based on the internal ratios of the assets that are being held in the pool.



