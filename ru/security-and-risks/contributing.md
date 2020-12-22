# Сотрудничество

**100% Открытый исходный код**

OUSD - это проект с полностью открытым исходным кодом, и мы приветствуем любые вклады в него. Есть много способов помочь: сообщать о проблемах, добавлять код и помогать нам улучшать наше сообщество.

Мы работаем публично, и наша компания Discord открыта для всех. Если у Вас есть вопросы или Вам нужна помощь в начале работы, наши каналы Discord OUSD - лучшее место, где можно получить помощь от нашей команды и сообщества.

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

#### Процесс разработки

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. Найдите интересную проблему и общайтесь! Сообщите каналу `#engineering` [Discord](https://discord.gg/jyxpUSe), над чем вы хотите работать.
2. Отправьте запрос [члену основной команды](https://github.com/orgs/OriginProtocol/teams/core/members) в Discord и попросите добавить Вас в нашу команду [разработчиков](https://github.com/orgs/OriginProtocol/teams/contributors). В противном случае вам нужно будет форкнуть соответствующий репозиторий и поместить ветки функций в свою собственную вилку.
3. Добавьте комментарий к проблеме или назначьте сами, чтобы несколько участников случайно не работали над одной и той же задачей.
4. Начните с ветки `master` и проверьте новую ветку функции, если Вы не вносите вклад в существующую функцию.
5. Следуйте соответствующему [стилю кодирования](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) и напишите отличный код.
6. Извлеките последние подтверждения изменения кода из `master` и убедитесь, что Ваш код работает с любой другой работой, которая добавилась с момента начала Вашей работы.
7. Переместите свою ветку в вышестоящий репозиторий \(т.е. https://github.com/OriginProtocol/\[repo\]\), чтобы другие участники могли легко поработать над ней в случае необходимости.
8. Запросите обзор в PR, щелкнув значок шестеренки рядом с надписью «Рецензенты» в правом столбце.

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Стиль написания кода

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### Дизайн протокола

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature \(RFCs, papers, etc\)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Принципы сообщества

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Сообщения о проблемах

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Проблемы с безопасностью

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **Улучшение сообщества**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Вакансии на полный рабочий день

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



