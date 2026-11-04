# Drama Skills · short-drama-novel-analyze

> **[short-drama-novel-analyze](https://github.com/simlpandordinary/short-drama-novel-analyze)** —— 飞书《WorkBuddy 视频系列 · 全技能与提示词总目录》里推荐的开源技能，已拆分为独立仓库分发（一个技能一个仓库）。

| 项 | 内容 |
| - | - |
| 上游仓库 | <https://github.com/zenstory-ai/drama-skills> |
| 上游路径 | `skills/short-drama-novel-analyze` |
| 上游协议 | MIT |
| 上游 Star | 3.7k+ |
| 拆分方式 | 仅抽取该技能自身文件，独立可用 |

## 技能说明

把长篇小说、连载网文或多集散稿拆成可追溯的原著分析：章节索引、改编价值快评、逐章功能提取、剧情单元与节奏聚合、人物与设定归并，最后给出改编价值判定与分集候选，交给 $short-drama-develop 立契约。用户说“导入这本小说”“拆这本书”“分析原著”“这本书能不能改短剧”“先看看值不值得拆”“把长篇拆成分集候选”，或直接给出小说文件路径时使用。只做只读的结构化分析，不写剧本、不建资产、不生成媒体，也不替创作者决定改编方案。

## 目录结构

```
├── LICENSE
├── README.upstream.md
├── SKILL.md
├── scripts/
│   ├── novel_index.py
│   └── selftest.py
├── references/
│   ├── adaptation-triage.md
│   ├── adaptation-value.md
│   ├── aggregation-and-entities.md
│   ├── chapter-extraction.md
│   └── stage-contract.md
├── assets/
│   └── episode-candidate.example.jsonl
└── agents/
    └── openai.yaml
```

- `SKILL.md` 是技能入口（触发条件 / 工作流 / 约束），安装时必须位于技能根目录。
- `references/`、`scripts/`、`assets/` 为该技能自带的参考文档、脚本与素材。
- `README.upstream.md` 为上游仓库原始说明，保留出处与版权信息。
- `LICENSE` 为上游许可证原件。

## 安装

WorkBuddy 技能目录为 `~/.workbuddy/skills/short-drama-novel-analyze/`：

```bash
git clone https://github.com/simlpandordinary/short-drama-novel-analyze.git ~/.workbuddy/skills/short-drama-novel-analyze
```

也可以直接对 AI 说：「把 <https://github.com/simlpandordinary/short-drama-novel-analyze> 装成 Skill」。

安装后用自然语言触发，例如「Drama Skills · short-drama-novel-analyze」「用 short-drama-novel-analyze 帮我处理这个任务」。

## 版权

原始作者与版权归上游仓库 `zenstory-ai/drama-skills` 所有。本仓库仅做独立分发与结构整理，未修改技能内容；商用请遵循上游许可证。
