# Gestión de Fondos

El contrato inteligente de OUSD agrega los depósitos de monedas estables de todos los usuarios en un solo pool de activos que luego se implementan en estrategias de ganancias basadas en asignaciones preestablecidas. A diferencia de las oportunidades de Yearn Vaults, TokenSets o Zapper, los usuarios no seleccionan estrategias individuales. Todas las monedas estables depositadas y, en consecuencia, todos los tokens OUSD son fungibles.&#x20;

Los holders de OGN deciden la ponderación de cómo se distribuyen los activos entre las estrategias admitidas mediante votación semanal. Estos votos ocurren offchain y no cuestan gas. Los resultados de la encuesta semanal serán ejecutados en cadena por miembros de [Estrategas multi-firma](https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC) (conocidos como "Estrategas").

En última instancia, creemos que debería depender de la comunidad decidir cuál es el equilibrio correcto de riesgo/beneficio apropiado para OUSD. Alentamos a la comunidad a favorecer las estrategias de alto rendimiento y, al mismo tiempo, mantener la diversificación en múltiples estrategias para eliminar los puntos únicos de falla y minimizar el riesgo.&#x20;

**Cómo funciona la votación de asignación de estrategia:**

* New snapshot proposals will open for voting on the [OGN governance portal ](http://vote.originprotocol.com)at midnight Tuesday UTC (7pm eastern Monday). La votación estará abierta durante 48 horas y finalizará a la medianoche del jueves UTC (Miércoles 7pm hora Este).
* Durante este tiempo, los interesados pueden discutir los cambios de asignación en un hilo en el canal #governance en el [Discord de Origin](https://www.originprotocol.com/discord).
* Each proposal will use "weighted voting", with options for each coin/strategy combination and an option to keep the existing allocation unchanged. OGN holders can spread their votes among different listed strategies or the existing allocation.
* After the voting time has ended, Strategists will submit, verify, and execute transactions to change OUSD to the determined allocation percentages for the week. If more than 50% of the weighted votes are cast for the existing allocation, Strategists will take no action.
* Allocations will be executed for strategies that use all stablecoins first (like Convex), then each stablecoin will be allocated to the remaining strategies according to the ratio of votes for that stablecoin / strategy combination.
* Si los Estrategas consideran que alguna de las asignaciones no es segura para los fondos detrás de OUSD, pueden optar por no ejecutarlas. Además, los Estrategas pueden negarse a realizar ajustes menores cuando los costos del gas sean mayores que los beneficios esperados.&#x20;
* Like all governance proposals, Strategist allocations must meet the minimum quorum requirements (currently 1M OGN) to be considered valid.
* From a security standpoint, it is important to know that while Strategists have the ability to move funds between approved strategies or instantly pause rebasing in the case of an emergency, Strategists do not have the power to add new strategies or withdraw funds without going through the timelock. Community members can use the Strategy Validator tools to more easily [create](https://analytics.ousd.com/strategist/creator) and [decode](https://analytics.ousd.com/strategist) which actions are being performed by the Strategists.
* When voting, please remember it is inefficient to move in and out of the Convex strategy frequently and some funds need to always remain outside of Convex in order to accommodate withdrawals.



****
