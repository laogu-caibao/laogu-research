# 研报精读

`laogu-research`

研报精读 skill：输入研报全文/链接/标题或公司名，提炼核心逻辑、评级目标价、关键假设与风险，对比其他券商观点找出分歧点。

## 一键安装

```bash
npx skills add laogu-caibao/laogu-research
```

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-research`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-research.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-research/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-research/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-research/`（项目级用 `.trae/skills/laogu-research/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，纯流程描述）
- `references/sources.md` — 数据源：研报获取以网页搜索为主力，卖方研报无统一公开 API（诚实说明，不虚构接口）

## 输入方式

- 研报全文（粘贴文本）
- 研报链接
- 研报标题，或"公司名 + 研报"（如"宁德时代 研报"）——此时先搜索研报摘要再精读

## 输出结构

- 报告卡片：券商、报告日期、评级、目标价、估值方法、标的（公司名+代码）
- 核心逻辑（≤3 条，带关键数字）
- 关键假设（2-3 条）与风险提示（2-3 条，来自原文）
- 分歧点：与其他券商近期研报的评级/目标价/逻辑对比
- 一句话总结

## 关键规则

- 数字必须来自原文，不补不猜；目标价缺失明确标注"原文未披露目标价"，不估算
- 不做买卖推荐

---
## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。
