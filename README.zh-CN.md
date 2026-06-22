# Academic Research Skills (ARS) — Cowork 移植版

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

[English](README.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md)

**Academic Research Skills (ARS)** 是一个面向学术研究的全套 AI 辅助技能套件，覆盖从文献调研到论文发表的完整流程。

本项目是 [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) 的 **Cowork 移植版**，原作者为台湾开发者 Cheng-I Wu。

## 与原版的区别

| 特性 | 原版（Claude Code） | 本移植版（Cowork） |
|------|-------------------|-------------------|
| 平台 | Claude Code CLI / VS Code / JetBrains | **Cowork 桌面应用** |
| 技能安装 | 软链接到 `.claude/skills/` | `save_skill` 写入 SKILL.md |
| 文件结构 | 多文件（agents/ + references/ + templates/） | **单文件内联**（全部内容嵌入 SKILL.md） |
| 跨对话运行 | ✅ 依赖项目目录 | ✅ 自包含，无外部依赖 |
| CLI 集成 | hooks, commands, scripts | 不适用（Cowork 无对应机制） |
| 版本 | v3.13.0 | v3.13.0（同步原版最新） |

> 仓库保留了完整的原始文件结构（agents/、references/、shared/、scripts/ 等）
> 供参考。SKILL.md 是自包含的内联版本，针对 Cowork 优化。

## 已安装技能

| 技能 | Agent | 模式 | 说明 |
|------|-------|------|------|
| `deep-research` | 13 | 8 种 | 深度研究、文献综述、系统综述、事实核查等 |
| `academic-paper` | 12 | 11 种 | 论文写作、规划、修订、引用检查、AI 披露等 |
| `academic-paper-reviewer` | 7 | 4 种 | 同行评审、重审、方法聚焦、校准 |
| `academic-pipeline` | 5 | 10 阶段 | 研究→写作→审稿→投稿全流程编排 |

## Cowork 安装方法

```bash
# 安装 deep-research
save_skill --name deep-research --file deep-research/SKILL.md

# 安装 academic-paper
save_skill --name academic-paper --file academic-paper/SKILL.md

# 安装 academic-paper-reviewer
save_skill --name academic-paper-reviewer --file academic-paper-reviewer/SKILL.md

# 安装 academic-pipeline
save_skill --name academic-pipeline --file academic-pipeline/SKILL.md
```

## 使用方法

在 Cowork 中输入 `/技能名` 启动：

| 命令 | 功能 |
|------|------|
| `/deep-research` | 启动深度研究 |
| `/academic-paper` | 启动论文写作 |
| `/academic-paper-reviewer` | 启动同行评审 |
| `/academic-pipeline` | 启动全流程 |

## 致谢

- 原作者 **Cheng-I Wu** ([@Imbad0202](https://github.com/Imbad0202)) — ARS 设计开发
- 原仓库: [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)
- 许可证: CC BY-NC 4.0（非商业使用）
