<div align="center">

![R 土壤学科研绘图](docs/banner.svg)

# R 土壤学科研绘图

**按研究问题选图，把数据、代码与图形一起交付。**

![Agent Skills](https://img.shields.io/badge/Agent_Skills-compatible-925136?style=flat-square)
![版本](https://img.shields.io/badge/技能版本-v1-925136?style=flat-square)
![中文](https://img.shields.io/badge/说明-中文-925136?style=flat-square)
[![GitHub Release](https://img.shields.io/github/v/release/SoMic520/r-soil-scientific-figures?style=flat-square&label=下载&color=925136)](https://github.com/SoMic520/r-soil-scientific-figures/releases/latest)

[功能介绍](#能帮你做什么) · [安装步骤](#安装步骤) · [使用示例](#使用示例) · [技能规则](skills/r-soil-scientific-figures/SKILL.md) · [下载发布包](https://github.com/SoMic520/r-soil-scientific-figures/releases/latest)

</div>

## 这是什么

面向土壤、农业、生态、环境、水文、微生物组、遥感与空间研究，从数据结构和实验设计出发选择图形，再交付可运行的 R 代码与标准输入表。

这是给 AI 助手使用的 **Agent Skill（技能包）**，其中包含任务规则、参考资料和辅助脚本。安装到支持技能的工具后，可以在对话中用下面的示例调用。完成任务仍需工具可用的模型及运行环境。

## 能帮你做什么

| 任务 | 具体能力 |
| --- | --- |
| **按数据和问题选图** | 内置 314 种图形、29 个图族和 35 种输入规范，结合变量类型、实验设计和研究问题给出选择。 |
| **完成常见科研图** | 支持显著性箱线图与柱状图、深度剖面、网络、群落排序、空间分析、预测及多面板图。 |
| **复刻已有图形** | 从论文截图识别布局与视觉编码，用提供的数据重建，并核对尺寸、文字与标注位置。 |
| **保留可复现交付** | 默认提供无注释和中文详注 R 代码、标准输入表、矢量 PDF、600 dpi PNG / LZW TIFF 与中文图注。 |

## 开始前准备什么

- 原始数据与字段含义、真实单位
- 分组、重复、实验设计和统计要求
- 目标图型或参考截图、期刊尺寸要求

按任务范围，通常可以获得：

- 可独立运行的 R 代码与标准输入表
- PDF、PNG、TIFF 图形与中文图注
- 图形质量检查和复现所需说明

## 安装步骤

### 1. 准备工具

先准备 **Codex、Claude Code 或其他支持 Agent Skills 的 AI 工具**，以及 [GitHub CLI](https://cli.github.com/)。GitHub CLI 需支持 `gh skill` 命令（2.90.0 及以上；建议使用当前稳定版）。它用于下载技能。

- **Windows**：在 PowerShell 执行 `winget install --id GitHub.cli --exact`。
- **macOS**：从 [GitHub CLI 官方下载页](https://cli.github.com/) 获取安装包；已有 Homebrew 时可执行 `brew install gh`。

安装后，打开终端或 PowerShell 检查版本并登录：

```shell
gh --version
gh auth login
```

### 2. 安装到你使用的 AI 工具

以 **Codex** 为例，复制下面这一行到终端或 PowerShell 执行：

```shell
gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent codex --scope user
```

`--scope user` 表示安装到当前用户，供不同项目使用。使用其他工具时，选择对应命令：

| AI 工具 | 安装命令 |
| --- | --- |
| Codex | `gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent codex --scope user` |
| Claude Code | `gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent claude-code --scope user` |
| GitHub Copilot | `gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent github-copilot --scope user` |
| Gemini CLI | `gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent gemini-cli --scope user` |
| Cursor | `gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent cursor --scope user` |
| OpenCode | `gh skill install SoMic520/r-soil-scientific-figures r-soil-scientific-figures --agent opencode --scope user` |

安装前想先看看规则，可以执行：

```shell
gh skill preview SoMic520/r-soil-scientific-figures r-soil-scientific-figures
```

### 3. 在对话中使用

安装完成后，重新打开 AI 工具或开始新会话，提供你的材料，并明确写出 **“请使用 r-soil-scientific-figures……”**。从下面选一条示例，替换成你的实际任务即可。

## 使用示例

```text
请使用 r-soil-scientific-figures 分析附件数据的结构，结合土壤深度和处理分组推荐图型，并说明推荐依据。
```

```text
请使用 r-soil-scientific-figures 绘制分面柱状图并标注显著性。先确认统计设计，交付 R 代码、标准 Excel、PDF、PNG、TIFF 和中文图注。
```

```text
请使用 r-soil-scientific-figures 根据参考截图和附件数据重建图形，按我指定的最终物理尺寸调整字体、图例与标注。
```

## 使用范围

图型与统计方法需要匹配实际研究设计。生成图形需要可用的 R 环境及相应软件包；截图只提供视觉参考，真实数值以用户数据为准。

## 下载与更新

- [最新发布包](https://github.com/SoMic520/r-soil-scientific-figures/releases/latest)：适合下载、留存或按平台说明手动安装。
- [当前技能 ZIP](dist/r-soil-scientific-figures-skill-20260816-v1.zip) 与 [SHA-256 校验值](dist/SHA256SUMS.txt)：用于核对文件完整性。
- 更新已安装的技能：

```shell
gh skill update r-soil-scientific-figures
```

AI 工具与 GitHub CLI 会持续更新；命令差异请以当前工具帮助为准。`gh skill` 的安装与预览说明见 [GitHub CLI 官方文档](https://cli.github.com/manual/gh_skill)。

## 仓库结构

```text
skills/r-soil-scientific-figures/
  SKILL.md       技能入口与工作规则
  agents/        智能体配置
  references/    参考资料与任务规范
  scripts/       辅助脚本与校验工具
docs/banner.svg  仓库封面
dist/            技能发布包与 SHA-256 校验值
```

[阅读完整技能规则](skills/r-soil-scientific-figures/SKILL.md) · [查看专项参考资料](skills/r-soil-scientific-figures/references/figure-taxonomy.md) · [查看拆分记录](CHANGELOG.md)

## 其他 Hemusci 技能

| 独立仓库 | 用途 |
| --- | --- |
| [土壤科学与自然科学写作](https://github.com/SoMic520/soil-all-writing) | 从原始底稿到正式交付，让文字与证据对齐。 |
| [土壤学期刊投稿格式审查](https://github.com/SoMic520/soil-journal-format-review) | 依照期刊官方规则，逐项检查投稿文件。 |
| [土壤试验方法顾问](https://github.com/SoMic520/soil-methods-consultant) | 从测量对象出发，找到有出处的实验方法。 |
| [土壤三普专业报告](https://github.com/SoMic520/soil-third-survey-report) | 对齐省、市、县成果层级，整理可送审的专业报告。 |

[返回 Hemusci 技能总目录](https://github.com/SoMic520/Hemusci-Skills) · [Hemusci 网站](https://hemusci.com/skills/)

---

此仓库于 2026-10-02 从 [Hemusci-Skills](https://github.com/SoMic520/Hemusci-Skills/tree/c41529fe9fe6833ff65679133dfed24ea4d4b61c/skills/r-soil-scientific-figures) 拆分，保留该技能的提交历史、规则与资料。原集合继续保留兼容安装入口。

**使用与许可**：沿用原仓库的许可状态，目前未设置开源许可证；公开可见不等同于授予再发布许可。参考资料、标准及第三方内容的权利归其各自权利人。有关复制、修改、传播或再发布的授权，请联系仓库所有者。
