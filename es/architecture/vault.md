# Bóveda

La bóveda es el núcleo del protocolo. La bóveda es responsable de acuñar/canjear tokens OUSD, reequilibrar fondos entre las diversas estrategias compatibles y liquidar tokens de recompensa.

Las funciones que se pueden llamar públicamente más importantes en la Bóveda son:

* `Acuñar()`permite convertir una única moneda estable compatible a OUSD
* `Acuña-Multiple()`permite convertir múltiples monedas estables compatibles a OUSD en una sola llamada
* `Canjear()`permite canjear una cantidad específica de OUSD por otras monedas estables admitidas.
* `Canjear todo()`permite a un usuario canjear su saldo completo de OUSD por otras monedas estables compatibles. Esto es particularmente útil ya que los saldos de los usuarios aumentan constantemente a medida que se acumula el rendimiento.
* `Rebasar ()`actualiza los saldos de todos los usuarios en función del valor de los activos almacenados actualmente en el grupo de liquidez.
* `Asignar()`mueve los activos bajo administración a sus [estrategias](strategies.md) prescritas para maximizar el rendimiento y diversificar el riesgo.

En los canjes, es el protocolo y no el usuario el que decide qué moneda estable \(s\) devolver al usuario. Esta decisión de qué moneda \(s\) devolver se basa en las relaciones internas de los activos que se mantienen en el grupo de liquidez.



