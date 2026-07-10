# B2B Buyer Qualification — Agent Skill

[English](#english) · [中文](#中文)

A portable agent skill that helps export sellers, founders, and small trade teams research, verify, score, and prioritize overseas B2B buyers, importers, distributors, and trade leads **before** outreach or follow-up.

> Uses public or user-provided information only. This skill evaluates fit and priority — it does **not** accuse any company of fraud and is not a "dig up dirt" tool.

---

## English

### What it does
Turns a rough lead into a practical buyer brief: who they are, what they sell or buy, whether they match your offer, what risks exist, and what outreach angle to use next.

### Who it's for
- Export sales reps qualifying new prospects.
- Founders / small teams without a dedicated risk function.
- Anyone preparing for a trade show, RFQ, or sample discussion.

### Inputs
Minimal info only: company name, website/profile, country/market, your product category, known contact (optional), and your goal (outreach / verification / meeting prep / RFQ / prioritization).

### Output
A structured buyer brief: verdict (score + priority + one-line reason), company snapshot, evidence, fit analysis, risk check, recommended next action, and an outreach angle. For multiple leads, a ranked table first, then expansion of only the top or riskiest leads.

### Score rubric (100 points)

| Dimension | Weight |
|---|---:|
| Product fit | 25 |
| Channel & market fit | 20 |
| Order potential | 20 |
| Legitimacy confidence | 20 |
| Outreach readiness | 15 |

Bands: `80–100` Strong target · `65–79` Worth outreach · `50–64` Research more · `30–49` Low priority · `0–29` Avoid / verify carefully.

### Install

Pick one method:

```bash
# Clone into your project as a subfolder
git clone https://github.com/qpood/b2b-buyer-qualification.git skills
cp -r skills/agent-skills/ ./agent-skills/
rm -rf skills
```

```bash
# Clone and use directly (the repo is already a valid skill folder)
git clone https://github.com/qpood/b2b-buyer-qualification.git
```

```bash
# Download the folder only (no git history)
# Requires `gh` CLI: gh auth login, then:
gh repo clone qpood/b2b-buyer-qualification -- --depth=1
cp -r b2b-buyer-qualification/agent-skills/ ./agent-skills/
rm -rf b2b-buyer-qualification
```

```bash
# Copy-paste: download the ZIP, then unzip and keep agent-skills/
```

After installing, reference `SKILL.md` from your agent:
- **Codex**: load the `SKILL.md` before acting.
- **Claude Code**: reference it from `CLAUDE.md`, copy into a Claude skills setup, or open `SKILL.md` as context.
- **Cursor**: point Cursor rules / chat context at the folder.
- **Other agents**: read the narrowest matching skill first, then follow its steps.

See [`EXAMPLES.md`](agent-skills/business/b2b-buyer-qualification/EXAMPLES.md) for worked, fictional examples.

---

## 中文

### 这个 Skill 是做什么的
在外发开发信、报价或参展前，先研究、核验、打分、排序一个潜在 B2B 买家 / 进口商 / 分销商 / 批发商 / 零售商 / 采购代理，输出一份「买家简报」：他是谁、卖什么 / 买什么、跟你是否匹配、有哪些风险、下一步该怎么做。

### 适合谁用
- 外贸业务员 / 出口销售：开发新客户前先筛一遍。
- 创始人 / 小团队：没有专职风控，也能快速判断线索质量。
- 参展 / RFQ 跟进：参展前做功课，RFQ 回复前先做优先级。

### 输入什么
最少提供：买家公司名、官网或平台主页（如有）、国家 / 目标市场、你卖的产品类目、已知联系人（如有）、你的目标（开发 / 核验 / 会议准备 / RFQ 评审 / 优先级排序）。信息不足时，技能只会问最必要的部分，并明确标注「待确认」。

### 输出什么
一份结构化「买家简报」：结论（评分 / 优先级 / 一句话理由）、公司快照、证据、匹配分析、风险检查、推荐的下一步动作，以及首封开发信角度。多个买家时先出表格，再只展开重点。

### 评分量表（100 分）

| 维度 | 权重 |
|---|---:|
| 产品匹配 Product fit | 25 |
| 渠道与市场匹配 Channel & market fit | 20 |
| 订单潜力 Order potential | 20 |
| 身份可信度 Legitimacy confidence | 20 |
| 触达就绪 Outreach readiness | 15 |

区间：`80–100` 强匹配 · `65–79` 值得开发 · `50–64` 先研究 · `30–49` 低优先级 · `0–29` 暂缓 / 验证。

### 安装

任选一种：

```bash
# 克隆到项目子目录
git clone https://github.com/qpood/b2b-buyer-qualification.git skills
cp -r skills/agent-skills/ ./agent-skills/
rm -rf skills
```

```bash
# 直接克隆使用（仓库本身就是一个合法的 skill 文件夹）
git clone https://github.com/qpood/b2b-buyer-qualification.git
```

```bash
# 只下载文件夹（不带 git 历史）
# 需要 `gh` CLI：先 gh auth login，然后：
gh repo clone qpood/b2b-buyer-qualification -- --depth=1
cp -r b2b-buyer-qualification/agent-skills/ ./agent-skills/
rm -rf b2b-buyer-qualification
```

```bash
# 直接下载 ZIP：解压后保留 agent-skills/ 文件夹即可
```

### 怎么用
把 `agent-skills/business/b2b-buyer-qualification/` 整个文件夹复制到你的项目，然后在智能体里引用 `SKILL.md`：
- **Codex**：执行前加载 `SKILL.md`。
- **Claude Code**：从 `CLAUDE.md` 引用，或直接打开 `SKILL.md` 作为上下文。
- **Cursor**：把该文件夹指向 Cursor 的 rules / chat 上下文。

示例见 [`EXAMPLES.md`](agent-skills/business/b2b-buyer-qualification/EXAMPLES.md)。

### 为什么它不是「查黑料」
这个 Skill 不是去挖买家黑料或给人贴「骗子」标签。它做的是**基于公开信息评估匹配度与优先级**：业务是否对口、渠道是否合适、有没有规模信号、身份是否可信、现在能不能联系。对拿不准的地方，它用 `待确认 / 风险信号 / 需核验` 来标注，**不会在没有强证据时指控欺诈**。涉及合规、制裁、法务等问题，它只作为「建议找专业人士复核」的信号，不下最终结论。

---

## Safety & privacy
- Public or user-provided information only.
- No private personal data; no fabricated contacts, shipments, certifications, or financials.
- Legal, sanctions, and compliance issues are signals for professional review, not final conclusions.
- For controlled / restricted / dual-use / medical / chemical goods, do a compliance check before outreach or quotation.

## License
[MIT](LICENSE).
