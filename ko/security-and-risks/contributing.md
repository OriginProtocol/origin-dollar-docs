# 기여

**100% 오픈소스**

OUSD는 완전한 오픈 소스 프로젝트이며, 모든 종류의 기여를 환영합니다. 문제 보고, 코드 제공, 커뮤니티 개선 지원 등 다양한 방법으로 오리진을 도울 수 있습니다.

오리진은 공개적으로 일하고 있으며, 오리진의 업무 진행 방식은 디스코드(Discord) 상에서 모두에게 공개되어 있습니다. 만약, OUSD와 관련하여 질문이 있거나 시작하는 데 도움이 필요하다면 디스코드 상의 OUSD 채널이 우리 팀과 커뮤니티의 도움을 받을 수있는 가장 좋은 곳입니다.

**Developer Analytics**

Our internal developer dashboard is available at [analytics.ousd.com](https://analytics.ousd.com). The dashboard shows the current circulating supply, the assets under management in the vault, and the current allocations between each of the stablecoins and strategies.

#### 개발 과정

Our branching strategy is similar to [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/), but we do all of our development in the `master` branch and have a `stable` branch for code that has been released.

Your development flow should look like:

1. 흥미로운 문제를 찾아 소통을 시작합니다! `#engineering` [디스코드(Discord)](https://discord.gg/jyxpUSe) 채널에 작업 할 내용을 알려주십시오.
2. 디스코드에서 [핵심 팀원](https://github.com/orgs/OriginProtocol/teams/core/members) 명의 구성원을 핑하고 [기여자 팀](https://github.com/orgs/OriginProtocol/teams/contributors)추가되도록 요청하십시오. 그렇지 않으면 관련 저장소를 포크하고 기능 브랜치를 자신의 포크로 푸시해야합니다.
3. 문제에 댓글을 추가하거나 자체 할당하여 실수로 동일한 작업을 수행하는 여러 기여자가 없도록합니다.
4. `master` 브랜치로 시작하고 기존 기능에 기여하지 않는 한 새로운 기능 브랜치를 확인하십시오.
5. 적절한 [코딩 스타일](https://docs.originprotocol.com/guides/getting_started/contributing.html#contributing-email-coding-style) 을 따르며, 멋진 코드를 작성해주세요.
6. `마스터` 에서 최신 커밋을 가져와 코드가 시작된 이후 병합 된 다른 작업과 함께 작동하는지 확인합니다.
7. 브랜치를 업스트림 저장소 \ (예: https: //github.com/OriginProtocol/ \ [repo \] \)로 푸시하여 필요한 경우 다른 기여자가 쉽게 작업 할 수 있도록합니다.
8. 오른쪽 열의 "검토자(Reviewers)"옆에 있는 톱니 바퀴 아이콘을 클릭하여 PR에서 리뷰를 요청하십시오.

The `master` branch is locked so that only members of the [core team](https://github.com/orgs/OriginProtocol/teams/core) are able to merge your pull requests. Pull requests that are peer-reviewed by other trusted contributors will be fast-tracked and merged faster! Check in the `#engineering` Discord channel for appropriate reviewers.

#### 코딩 스타일

We use a variety of programming languages in our repositories. When contributing, please follow existing coding conventions and refer to the CONTRIBUTING.md file in the repository, if one exists.

For JavaScript, we use [NPM’s style](https://docs.npmjs.com/misc/coding-style), which is automatically enforced via [prettier](https://prettier.io/).

For Solidity, we use two-space indents.

#### 프로토콜 설계

When considering protocol or implementation design proposals, we are looking for:

* 이 설계 제안이 해결하는 문제에 대한 설명
* 관련된 장단점에 대한 논의
* 다른 기존 솔루션 검토
* 관련 문헌 링크 \ (RFC, 논문 등 \)
* 제안 된 솔루션에 대한 논의

Please note that protocol design is hard and meticulous work. You may need to review existing literature and think through generalized use cases.

#### 커뮤니티 가이드라인

We want to keep the Origin community awesome, growing and collaborative. We need your help to keep it that way. To help with this we’ve come up with some general guidelines for the community as a whole:

* 예의 바르게 행동 해주세요: 커뮤니티 구성원들에게 예의 바르고 정중하게 행동하고 구성원들을 존중해주세요. 지역, 인종, 성별 또는 기타 다양한 방식의 무례함과 학대는 용납되지 않습니다. 오리진은 좋은 사람을 비열한 사람보다 훨씬 더 좋아합니다!
* 다양성 및 참여 장려: 커뮤니티의 모든 사람이 자신의 배경과 기여도에 관계없이 환영받는 기분을 느끼게하고 커뮤니티 참여를 장려하기 위해 가능한 모든 일을 합니다.
* 합법적 유지: 기본적으로 아무도 문제를 일으키지 않길 원합니다. 자신이 소유한 콘텐츠만 공유할 것을 권장하며, 개인 정보 또는 민감한 정보를 공유하지 않도록 합니다. 또한, 정보와 관련된 법률을 위반하지 마세요.
* 주제 유지: 각 커뮤니티 채널의 성격에 맞는 대화를 지향합니다. 대화를 하기 전에 해당 메세지를 올바른 채널에 게시하고 있는지 확인하고, 주제에서 벗어난 토론은 지양해주세요. 문제를 업데이트하거나 이메일에 응답할 때 잠재적으로 많은 사람이 해당 글을 보게 된다는 것을 항상 염두 해주세요. 업데이트하기 전에 내용들을 검토해주세요. 또한 아무도 스팸을 좋아하지 않는다는 것을 기억하세요.

#### 문제 보고

If you find bugs, mistakes or inconsistencies in Origin’s code or documents, please let us know by filing a GitHub issue. No issue is too small. Help us fix our tpyos!

#### 보안 이슈

OUSD is still in early development, which means there may be problems with the protocol or in our implementations. We take security vulnerabilities very seriously. If you discover a security issue, please bring it to our attention right away!

If you find a security vulnerability please send your report privately to [security@originprotocol.com](mailto:security@originprotocol.com) or send an encrypted message to [@joshfraser on Keybase](https://keybase.io/joshfraser). Please DO NOT file a public issue. Be sure to review our guidelines for responsible disclosure and eligibility for bug bounties.

{% page-ref page="bug-bounties.md" %}

#### **커뮤니티 개선**

Origin is just as much about community as it is about our technology.

We need constant help in improving our documentation, building new tools to interface with our platform, spreading the word to new users, helping new users getting setup and much more.

Please get in touch if you would like to help out. Our `general` channel on [Discord](https://www.originprotocol.com/discord) is a great place to share ideas and volunteer to help.

#### 채용 포지션

Origin occasionally hires developers for part-time or full-time positions.

We have a strong preference for hiring people who have already started contributing to the project. If you want a full time position on our team, your best shot is to engage with our team and start contributing code. It is very unlikely that we would offer you a full-time position on our engineering team unless you’ve had at least a few pull requests merged.

If you are interested, check out [the Origin Protocol job listings](https://angel.co/originprotocol/jobs). If you’d like to help in other ways, please propose your ideas in [our Discord channel](https://www.originprotocol.com/discord).



