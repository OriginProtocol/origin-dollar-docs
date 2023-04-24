# Đóng góp

**100% Mã nguồn mở**

OUSD là dự án mã nguồn mở hoàn toàn và chúng tôi hoan nghênh mọi đóng góp của toàn thể cộng đồng. Bạn có thể hỗ trợ đội ngũ chúng tôi bằng việc báo cáo sự cố bảo mật, đóng góp lập trình hay giúp chúng tôi cải thiện cộng đồng của mình.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

We work in public and our company Discord is open to all. If you have questions or need help getting started, our [Discord OUSD channels](https://discord.gg/jyxpUSe) are the best place to get assistance from our team and community.

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies. Various other developer tools can be found at [ousd.com/dashboard](https://ousd.com/dashboard).

#### Quá trình phát triển

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. Tìm một vấn đề thú vị và trao đổi với chúng tôi! Vui lòng ghé kênh `#engineering` [Discord](https://discord.gg/jyxpUSe) và cho chúng tôi biết bạn muốn làm gì.
2. Nhắn tin cho [thành viên của team](https://github.com/orgs/OriginProtocol/teams/core/members) trên Discord và yêu cầu được thêm vào nhóm [cộng tác viên](https://github.com/orgs/OriginProtocol/teams/contributors) của chúng tôi. Nếu không, bạn sẽ cần phải folk kho giữ liệu code (repo) liên quan và đẩy các nhánh tính năng vào folk riêng của bạn.
3. Thêm nhận xét về vấn đề hoặc tự phân bổ cho bản thân tránh tình trạng nhiều cộng tác viên cùng xử lý 1 nhiệm vụ.
4. Bắt đầu với nhánh `chính` và kiểm tra nhánh tính năng mới trừ khi bạn đang đóng góp vào một tính năng hiện có.
5. Viết code.
6. Kéo các cam kết mới nhất từ `nhánh chính` và xác nhận rằng mã lập trình của bạn hoạt động tốt với với bất kỳ công việc nào đã được tích hợp kể từ khi bạn bắt đầu.
7. Push your branch to the upstream repository (i.e. https://github.com/OriginProtocol/\[repo]) so that other contributors can easily work off of it if necessary.
8. Vui lòng yêu cầu đánh giá trong bài PR bằng cách nhấp vào biểu tượng bánh răng bên cạnh “Người đánh giá” ở cột bên phải.

For critical smart contract code to be merged it must pass the following checklist:

*  Code được kiểm tra bởi 2 người đánh giá
*  Vươt qua bài kiểm tra unit
*  Vượt qua Slither không bị cảnh báo
*  Vượt qua kiểm tra Echidna

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### Kiểu lập trình

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io).

For Solidity, we use two-space indents.

#### Thiết kế giao thức

When considering protocol or implementation design proposals, we are looking for:

* Mô tả vấn đề mà bản đề xuất này sẽ giải quyết
* Thảo luận về những đánh đổi liên quan
* Xem xét các giải pháp hiện có khác
* Links to relevant literature (RFCs, papers, etc)
* Thảo luận về giải pháp đề xuất

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### Hỗ trợ cộng đồng

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* Thái độ tốt: Lịch sự, tôn trọng với các thành viên trong cộng đồng: không phân biệt vùng miền, chủng tộc, giới tính hoặc các hành vi tương tự. Chúng tôi thích những người tử tế hơn những người xấu tính!
* Thái độ hoan nghênh: Làm cho mọi người trong cộng đồng của chúng tôi cảm thấy được chào đón không phân biệt tiểu sử và mức độ đóng góp của họ, làm mọi cách có thể để khuyến khích sự gắn kết của cộng đồng.
* Tuân thủ pháp luật: Về cơ bản, không để bất kỳ ai gặp rắc rối. Chỉ chia sẻ nội dung mà bạn sở hữu, không chia sẻ thông tin riêng tư hoặc thông tin nhạy cảm và không vi phạm pháp luật.
* Duy trì đúng chủ đề: Đảm bảo rằng nội dung được đăng lên các kênh 1 cách phù hợp, tránh gây thảo luận lạc đề. Hãy nhớ khi bạn cập nhật một vấn đề hoặc trả lời email mà bạn có khả năng gửi cho một số lượng lớn người nhận. Vui lòng kiểm tra thật kỹ trước khi thực hiện. Cần lưu ý rằng không ai thích bị làm phiền cả.

#### Báo cáo lỗi

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### Vấn đề bảo mật

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% content-ref url="../security-and-risks/bug-bounties.md" %}
[bug-bounties.md](../security-and-risks/bug-bounties.md)
{% endcontent-ref %}

#### **Phát triển cộng đồng**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `discussion` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### Vị trí Toàn thời gian

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full-time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).

