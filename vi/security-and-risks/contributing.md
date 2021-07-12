# Đóng góp

**100% Mã nguồn mở**

OUSD là dự án mã nguồn mở hoàn toàn và chúng tôi hoan nghênh mọi đóng góp của toàn thể cộng đồng. Bạn có thể hỗ trợ đội ngũ chúng tôi bằng việc báo cáo sự cố bảo mật, đóng góp lập trình hay giúp chúng tôi cải thiện cộng đồng của mình.

Chúng tôi làm việc một cách công khai và tài khoản Discord luôn chào đón tất cả cá thành viên trong cộng đồng. Nếu bạn có câu hỏi hoặc cần trợ giúp, các kênh Discord OUSD là nơi tốt nhất để nhận hỗ trợ từ nhóm và cộng đồng của chúng tôi.

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

#### Quá trình phát triển

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. Tìm một vấn đề thú vị và trao đổi với chúng tôi! Vui lòng ghé kênh `#engineering` [Discord](https://discord.gg/jyxpUSe) và cho chúng tôi biết bạn muốn làm gì.
2. Nhắn tin cho [thành viên của team](https://github.com/orgs/OriginProtocol/teams/core/members) trên Discord và yêu cầu được thêm vào nhóm [cộng tác viên](https://github.com/orgs/OriginProtocol/teams/contributors) của chúng tôi. Nếu không, bạn sẽ cần phải folk kho giữ liệu code (repo) liên quan và đẩy các nhánh tính năng vào folk riêng của bạn.
3. Thêm nhận xét về vấn đề hoặc tự phân bổ cho bản thân tránh tình trạng nhiều cộng tác viên cùng xử lý 1 nhiệm vụ.
4. Bắt đầu với nhánh `chính` và kiểm tra nhánh tính năng mới trừ khi bạn đang đóng góp vào một tính năng hiện có.
5. Sử dụng [kiểu lập trình](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) thích hợp và lập trình mã code tốt.
6. Kéo các cam kết mới nhất từ `nhánh chính` và xác nhận rằng mã lập trình của bạn hoạt động tốt với với bất kỳ công việc nào đã được tích hợp kể từ khi bạn bắt đầu.
7. Đẩy chi nhánh của bạn lên kho lưu trữ ngược dòng (tức là https: //github.com/OriginProtocol/ [repo]) để những người đóng góp khác có thể dễ dàng xử lý nó nếu cần.
8. Vui lòng yêu cầu đánh giá trong bài PR bằng cách nhấp vào biểu tượng bánh răng bên cạnh “Người đánh giá” ở cột bên phải.

For critical smart contract code to be merged it must pass the following checklist:

*  Code reviewed by 2 reviewers
*  Unit tests pass
*  Slither tests pass with no warning
*  Echidna tests pass

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Kiểu lập trình

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### Thiết kế giao thức

When considering protocol or implementation design proposals, we are looking for:

* A description of the problem this design proposal solves
* Discussion of the trade-offs involved
* Review of other existing solutions
* Links to relevant literature \(RFCs, papers, etc\)
* Discussion of the proposed solution

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Hỗ trợ cộng đồng

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Be nice: Be courteous, respectful and polite to fellow community members: no regional, racial, gender, or other abuse will be tolerated. We like nice people way better than mean ones!
* Encourage diversity and participation: Make everyone in our community feel welcome, regardless of their background and the extent of their contributions, and do everything possible to encourage participation in our community.
* Keep it legal: Basically, don’t get anybody in trouble. Share only content that you own, do not share private or sensitive information, and don’t break laws.
* Stay on topic: Make sure that you are posting to the correct channel and avoid off-topic discussions. Remember when you update an issue or respond to an email you are potentially sending to a large number of people. Please consider this before you update. Also remember that nobody likes spam.

#### Báo cáo lỗi

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Vấn đề bảo mật

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **Phát triển cộng đồng**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Vị trí Toàn thời gian

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



