# 如何贡献

**100% 开源。**

OUSD 是一个完全开源的项目，而我们欢迎各种各样的贡献。 您可以通过报告问题，贡献代码或帮助我们改善社区的多种方式提供帮助。

我们的工作和我们的公司 Discord 都是公开的。 如果您有任何疑问或需要任何帮助，我们的 Discord OUSD 渠道是从我们的团队和社区获得帮助的最佳场所。

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

#### 开发过程

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. 选择一个您感兴趣的问题！ 请在 `#engineering` [Discord](https://discord.gg/jyxpUSe) 频道里让我们的团队知道您想贡献的内容。
2. 在 Discord 给其中一位 [核心团队成员](https://github.com/orgs/OriginProtocol/teams/core/members) 发信息，并要求把您添加到我们的 [贡献者团队](https://github.com/orgs/OriginProtocol/teams/contributors)。 否则，您需要分支相关的存储库，并将功能分支推到您自己的分叉。
3. 在议题上添加评论或将议题分配给自己，这样我们不会有多个贡献者无意间试图解决同一个问题。
4. 从 `master` 分支开始，然后签出新功能分支，除非您想为现有功能做出贡献。
5. 遵循适当的 [编码样式](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) 并编写一些很棒的代码。
6. 从 `master` 提取最新提交，并确认您的代码可与自您开始之后已合并的任何其他代码一起使用。
7. 将您的分支推到上游存储库 \(即 https://github.com/OriginProtocol/\[repo\]\) ，以便其他贡献者可以轻松地使用它。
8. 请通过单击右列的“Reviewers”旁边的齿轮图标来请求 PR 的审阅。

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### 编码风格

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### 协议设计

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature \(RFCs, papers, etc\)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### 社区准则

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### 报告问题

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### 安全问题

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **社区发展**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### 全职职位

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



