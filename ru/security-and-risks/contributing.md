# Сотрудничество

**100% Открытый исходный код**

OUSD - это проект с полностью открытым исходным кодом, и мы приветствуем любые вклады в него. Есть много способов помочь: сообщать о проблемах, добавлять код и помогать нам улучшать наше сообщество.

Мы работаем публично, и наша компания Discord открыта для всех. Если у Вас есть вопросы или Вам нужна помощь в начале работы, наши каналы Discord OUSD - лучшее место, где можно получить помощь от нашей команды и сообщества.

#### Процесс разработки

Наша стратегия ветвления кода аналогична [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), но мы ведем всю нашу разработку в ветке `master` и имеем отдельную ветку `stable` для кода, который был выпущен.

Ваш процесс разработки должен выглядеть так:

1. Найдите интересную проблему и общайтесь! Сообщите каналу `#engineering` [Discord](https://discord.gg/jyxpUSe), над чем вы хотите работать.
2. Отправьте запрос [члену основной команды](https://github.com/orgs/OriginProtocol/teams/core/members) в Discord и попросите добавить Вас в нашу команду [разработчиков](https://github.com/orgs/OriginProtocol/teams/contributors). В противном случае вам нужно будет форкнуть соответствующий репозиторий и поместить ветки функций в свою собственную вилку.
3. Добавьте комментарий к проблеме или назначьте сами, чтобы несколько участников случайно не работали над одной и той же задачей.
4. Начните с ветки `master` и проверьте новую ветку функции, если Вы не вносите вклад в существующую функцию.
5. Следуйте соответствующему [стилю кодирования](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) и напишите отличный код.
6. Извлеките последние подтверждения изменения кода из `master` и убедитесь, что Ваш код работает с любой другой работой, которая добавилась с момента начала Вашей работы.
7. Переместите свою ветку в вышестоящий репозиторий \(т.е. https://github.com/OriginProtocol/\[repo\]\), чтобы другие участники могли легко поработать над ней в случае необходимости.
8. Запросите обзор в PR, щелкнув значок шестеренки рядом с надписью «Рецензенты» в правом столбце.

Ветка `master` заблокирована таким образом, что только члены [основной команды](https://github.com/orgs/OriginProtocol/teams/core) способны обработать Ваши запросы на добавление внёсенных изменений. Запросы на добавление внёсенных изменений, которые проверяются другими доверенными участниками, будут быстрее отслеживаться и добавляться! Поищите подходящих рецензентов на канале `#engineering` в Discord.

#### Стиль написания кода

В наших репозиториях мы используем множество языков программирования. При внесении Вашего вклада, пожалуйста, следуйте существующим соглашениям о написании кода и обращайтесь к файлу CONTRIBUTING.md в репозитории, если он существует.

Для JavaScript мы используем [NPM стиль](https://docs.npmjs.com/misc/coding-style), который автоматически применяется через [prettier](https://prettier.io/).

Для Solidity мы используем отступы через два пробела.

#### Дизайн протокола

При рассмотрении предложений по дизайну протокола или реализации мы ищем:

* Описание проблемы, которую решает данное проектное предложение
* Обсуждение возможных компромиссов
* Обзор других существующих решений
* Ссылки на соответствующую литературу \(RFC, статьи и т. д.\)
* Обсуждение предлагаемого решения

Обратите внимание, что разработка протокола - это тяжелая и кропотливая работа. Возможно, вам потребуется просмотреть существующую литературу и продумать обобщенные варианты использования.

#### Принципы сообщества

Мы хотим, чтобы сообщество Origin было отличным, растущим и способным сотрудничать. Нам нужна ваша помощь, чтобы так и было. Чтобы помочь с этим, мы разработали несколько общих рекомендаций для сообщества в целом:

* Ведите себя хорошо: будьте вежливы, уважительны и учтивы по отношению к другим членам сообщества: недопустимы оскорбления на религиозной, расовой, гендерной или любой другой почве. Нам больше нравятся хорошие люди, чем плохие!
* Поощряйте разнообразие и участие: сделайте так, чтобы каждый в нашем сообществе почувствовал себя желанным гостем, независимо от его происхождения и степени их вклада, и сделайте все возможное, чтобы поощрять участие в нашем сообществе.
* Соблюдайте закон: не доставляйте никому проблем. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Reporting Issues

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Security Issues

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **Community Improvement**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Full-Time Positions

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



