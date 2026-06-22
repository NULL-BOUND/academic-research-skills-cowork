# Academic Research Skills (ARS) — Cowork 移植版

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

[English](README.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md)

**Academic Research Skills (ARS)** 是一套全方位的 AI 輔助學術研究技能套件，涵蓋從文獻調研到論文發表的完整流程。

本專案是 [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills) 的 **Cowork 移植版**，原作者為臺灣開發者 Cheng-I Wu。

## 與原版的差異

| 特性 | 原版（Claude Code） | 本移植版（Cowork） |
|------|-------------------|-------------------|
| 平臺 | Claude Code CLI / VS Code / JetBrains | **Cowork 桌面應用** |
| 技能安裝 | 軟連結到 `.claude/skills/` | `save_skill` 寫入 SKILL.md |
| 檔案結構 | 多檔案（agents/ + references/ + templates/） | **單檔案內聯**（全部內容嵌入 SKILL.md） |
| 跨對話執行 | ✅ 依賴專案目錄 | ✅ 自包含，無外部依賴 |
| CLI 整合 | hooks, commands, scripts | 不適用（Cowork 無對應機制） |
| 版本 | v3.13.0 | v3.13.0（同步原版最新） |

> 倉庫保留了完整的原始檔案結構（agents/、references/、shared/、scripts/ 等）
> 供參考。SKILL.md 是自包含的內聯版本，針對 Cowork 優化。

## 已安裝技能

| 技能 | Agent | 模式 | 說明 |
|------|-------|------|------|
| `deep-research` | 13 | 8 種 | 深度研究、文獻回顧、系統性回顧、事實查核等 |
| `academic-paper` | 12 | 11 種 | 論文寫作、規劃、修訂、引用檢查、AI 揭露等 |
| `academic-paper-reviewer` | 7 | 4 種 | 同儕審查、重審、方法聚焦、校準 |
| `academic-pipeline` | 5 | 10 階段 | 研究→寫作→審稿→投稿全流程編排 |

## Cowork 安裝方法

```bash
# 安裝 deep-research
save_skill --name deep-research --file deep-research/SKILL.md

# 安裝 academic-paper
save_skill --name academic-paper --file academic-paper/SKILL.md

# 安裝 academic-paper-reviewer
save_skill --name academic-paper-reviewer --file academic-paper-reviewer/SKILL.md

# 安裝 academic-pipeline
save_skill --name academic-pipeline --file academic-pipeline/SKILL.md
```

## 使用方法

在 Cowork 中輸入 `/技能名` 啟動：

| 指令 | 功能 |
|------|------|
| `/deep-research` | 啟動深度研究 |
| `/academic-paper` | 啟動論文寫作 |
| `/academic-paper-reviewer` | 啟動同儕審查 |
| `/academic-pipeline` | 啟動全流程 |

## 致謝

- 原作者 **Cheng-I Wu**（[@Imbad0202](https://github.com/Imbad0202)）— ARS 設計開發
- 原倉庫：[Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)
- 許可證：CC BY-NC 4.0（非商業使用）
