# Verify Before Claim（先核实，再断言）

## 简介

一份防止 AI 幻觉的规则文件：在给出"能不能做 / 有没有 / 是否可行"这类结论前，强制先核实、亲测，没有把握时默认回答"不确定"，杜绝"事实不行却仍说可行"的幻觉。

## 文件说明

| 文件 | 说明 |
|------|------|
| `中文版/AGENTS.md` | 中文版规则 |
| `English/AGENTS.md` | 英文版规则 |

## 安装方法

`AGENTS.md` 是跨厂商通用格式，Codex、Claude Code、DSH、Cursor、Copilot 等均会读取。

**方式一：拖入聊天窗口（推荐）**

打开 `中文版/` 或 `English/` 文件夹，把里面的 `AGENTS.md` 直接拖进所用 Agent 的聊天窗口，它会自动安装到项目目录。

**方式二：手动放入项目根目录**

把 `AGENTS.md` 复制到项目根目录，Agent 启动时会自动加载。

**方式三：全局生效（Codex）**

放到 `~/.codex/AGENTS.md`，对所有项目生效。

> 注意：文件名必须是 `AGENTS.md`（精确大小写）。拖入后建议让 Agent 概括一次已加载的规则，确认已生效。

## 核心规则

| # | 规则 | 说明 |
|---|------|------|
| 1 | 没亲测就没结论 | 无亲手验证或可靠证据时，默认回答"不确定"，绝不说"可行/有效" |
| 2 | 存在 ≠ 有效 | "官方说有这功能"不等于"能解决你的问题"，不能混为一谈 |
| 3 | 证据要分级 | 官方 > 权威第三方 > 个人博客；二手来源必须标注"未找到官方确认" |

---

# Verify Before Claim

## About

A rules file that prevents AI hallucination: before giving any "can it / does it exist / is it feasible" conclusion, it forces verification and hands-on testing, and defaults to "not sure" when unverified — eliminating the "actually doesn't work, yet claimed to work" hallucination.

## Files

| File | Description |
|------|-------------|
| `中文版/AGENTS.md` | Chinese version |
| `English/AGENTS.md` | English version |

## Installation

`AGENTS.md` is a cross-vendor format read by Codex, Claude Code, DSH, Cursor, Copilot and more.

**Method 1: Drag into the chat window (recommended)**

Open the `中文版/` or `English/` folder, then drag the `AGENTS.md` inside it directly into the chat window of the Agent you use; it will be installed into the project directory automatically.

**Method 2: Place in the project root manually**

Copy `AGENTS.md` to the project root; the Agent loads it automatically at startup.

**Method 3: Global (Codex)**

Put it at `~/.codex/AGENTS.md` to apply to all projects.

> Note: the filename must be `AGENTS.md` (exact case). After installing, ask the Agent to summarize the loaded rules to confirm it took effect.

## Core Rules

| # | Rule | Description |
|---|------|-------------|
| 1 | No test, no conclusion | Without hands-on verification or reliable evidence, default to "not sure" — never say "it works" |
| 2 | Existence ≠ effectiveness | "Official source says the feature exists" ≠ "it solves your problem" — don't conflate them |
| 3 | Grade the evidence | Official > authoritative third-party > personal blog; second-hand sources must be labeled "no official confirmation found" |
