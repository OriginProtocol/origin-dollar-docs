# Contribuyendo

**100% Código abierto**

OUSD es un proyecto completamente de código abierto y agradecemos contribuciones de todo tipo. Hay muchas formas de ayudar, desde informar problemas, contribuir con código y ayudarnos a mejorar nuestra comunidad.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

We work in public and our company Discord is open to all. If you have questions or need help getting started, our [Discord OUSD channels](https://discord.gg/jyxpUSe) are the best place to get assistance from our team and community.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies. Various other developer tools can be found at [ousd.com/dashboard](https://ousd.com/dashboard).

#### Proceso de Desarrollo

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. ¡Encuentra un tema interesante y comunícate! Por favor informe al canal `#engineering` [Discord](https://discord.gg/jyxpUSe) qué desea trabajar.
2. Haga ping a un miembro del equipo central, [](https://github.com/orgs/OriginProtocol/teams/core/members) miembro en Discord y pida que lo agreguen a nuestro equipo de [colaboradores](https://github.com/orgs/OriginProtocol/teams/contributors). De lo contrario, deberá bifurcar el repositorio relevante y enviar las ramas de funciones a su propia bifurcación.
3. Agregue un comentario al problema o autoasignelo para que no tengamos varios colaboradores trabajando involuntariamente en la misma tarea.
4. Comience con la rama `master` y compruebe una nueva rama de función a menos que esté contribuyendo a una función existente.
5. Escribe un código asombroso.
6. Extraiga las últimas confirmaciones de `master` y confirme que su código funciona con cualquier otro trabajo que se haya fusionado desde que comenzó.
7. Push your branch to the upstream repository (i.e. https://github.com/OriginProtocol/\[repo]) so that other contributors can easily work off of it if necessary.
8. Solicite una revisión en el RP haciendo clic en el ícono de ajustes junto a "Reviewers" en la columna de la derecha.

For critical smart contract code to be merged it must pass the following checklist:

*  Código revisado por 2 revisores
*  Las pruebas unitarias pasan
*  Las pruebas de deslizamiento pasan sin previo aviso
*  Pasan las pruebas de equidna

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Estilo de Codificación

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io).

For Solidity, we use two-space indents.

#### Diseño de Protocolo

When considering protocol or implementation design proposals, we are looking for:

* Una descripción del problema que resuelve esta propuesta de diseño
* Discusión de las compensaciones involucradas
* Revisión de otras soluciones existentes
* Links to relevant literature (RFCs, papers, etc)
* Discusión de la solución propuesta

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Principios de la Comunidad

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Sea amable: sea cortés, respetuoso y cortés con los miembros de la comunidad: no se tolerará ningún abuso regional, racial, de género o de otro tipo. ¡Nos gustan las personas agradables mucho más que las malas!
* Fomentar la diversidad y la participación: hacer que todos en nuestra comunidad se sientan bienvenidos, independientemente de sus antecedentes y el alcance de sus contribuciones, y hacer todo lo posible para fomentar la participación en nuestra comunidad.
* Manténgala legal: Básicamente, no meta a nadie en problemas. Comparta solo el contenido de su propiedad, no comparta información privada o confidencial y no infrinja las leyes.
* Mantente en el tema: asegúrate de publicar en el canal correcto y evita discusiones fuera del tema. Recuerde cuando actualiza un problema o responde a un correo electrónico que potencialmente está enviando a una gran cantidad de personas. Considere esto antes de actualizar. Recuerde también que a nadie le gusta el spam.

#### Informar Problemas

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Temas de Seguridad

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% content-ref url="../security-and-risks/bug-bounties.md" %}
[bug-bounties.md](../security-and-risks/bug-bounties.md)
{% endcontent-ref %}

#### **Mejora de la Comunidad**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `discussion` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Posiciones de Tiempo Completo

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full-time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).

