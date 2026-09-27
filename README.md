# AitkRadar 存证链镜像（evidence）

主仓 `jyo-xu/aitkradar` 的抓取证据记录（G8 合规形态：纯文本片段 + 元数据 + 整页哈希，**不含整页 HTML**）。

- 目录结构：`{YYYY-MM-DD}/{snapshot_id}.json`（snapshot_id = 整页 SHA256 前 16 位）
- 每次抓取由管道自动 commit；本仓历史 = 不可篡改的"我们当时看到了什么"证据链
- visibility=internal 的记录（空壳/非 JSON）只存证不上站
- 本仓独立于主代码仓（跨账号容灾：主仓在 jyo-xu，本仓在 echo77777-chen）
