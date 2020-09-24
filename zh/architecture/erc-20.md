# 概觀

![](../.gitbook/assets/ousd_docs_graphics_3.png)

OUSD 由一系列智能合約組成。 每一個合約都被包在可以通過治理協議升級的代理合約中。

在內部，每個持有者池中的所有權百分比是用積分系統來跟踪。 在查看餘額或啟動錢包之間的轉賬時由 ERC-20 合約處理轉換為美元的條款。

保險庫（The Vault）負責鑄造（minting）和燃燒（burning）OUSD。 它也會強制部署到每個受支持的 [策略](../core-concepts/supported-strategies/)的資產百分比。 為了優化gas成本，保險庫保留了一個緩衝區以允許大多數存款和贖回都可以在無需從策略中存入/清算資產的情況下發生。



