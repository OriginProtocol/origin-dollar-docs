# 如何贡献

**100% 开源。**

OUSD 是一个完全开源的项目，而我们欢迎各种各样的贡献。 您可以通过报告问题，贡献代码或帮助我们改善社区的多种方式提供帮助。

我们的工作和我们的公司 Discord 都是公开的。 如果您有任何疑问或需要任何帮助，我们的 Discord OUSD 渠道是从我们的团队和社区获得帮助的最佳场所。

## 开发过程

我们的分支策略类似于 [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/)，但是我们在 `master` 分支中进行所有开发，并为已发布的代码提供 `stable` 分支。

您的开发流程应如下：

1. 选择一个您感兴趣的问题！ 请在 `#engineering` [Discord](https://discord.gg/jyxpUSe) 频道里让我们的团队知道您想贡献的内容。
2. 在 Discord 给其中一位 [核心团队成员](https://github.com/orgs/OriginProtocol/teams/core/members) 发信息，并要求把您添加到我们的 [贡献者团队](https://github.com/orgs/OriginProtocol/teams/contributors)。 否则，您需要分支相关的存储库，并将功能分支推到您自己的分叉。
3. 在议题上添加评论或将议题分配给自己，这样我们不会有多个贡献者无意间试图解决同一个问题。
4. 从 `master` 分支开始，然后签出新功能分支，除非您想为现有功能做出贡献。
5. 遵循适当的 [编码样式](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) 并编写一些很棒的代码。
6. 从 `master` 提取最新提交，并确认您的代码可与自您开始之后已合并的任何其他代码一起使用。
7. 将您的分支推到上游存储库 \(即 [https://github.com/OriginProtocol/\[repo\]\](https://github.com/OriginProtocol/[repo]\)\) ，以便其他贡献者可以轻松地使用它。
8. 请通过单击右列的“Reviewers”旁边的齿轮图标来请求 PR 的审阅。

`master` 分支被锁定，只有 [核心团队](https://github.com/orgs/OriginProtocol/teams/core) 成员能合并您的拉取请求。 由其他受信任的贡献者进行同行评审的拉取请求将被快速跟踪并更快地合并！ 在 `#engineering` Discord 频道中寻找合适的评审人。

## 编码风格

我们的存储库中使用各种编程语言。 请遵循现有的编码约定，并参考存储库中的CONTRIBUTING.md文件（如果有的话）。

对于JavaScript，我们使用 [NPM的样式](https://docs.npmjs.com/misc/coding-style)，该样式通过 [prettier](https://prettier.io/)自动实施。

对于Solidity，我们使用两个空格的缩进。

## 协议设计

在考虑协议或实施设计方案时，我们会考虑以下：

* 详细描述这个设计方案解决的问题
* 讨论所涉及的取舍
* 检讨其他现有解决方案
* 相关文献\（RFC，论文等\）的链接
* 对于提出的解决方案进行研讨

请注意，协议设计是艰苦而细腻的工作。 您可能需要产看现有文献并仔细考虑通用的用例。

## 社区准则

我们希望保持 Origin 社区的和谐和成长。 我们需要您的帮助来达到这个目标。 我们为整个社区准备了一些社区准则：

* 对其他社区成员要礼貌并互相尊重。任何地区，种族，性别或其他歧视行为都不能容忍。 做个善良的人！
* 鼓励多样性；使我们社区中的每个人都受到欢迎，无论他们的背景和贡献程度，尽量鼓励它们积极参与我们的社区。
* 保持合法，不要给任何人带来麻烦。 仅共享您自己的内容，不分享私人或敏感信息，更不要违反法律。
* 紧贴主题，确保您将信息发布到正确的频道，并避免主题外的讨论。 请记住，当您更新问题或回复电子邮件时，可能会发送给许多人。 请记得考虑这一点。 请记住，没有人喜欢垃圾邮件。

## 报告问题

如果您发现 Origin 的代码或文档中存在错误，请通过提交 GitHub 问题通知我们。 没有太小的问题。 帮助我们修复错别字！

## 安全问题

OUSD 仍在早期开发中，这意味着协议和产品中可能存在问题。 我们非常重视安全。 如果发现安全问题，请立即通知我们！

如果发现安全漏洞，请私下将报告发送到 [security@originprotocol.com](mailto:security@originprotocol.com) 或将加密消息[通过Keybase 发送给 @joshfraser](https://keybase.io/joshfraser)。 请不要创建公开议题（file a public issue）。 请务必查看我们的负责任的披露和获得漏洞赏金的资格的准则。

{% page-ref page="asset-risk.md" %}

## **社区发展**

我们的社区与我们的技术一样重要。

我们总是需要帮助来改善文档、构建与平台交互的新工具，向新用户传播信息和帮助新用户进行设置等。

如果您想帮助我们，请随时与我们联系。 我们 [Discord](https://www.originprotocol.com/discord) 上的 `general` 频道是一个分享想法并自愿提供帮助的好地方。

## 全职职位

Origin 有时会聘请开发人员担任兼职或全职职位。

我们偏向与雇用已经开始对项目做出贡献的人。 如果您想在我们的团队中担任全职职位，最好的办法是与我们的团队互动并开始贡献代码。 除非您至少合并了一些拉取请求，否则我们不太可能会给您一个全职的工程职位。

如果您有兴趣，请查看 [Origin Protocol 招聘岗位](https://angel.co/originprotocol/jobs)。 如果您想通过其他方式提供帮助，请在 [我们的 Discord 频道](https://www.originprotocol.com/discord)与我们分享。

