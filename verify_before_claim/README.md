# Verify Before Claim

> 回答「能不能 / 有没有 / 可行吗」之前，先核实；没有证据，就没有结论。

[![Format](https://img.shields.io/badge/format-AGENTS.md-ff69b4.svg)](https://agents.md/)

一份防 AI 幻觉的规则文件。核心行为：**缺乏实测或可靠证据时，默认回答「不确定」，不给出「能 / 可行 / 有效」的肯定结论。**

---

## 目录

- [快速开始](#快速开始)
- [文件说明](#文件说明)
- [支持的工具](#支持的工具)
- [需要额外配置的工具](#需要额外配置的工具)
- [文件名规则](#文件名规则)
- [自检](#自检)
- [规则正文](#规则正文)
- [边界与免责声明](#边界与免责声明)

---

## 快速开始

1. 打开 `Chinese/` 或 `English/`
2. 把其中的 `AGENTS.md` 复制到项目根目录
3. 文件名保持 `AGENTS.md`

无需安装、无需配置、无需插件。

## 文件说明

| 文件 | 用途 |
|------|------|
| `Chinese/AGENTS.md` | 中文规则 |
| `English/AGENTS.md` | 英文规则 |

两个版本内容等价。

## 支持的工具

`AGENTS.md` 是跨厂商通用格式，据 [agents.md 官方清单](https://agents.md/)：

`Codex · Cursor · GitHub Copilot · VS Code · Gemini CLI · Aider · Windsurf · Zed · Jules · Devin · Amp · Factory · Roo Code · OpenCode · Goose · Kilo Code · Warp · Augment · Junie · UiPath · Semgrep · Ona`

## 需要额外配置的工具

以下工具不直接读取 `AGENTS.md`，需要额外配置。相关配置方法未经实测，此处仅作提示，具体以各工具官方文档为准：

| 工具 | 说明 |
|------|------|
| **Claude Code** | 默认优先读取 `CLAUDE.md` |
| **Gemini CLI** | 默认读取 `GEMINI.md` |
| **Aider** | 需显式声明才读取 `AGENTS.md` |

## 文件名规则

加载依赖文件名的精确匹配，与内容无关。文件名不符会静默失效——不报错，只是不生效。

## 自检

规则带执行标记，生效时回复开头会出现：

```
【【【 Verify Before Claim 已执行 】】】
```

1. 新开一个会话
2. 首轮问一个「能不能」问题
3. 无标记 → 路径或文件名有误；有标记但回答仍不严谨 → 属于遵守问题，而非加载问题

## 规则正文

| # | 规则 |
|---|------|
| 1 | **无实测即无结论**：缺乏实测或可靠证据时，默认「不确定」 |
| 2 | **存在 ≠ 有效**：官方记载存在，不等于能解决问题 |
| 3 | **证据分级**：官方 > 权威第三方 > 个人博客；二手来源标注「未找到官方确认」 |

## 边界与免责声明

- 不保证 100% 生效，加载、触发、遵守三层都可能失手。
- 注入成功不等于一定遵守，这是提示词层面的约束，非硬校验。
- 本文档基于公开信息整理，未经逐项实测，各工具支持情况可能随版本变化。

---

# Verify Before Claim

> Before answering "can it / does it exist / is it feasible", verify first. No evidence, no conclusion.

[![Format](https://img.shields.io/badge/format-AGENTS.md-ff69b4.svg)](https://agents.md/)

A rules file that prevents AI hallucination. Core behavior: **without hands-on testing or reliable evidence, the default answer is "not sure" — no definitive "it works / it's feasible / it's effective" conclusion.**

---

## Table of Contents

- [Quick Start](#quick-start)
- [Files](#files)
- [Supported Tools](#supported-tools)
- [Tools That Need Extra Configuration](#tools-that-need-extra-configuration)
- [Filename Rule](#filename-rule)
- [Self-Check](#self-check)
- [Core Rules](#core-rules)
- [Limits & Disclaimer](#limits--disclaimer)

---

## Quick Start

1. Open `Chinese/` or `English/`
2. Copy the `AGENTS.md` inside into the project root
3. Keep the filename `AGENTS.md`

No install, no config, no plugin.

## Files

| File | Purpose |
|------|---------|
| `Chinese/AGENTS.md` | Chinese rules |
| `English/AGENTS.md` | English rules |

Both versions are equivalent.

## Supported Tools

`AGENTS.md` is a cross-vendor format, per the [agents.md official list](https://agents.md/):

`Codex · Cursor · GitHub Copilot · VS Code · Gemini CLI · Aider · Windsurf · Zed · Jules · Devin · Amp · Factory · Roo Code · OpenCode · Goose · Kilo Code · Warp · Augment · Junie · UiPath · Semgrep · Ona`

## Tools That Need Extra Configuration

These tools do not read `AGENTS.md` directly and need extra configuration. The config methods are untested; this section only flags the difference — see each tool's official docs:

| Tool | Note |
|------|------|
| **Claude Code** | Reads `CLAUDE.md` first by default |
| **Gemini CLI** | Reads `GEMINI.md` by default |
| **Aider** | Needs an explicit declaration to read `AGENTS.md` |

## Filename Rule

Discovery is filename-exact, not content-based. A mismatched filename fails silently — no error, just no effect.

## Self-Check

The rule carries an execution marker; when it fires, the reply begins with:

```
[[[ Verify Before Claim executed ]]]
```

1. Open a new session
2. Ask a "can it" question on the first turn
3. No marker → wrong path or filename. Marker present but the answer is loose → a compliance problem, not a loading problem

## Core Rules

| # | Rule |
|---|------|
| 1 | **No test, no conclusion**: without testing or reliable evidence, default to "not sure" |
| 2 | **Existence ≠ effectiveness**: documented existence is not a solved problem |
| 3 | **Grade the evidence**: official > authoritative third-party > personal blog; second-hand sources labeled "no official confirmation found" |

## Limits & Disclaimer

- No 100% guarantee; loading, triggering, and compliance can each fail.
- Injected is not the same as obeyed; this is a prompt-level constraint, not a hard check.
- This document is based on public information, not item-by-item testing; tool support may change across versions.
