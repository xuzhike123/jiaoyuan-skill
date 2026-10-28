# PIPELINE_STATE

- **bundle**: `bundle.jiaoyuan`
- **version**: 1.0
- **updated**: 2026-10-28
- **mode**: single（单入口 + 11 张能力卡）
- **source**: `https://github.com/M0rtzz/Selected-Works-of-MaoTseTung`

## 阶段状态

| 阶段 | 状态 | 产出 |
|---|---|---|
| 0 整体理解（Adler） | ✅ 完成 | `BOOK_OVERVIEW.md` |
| 1 并行提取（框架/原则/案例/反例/术语） | ✅ 完成 | `references/capabilities/*`、`glossary.md` |
| 1.5 三重验证 | ✅ 完成 | `verified.md` |
| 1.6 晋级门 | ✅ 完成 | `coverage-audit.md`（11 晋级 / 1 降级 / 4 淘汰或参考） |
| 2 RIA++ 能力卡 | ✅ 完成 | 11 张卡（R/I/A1/A2/E/B） |
| 3 Zettelkasten 链接 | ✅ 完成 | `capability-index.md`、`SKILL.md` 路由表、`glossary.md` 互链 |
| 4 压力测试 | 🟡 初版 | `test-prompts.json`（15 条，待跑） |
| 5 编译与交付 | ✅ 完成 | `SKILL.md`、`references/`、`README.md`、`BUILD_MANIFEST.json` |

## 语料统计

- 《毛泽东选集》txt：约 201 万字符，目录 159 条（1–4 卷）。
- 诗词：约 2.5 万字符（30 首）；“品读”约 5 万字符（更全，用于校读）。
- 画传：12 卷 PDF（未 OCR）。
- 早期文稿：约 27.6 万字符（背景）。

## 断点续跑

下一阶段从 **阶段 4（压力测试）** 继续：
1. 用 `test-prompts.json` 逐条跑，记录命中/越界。
2. 对未通过的卡回炉，更新 `verified.md`。
3. 补 `needs-review.md` 的 P0 项（诗词、卷次映射）。
