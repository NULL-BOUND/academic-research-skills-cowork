# Academic Research Skills (ARS) — Cowork Edition

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

[English](README.md) | [繁體中文](README.zh-TW.md) | [简体中文](README.zh-CN.md)

**Academic Research Skills (ARS)** is a comprehensive suite of AI-assisted skills for academic research, covering the entire pipeline from literature review to paper publication.

This project is a **Cowork port** of [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills), originally built for Claude Code CLI.

## Comparison with the Original

| Feature | Original (Claude Code) | This Port (Cowork) |
|---------|----------------------|-------------------|
| Platform | Claude Code CLI / VS Code / JetBrains | **Cowork Desktop App** |
| Skill install | Symlink to `.claude/skills/` | `save_skill` into single SKILL.md |
| File structure | Multi-file (agents/ + references/ + templates/) | **Single-file inline** (all content embedded into SKILL.md) |
| Cross-session | ✅ Depends on project dir | ✅ Self-contained, no external deps |
| CLI integration | hooks, commands, scripts | N/A (Cowork has no equivalent) |
| Version | v3.13.0 | v3.13.0 (synchronized with original) |

> The repository retains the complete original file structure (agents/, references/, shared/, scripts/, etc.)
> for reference. The SKILL.md files are self-contained inline versions optimized for Cowork.

## Skills Included

| Skill | Agents | Modes | Description |
|-------|--------|-------|-------------|
| `deep-research` | 13 | 8 | Deep research, literature review, systematic review, fact-check, Socratic dialogue |
| `academic-paper` | 12 | 11 | Paper writing, planning, revision, citation check, AI disclosure |
| `academic-paper-reviewer` | 7 | 4 | Peer review, re-review, methodology focus, calibration |
| `academic-pipeline` | 5 | 10 stages | Research → Write → Review → Submission orchestration |

## How to Install in Cowork

Each skill's `SKILL.md` is self-contained with all agent definitions and key references embedded inline. To install in Cowork:

```bash
# deep-research
save_skill --name deep-research --file deep-research/SKILL.md

# academic-paper
save_skill --name academic-paper --file academic-paper/SKILL.md

# academic-paper-reviewer
save_skill --name academic-paper-reviewer --file academic-paper-reviewer/SKILL.md

# academic-pipeline
save_skill --name academic-pipeline --file academic-pipeline/SKILL.md
```

## How to Use

Enter `/skill_name` in Cowork to launch:

| Command | Function |
|---------|----------|
| `/deep-research` | Start deep research |
| `/academic-paper` | Start paper writing |
| `/academic-paper-reviewer` | Start peer review |
| `/academic-pipeline` | Start full pipeline |

## Acknowledgements

- Original author **Cheng-I Wu** ([@Imbad0202](https://github.com/Imbad0202)) — creator of ARS
- Original repository: [Imbad0202/academic-research-skills](https://github.com/Imbad0202/academic-research-skills)
- License: CC BY-NC 4.0 (non-commercial)
