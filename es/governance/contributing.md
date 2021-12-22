# Contribuyendo

**100% Código abierto**

OUSD es un proyecto completamente de código abierto y agradecemos contribuciones de todo tipo. Hay muchas formas de ayudar, desde informar problemas, contribuir con código y ayudarnos a mejorar nuestra comunidad.

{% content-ref url="broken-reference" %}
[Enlace roto](broken-reference)
{% endcontent-ref %}

Trabajamos en público y el Discord de nuestra empresa está abierto a todos. Si tiene preguntas o necesita ayuda para comenzar, nuestros [canales de OUSD en Discord](https://discord.gg/jyxpUSe) son el mejor lugar para obtener ayuda de nuestro equipo y comunidad.

{% content-ref url="broken-reference" %}
[Enlace roto](broken-reference)
{% endcontent-ref %}

**Análisis del Desarrollador**

Nuestro panel de desarrollo interno está disponible en [analytics.ousd.com](https://analytics.ousd.com). El panel muestra el suministro circulante actual, los activos bajo administración en la bóveda y las asignaciones actuales entre cada una de las monedas estables y estrategias. Se pueden encontrar otras herramientas para desarrolladores en [ousd.com/dashboard](https://ousd.com/dashboard).

#### Proceso de Desarrollo

Nuestra estrategia de ramificación es similar a [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), pero hacemos todo nuestro desarrollo en la rama `master` y tenemos una rama `estable` para el código que se ha lanzado.

Su flujo de desarrollo debería verse así:

1. ¡Encuentra un tema interesante y comunícate! Por favor informe al canal `#engineering` [Discord](https://discord.gg/jyxpUSe) qué desea trabajar.
2. Haga ping a un miembro del equipo central, [](https://github.com/orgs/OriginProtocol/teams/core/members) miembro en Discord y pida que lo agreguen a nuestro equipo de [colaboradores](https://github.com/orgs/OriginProtocol/teams/contributors). De lo contrario, deberá bifurcar el repositorio relevante y enviar las ramas de funciones a su propia bifurcación.
3. Agregue un comentario al problema o autoasignelo para que no tengamos varios colaboradores trabajando involuntariamente en la misma tarea.
4. Comience con la rama `master` y compruebe una nueva rama de función a menos que esté contribuyendo a una función existente.
5. Escribe un código asombroso.
6. Extraiga las últimas confirmaciones de `master` y confirme que su código funciona con cualquier otro trabajo que se haya fusionado desde que comenzó.
7. Empuje su rama al repositorio (es decir, https://github.com/OriginProtocol/\[repo]) para que otros contribuyentes puedan trabajar fácilmente si es necesario.
8. Solicite una revisión en el RP haciendo clic en el ícono de ajustes junto a "Reviewers" en la columna de la derecha.

Para fusionar el código de contrato inteligente crítico, debe pasar la siguiente lista de verificación:

*  Código revisado por 2 revisores
*  Las pruebas unitarias pasan
*  Las pruebas de deslizamiento pasan sin previo aviso
*  Pasan las pruebas de equidna

La rama `master` está bloqueada para que solo los miembros del [equipo central](https://github.com/orgs/OriginProtocol/teams/core) puedan fusionar sus solicitudes de extracción. Las solicitudes de extracción que son revisadas por pares por otros colaboradores de confianza se acelerarán y se fusionarán más rápido! Consulte el canal `#engineering` de Discord para ver los revisores adecuados.

#### Estilo de Codificación

Usamos una variedad de lenguajes de programación en nuestros repositorios. Cuando contribuya, siga las convenciones de codificación existentes y consulte el archivo CONTRIBUTING.md en el repositorio, si existe.

Para JavaScript, usamos el [estilo NPM](https://docs.npmjs.com/misc/coding-style), que se aplica automáticamente a través de [prettier](https://prettier.io).

Para Solidity, usamos sangrías de dos espacios.

#### Diseño de Protocolo

Al considerar propuestas de diseño de protocolo o implementación, buscamos:

* Una descripción del problema que resuelve esta propuesta de diseño
* Discusión de las compensaciones involucradas
* Revisión de otras soluciones existentes
* Enlaces a literatura relevante (RFC, artículos, etc.)
* Discusión de la solución propuesta

Tenga en cuenta que el diseño del protocolo es un trabajo arduo y meticuloso. Es posible que deba revisar la literatura existente y pensar en casos de uso generalizados.

#### Principios de la Comunidad

Queremos que la comunidad de Origin siga siendo increíble, en crecimiento y colaborativa. Necesitamos su ayuda para que siga siendo así. Para ayudar con esto, hemos elaborado algunas pautas generales para la comunidad en su conjunto:

* Sea amable: sea cortés, respetuoso y cortés con los miembros de la comunidad: no se tolerará ningún abuso regional, racial, de género o de otro tipo. ¡Nos gustan las personas agradables mucho más que las malas!
* Fomentar la diversidad y la participación: hacer que todos en nuestra comunidad se sientan bienvenidos, independientemente de sus antecedentes y el alcance de sus contribuciones, y hacer todo lo posible para fomentar la participación en nuestra comunidad.
* Manténgala legal: Básicamente, no meta a nadie en problemas. Comparta solo el contenido de su propiedad, no comparta información privada o confidencial y no infrinja las leyes.
* Mantente en el tema: asegúrate de publicar en el canal correcto y evita discusiones fuera del tema. Recuerde cuando actualiza un problema o responde a un correo electrónico que potencialmente está enviando a una gran cantidad de personas. Considere esto antes de actualizar. Recuerde también que a nadie le gusta el spam.

#### Informar Problemas

Si encuentra bugs, errores o inconsistencias en el código o los documentos de Origin, háganoslo saber presentando un problema en GitHub. Ningún problema es demasiado pequeño. ¡Ayúdanos a arreglar nuestros errores!

#### Temas de Seguridad

OUSD aún está en desarrollo temprano, lo que significa que puede haber problemas con el protocolo o en nuestras implementaciones. Nos tomamos muy en serio las vulnerabilidades de seguridad. Si descubre un problema de seguridad, háganoslo saber de inmediato!

Si encuentra una vulnerabilidad de seguridad, envíe su informe de forma privada a [security@originprotocol.com](mailto:security@originprotocol.com) o envíe un mensaje cifrado a [@joshfraser en Keybase](https://keybase.io/joshfraser). NO presente un problema público. Asegúrese de revisar nuestras pautas para la divulgación responsable y la elegibilidad para recompensas por errores.

{% content-ref url="../security-and-risks/bug-bounties.md" %}
[bug-bounties.md](../security-and-risks/bug-bounties.md)
{% endcontent-ref %}

#### **Mejora de la Comunidad**

Origin tiene tanto que ver con la comunidad como con nuestra tecnología.

Necesitamos ayuda constante para mejorar nuestra documentación, crear nuevas herramientas para interactuar con nuestra plataforma, hacer correr la voz a nuevos usuarios, ayudar a los nuevos usuarios a configurar y mucho más.

Póngase en contacto si desea ayudar. Our `discussion` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Posiciones de Tiempo Completo

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full-time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).

