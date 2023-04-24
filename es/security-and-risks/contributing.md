# Contribuyendo

**100% Código abierto**

OUSD es un proyecto completamente de código abierto y agradecemos contribuciones de todo tipo. Hay muchas formas de ayudar, desde informar problemas, contribuir con código y ayudarnos a mejorar nuestra comunidad.

Trabajamos en público y nuestra compañía en Discord está abierta a todos. Si tiene preguntas o necesita ayuda para comenzar, nuestros canales de Discord de OUSD son el mejor lugar para obtener ayuda de nuestro equipo y comunidad.

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

#### Proceso de Desarrollo

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. ¡Encuentra un tema interesante y comunícate! Por favor informe al canal `#engineering` [Discord](https://discord.gg/jyxpUSe) qué desea trabajar.
2. Haga ping a un miembro del equipo central, [](https://github.com/orgs/OriginProtocol/teams/core/members) miembro en Discord y pida que lo agreguen a nuestro equipo de [colaboradores](https://github.com/orgs/OriginProtocol/teams/contributors). De lo contrario, deberá bifurcar el repositorio relevante y enviar las ramas de funciones a su propia bifurcación.
3. Agregue un comentario al problema o autoasignelo para que no tengamos varios colaboradores trabajando involuntariamente en la misma tarea.
4. Comience con la rama `master` y compruebe una nueva rama de función a menos que esté contribuyendo a una función existente.
5. Siga el estilo de codificación [apropiado](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) y escriba un código increíble.
6. Extraiga las últimas confirmaciones de `master` y confirme que su código funciona con cualquier otro trabajo que se haya fusionado desde que comenzó.
7. Empuje su rama al repositorio de arriba \ (es decir, https: //github.com/OriginProtocol/ \ [repo \] \) para que otros contribuyentes puedan trabajar fácilmente si es necesario.
8. Solicite una revisión en el RP haciendo clic en el ícono de ajustes junto a "Reviewers" en la columna de la derecha.

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Estilo de Codificación

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### Diseño de Protocolo

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature \(RFCs, papers, etc\)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Principios de la Comunidad

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Informar Problemas

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Temas de Seguridad

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **Mejora de la Comunidad**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Posiciones de Tiempo Completo

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



