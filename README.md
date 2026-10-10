# Analyze Business Plan · BP 解读与投资分析

面向创业公司商业计划书、融资材料和路演 PDF 的 Codex skill，以风险投资视角输出有来源、有证据分层的 Markdown 投资分析报告。

## 分析内容

- 锁定 BP 版本，检查不同页面的数字、口径与预测是否一致。
- 区分公司披露、外部验证、分析推断、反证与待尽调事项。
- 按目标市场与使用场景分析市场规模、竞争格局及竞争者时间线。
- 核验技术领先性、创始人履历、法律主体及知识产权关系。
- 分销售、租赁、按次收费、RaaS 等模式重建单位经济与客户 ROI。
- 压力测试商业化预测、融资需求与资金用途，生成能改变投资结论的尽调问题。

## 安装

将本仓库下载或克隆为 `analyze-business-plan` 文件夹，放入你配置的 Codex skills 目录，保留完整目录结构。

安装后的结构应为：

```text
<skills-directory>/analyze-business-plan/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── bp-report-template.md
└── references/
    ├── analysis-framework.md
    └── due-diligence-questions.md
```

## 使用

向 Codex 提供 BP 文件或可访问的资料，并明确调用：

```text
使用 $analyze-business-plan 分析这份 BP：核查内部矛盾，按目标市场验证竞争，
重建单位经济与客户 ROI，核验技术、团队及主体，输出带来源链接的投资报告和尽调问题。
```

默认交付 `report.md`。分析时需要读取完整材料，并具备外部资料检索能力；PDF 或幻灯片类材料还需要可用的解析和渲染能力，主指令会要求使用 PDF skill。

## 文件说明

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 核心工作流、证据规则与交付要求 |
| [agents/openai.yaml](agents/openai.yaml) | 界面名称、简介与默认提示词 |
| [assets/bp-report-template.md](assets/bp-report-template.md) | 中文投资报告模板 |
| [references/analysis-framework.md](references/analysis-framework.md) | 市场、竞争、技术、团队、商业化与融资分析框架 |
| [references/due-diligence-questions.md](references/due-diligence-questions.md) | 针对公司事实与证据缺口设计尽调问题的方法 |

缺少数据时，报告保留不确定性，并将分析假设与公司实际表现分开标注。
