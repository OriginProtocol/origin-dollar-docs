# 時間鎖

{% hint style="danger" %}
確保一切正常運作後，時間鎖將很快的被添加。 在此之前，所有合約將由 Origin 的 5 of 8 多簽錢包管理。 如果發現任何關鍵問題的話，這允許問題的迅速處理。
{% endhint %}

在執行 OUSD 合同的任何更改之前，時間鎖合約會強制執行 48 小時的等待期。 該時間鎖可通過我們的多簽被調用，並且是我們的 [ERC-20](erc-20.md)、 [保險庫](vault.md) ，和 [策略](strategies.md) 合約的主人。 如果 OUSD 的管理員變得惡意，受到威脅或做出用戶不喜歡的更改，則延時的管理員操作將給用戶機會退出 OUSD。

{% hint style="info" %}
時間鎖是一項安全措施，如果 OUSD 持有者反對協議的任何擬議升級，則可以使用這 48 小時的時間提取資金。
{% endhint %}

OUSD 使用的時間鎖是 [Composite Timelock](https://compound.finance/docs/governance) 的略微修改版本，該版本已[由OpenZeppelin進行了審核](https://blog.openzeppelin.com/compound-finance-patch-audit/)。 3個顯著差異是：

1. OUSD 最初將使用比 Compound（72小時）更短的等待時間（48小時），以便在發現任何問題時更快地做出響應。
2. 48 小時過後，任何人都可以自由執行更改，而不僅僅是合約的主人。
3. 存款（不包括取款或轉賬）可以立即被凍結，而無需等待 48 小時的等待時間。 這是在發現關鍵漏洞的情況下。





