# Gestión de Fondos

El contrato inteligente de OUSD agrega los depósitos de monedas estables de todos los usuarios en un solo grupo de activos invertibles. Funds are then allocated across one or more** **earning strategies at any given moment in time. La Bóveda favorece las estrategias de alto rendimiento, pero también busca mantener la diversificación en múltiples estrategias. La diversificación elimina los puntos únicos de fallas y mitiga los riesgos.

A diferencia de las oportunidades de Yearn Vaults, TokenSets o Zapper, los usuarios no seleccionan estrategias individuales. Todas las monedas estables depositadas y, en consecuencia, todos los tokens OUSD son fungibles. Una vez que se implemente nuestra estructura de gobierno completa, estas decisiones se tomarán con los comentarios de los holders de los tokens de gobierno de OUSD. Se anima a los holders de OGN a participar en la creación y votación de propuestas que afecten al protocolo en [el portal de gobernanza de OGN](https://vote.originprotocol.com).

**Estrategias de Ganancias**

Las estrategias de ganancias ponen a trabajar el capital desplegado en varias plataformas DeFi. La Bóveda determinará qué estrategias están activas y qué porcentaje del capital implementado recibirán. Estas estrategias se actualizarán y reemplazarán con el tiempo.

**Estratega**

La versión inicial del contrato inteligente de la Bóveda de OUSD le da a cada estrategia válida un peso simple entre 0% y 100% para realizar una asignación de activos simple. Estos pesos se cambiarán a menudo mediante actualizaciones de Origin a corto plazo y mediante una gobernanza descentralizada a largo plazo.

**Diversificación**

La diversificación a través de múltiples [plataformas](supported-strategies/) DeFi subyacentes reducirá el contrato inteligente y otros riesgos sistémicos. El contrato inteligente calculará los APY actuales y esperados en un esfuerzo por proporcionar rendimientos competitivos a los holders de OUSD. Con el tiempo, el contrato de la Bóveda se actualizará para cambiar de forma inteligente y autónoma entre estrategias sin ninguna intervención manual. Por ejemplo, la Bóveda cambiará automáticamente el capital entre varias estrategias de préstamos para optimizar los rendimientos.

Sin embargo, todavía se espera que ciertos parámetros de riesgo o decisiones sobre si ciertas estrategias se incluirán en el motor de toma de decisiones automatizado se tomen a través de votaciones de gobernanza. 
