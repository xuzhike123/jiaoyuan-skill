<img width="5120" height="2116" alt="大海航行靠舵手" src="https://github.com/user-attachments/assets/a05a37c3-14d4-443e-8cf4-9d4eef8015d4" />
# 教员（jiaoyuan）— 毛泽东式认识论与工作方法

> **从实际出发，抓住主要矛盾，站在多数人一边，集中力量解决它，再用实践检验。**
> 这是一套可执行的方法，不是语录合集，也不是角色扮演。

---

## 它是什么

- 一套**分析问题**的流程：调查 → 抓主要矛盾 → 定战略 → 组织力量 → 检验修正。
- 一套**带团队**的方法：党委会工作法、群众路线、统一战线、整风复盘。
- 一份**人物侧写**：从诗词与画传里读出的性格、语气、意象。
- 一份**引语校准表**：哪些是原话、哪些是误引、哪些不能当原话用。

## 它不是什么

- 不冒充毛泽东本人，不伪造语录、落款、“最高指示”。
- 不用于政治煽动、人身攻击、给身边人贴“敌人”标签。
- 不预测股市、彩票、选举、战争胜负。
- 不把革命年代的“敌我/阶级斗争”套到家庭、同事、朋友关系上。
- 不为晚年错误（特别是文化大革命）辩护。

---

## 安装

本仓库的 skill 目录可以直接复制到 DeepSeek Harness 的用户 skill 目录：

```powershell
# Windows PowerShell
Copy-Item -Recurse -Force .\jiaoyuan-skill "$env:USERPROFILE\.dsh\skills\jiaoyuan"
```

安装后新建会话（或在技能列表刷新后）即可在 `~/.dsh/skills` 下看到 `jiaoyuan`。
`SKILL.md` 的 frontmatter 已包含触发描述，agent 会在相关任务中自动加载。

> 目录名建议用 `jiaoyuan`（与 frontmatter 的 `name` 一致）。不要装到 `sources/`、`tools/` 等开发目录。

---

## 怎么用

直接用自然语言，不需要背命令：

- **诊断**：“我们增长停滞，三个部门互相甩锅，帮我拿个方案。”
- **讲授**：“讲讲《矛盾论》里的主要矛盾，举一个现代例子。”
- **拟作**：“用教员的语气写一段 Q4 动员，300 字。”
- **查证**：“‘没有调查，没有发言权’出自哪篇？上下文是什么？”
- **读人**：“从《沁园春·雪》看，他是什么性格？”

agent 会先走“教员三问”，再按路由加载一张能力卡；拟作模式会明确标注“拟教员文风，非本人原作”。

---

## 结构

```
SKILL.md                    入口：三问、五步、路由、边界
README.md                   本文件
BUILD_MANIFEST.json         构建信息与文件校验
test-prompts.json           15 条触发/边界测试
references/
├── overview.md             来源、方法、结构、局限
├── persona.md              六组张力、诗心四母题、画传十二卷、阴影
├── voice.md                语体、句法、比喻库、段落模板、改写示例
├── quotes.md               62 条已核引语 + 常见误引
├── corpus-map.md           159 篇篇目地图（含 txt 行号）
├── glossary.md             术语表（原义→现代转译→误用）
├── cheatsheet.md           一页速查
├── capability-index.md     完整意图索引
└── capabilities/           11 张能力卡（R/I/A1/A2/E/B）
examples/
├── demo-diagnosis.md       诊断模式示例
└── demo-voice.md           拟作模式示例（已标注）
books/jiaoyuan/
├── BOOK_OVERVIEW.md        语料整体理解（Adler 四步）
├── DIGEST.md               精华长文
├── verified.md             三重验证记录
├── coverage-audit.md       覆盖审计
├── needs-review.md         待核与缺口
└── PIPELINE_STATE.md       流水线状态
```

---

## 来源与引用纪律

- 主要依据：《毛泽东选集》第一至四卷（人民出版社通行版）。
- 第五卷内容单独标注；静火、赤旗、草堂等汇编卷**不作原话引用**。
- 诗词以《毛泽东诗词集》为准；画传是后人编绘，只读人格原型，不当史实。
- 所有引语先查 `references/quotes.md`；不确定就写“大意是”。

语料来自 [M0rtzz/Selected-Works-of-MaoTseTung](https://github.com/M0rtzz/Selected-Works-of-MaoTseTung)，感谢整理者。

---

## 测试

`test-prompts.json` 含 15 条用例：11 条触发、4 条边界（冒充、攻击对手、预测股市、亲密关系套阶级分析）。
建议在接入后先跑一遍，重点看：

1. 是否加载了正确的能力卡；
2. 是否给出可执行动作与检验标准；
3. 是否在边界题上明确拒绝并转译。

---

## 声明

本 skill 是**方法论与人格的蒸馏**，用于分析、写作、教学与自我训练，不代表任何政治立场，也不构成对历史人物的全面评价。
历史评价以《关于建国以来党的若干历史问题的决议》为准。
