# 配置与事件查看

[English](CONFIG.md) · [返回游戏介绍](README.zh-CN.md)

这是 v0.2.3-playtest.4 的配置快照，供阅读、分析和交流创意，包含剧情剧透。游戏程序源码和运行工程不在这个仓库中。

| 路径 | 内容 |
| --- | --- |
| `config/events_vr/` | 正式基础事件包：注册表、JSON Schema、40 个事件与 96 个选择 |
| `config/registry/items.json` | 19 种现行物品的名称、价格、重量等定义 |
| `config/registry/legacy_items.json` | 旧存档兼容物品，不属于现行商店列表 |
| `config/shop_catalog.json` | 商店商品目录 |
| `config/balance.json` | 初始预算、日常消耗等平衡参数 |
| `config/registry/actions.json` | 动作配置 |
| `config/registry/world.json` | 世界实体与状态配置 |
| `config/registry/director.json` | 事件导演与投放配置 |

## 使用 Event Graph Reviewer

我另一个项目 [Event Graph Reviewer](https://github.com/AmethystineAlpaca/event-graph-reviewer) 能在本地把事件与选项的显式前置关系可视化。需要 Python 3.9+、Node.js 20+、npm 和浏览器；普通试玩不需要这些工具。

在同一个父目录下执行：

```bash
git clone https://github.com/AmethystineAlpaca/z-shelter-public.git
git clone https://github.com/AmethystineAlpaca/event-graph-reviewer.git
cd event-graph-reviewer
./scripts/dev.sh ../z-shelter-public/config/events_vr
```

首次启动会安装查看器的 npm 依赖。打开终端打印的 localhost 地址，保持终端运行；Ctrl+C 退出。可按事件 ID 或标题搜索，点击节点查看条件、效果及相邻关系。修改本地事件 JSON 后需停止并重新运行命令。

查看器只加载注册表中列出的事件。它展示显式剧情前置条件，不会模拟随机投放、延迟排程、世界状态、资源事务或实际游戏平衡。物品等配置可直接阅读 JSON，不会在事件查看器里生成独立的物品图。

当前下载版不支持从这个仓库热加载配置。修改这里的文件不会改变已安装的游戏；集成修改需要开发者在私有工程中验证并重新导出。

欢迎通过 Issues 分享想法、事件 ID 或图中发现的问题。公开可读不代表授予开源或商用授权，具体见 [权利说明](RIGHTS.md)。
