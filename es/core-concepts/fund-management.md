# Gestión de Fondos

El contrato inteligente de OUSD agrega los depósitos de monedas estables de todos los usuarios en un solo pool de activos que luego se implementan en estrategias de ganancias basadas en asignaciones preestablecidas. A diferencia de las oportunidades de Yearn Vaults, TokenSets o Zapper, los usuarios no seleccionan estrategias individuales. Todas las monedas estables depositadas y, en consecuencia, todos los tokens OUSD son fungibles.&#x20;

Los holders de OGN deciden la ponderación de cómo se distribuyen los activos entre las estrategias admitidas mediante votación semanal. Estos votos ocurren offchain y no cuestan gas. Los resultados de la encuesta semanal serán ejecutados en cadena por miembros de [Estrategas multi-firma](https://etherscan.io/address/0xF14BBdf064E3F67f51cd9BD646aE3716aD938FDC) (conocidos como "Estrategas").

En última instancia, creemos que debería depender de la comunidad decidir cuál es el equilibrio correcto de riesgo/beneficio apropiado para OUSD. Alentamos a la comunidad a favorecer las estrategias de alto rendimiento y, al mismo tiempo, mantener la diversificación en múltiples estrategias para eliminar los puntos únicos de falla y minimizar el riesgo.&#x20;

**Cómo funciona la votación de asignación de estrategia:**

* New snapshot proposals will open for voting on the [OGN governance portal ](http://vote.originprotocol.com)at midnight Tuesday UTC (7pm eastern Monday). La votación estará abierta durante 48 horas y finalizará a la medianoche del jueves UTC (Miércoles 7pm hora Este).
* Durante este tiempo, los interesados pueden discutir los cambios de asignación en un hilo en el canal #governance en el [Discord de Origin](https://www.originprotocol.com/discord).
* Cada propuesta utilizará "votación ponderada", con opciones para cada combinación de moneda/estrategia. Los holders de OGN pueden repartir sus votos entre diferentes estrategias enumeradas.
* Una vez finalizado el tiempo de votación, los Estrategas enviarán, verificarán y ejecutarán transacciones para cambiar el OUSD a los porcentajes de asignación determinados para la semana.
* Estas asignaciones se ejecutarán para las estrategias que usan todas las monedas estables primero (como Convex), luego cada moneda estable se asignará a las estrategias restantes de acuerdo con la proporción de votos para esa combinación de moneda estable/estrategia.
* Si los Estrategas consideran que alguna de las asignaciones no es segura para los fondos detrás de OUSD, pueden optar por no ejecutarlas. Además, los Estrategas pueden negarse a realizar ajustes menores cuando los costos del gas sean mayores que los beneficios esperados.&#x20;
* Desde el punto de vista de la seguridad, es importante saber que si bien los Estrategas tienen la capacidad de mover fondos entre estrategias aprobadas o pausar instantáneamente el rebase en caso de una emergencia, los Estrategas no tienen el poder de agregar nuevas estrategias o retirar fondos sin pasar por el bloqueo de tiempo. Los miembros de la comunidad pueden utilizar las herramientas del Validador de estrategias para [crear](https://analytics.ousd.com/strategist/creator) y [decodificar](https://analytics.ousd.com/strategist) más fácilmente qué acciones están realizando los estrategas.
* Al votar, recuerde que es ineficiente entrar y salir de la estrategia Convex con frecuencia y algunos fondos deben permanecer siempre fuera de Convex para poder realizar retiros.



****
