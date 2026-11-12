# Verify Before Claim（先核实，再断言）

## 简介

一个用于防止 AI 幻觉的 Skill：在给出任何肯定性结论之前，强制先核实事实，并附上高可信度证据（如官方网址）。

## 适用场景

| 触发场景 |
|----------|
| 回答某产品/工具/接口/路径「能否做到某事、是否支持某操作」 |
| 断言某个功能、菜单、入口、加速项是否存在 |
| 用户指出此前给出过未经核实的错误结论时 |

## 核心规则

| # | 规则 | 说明 |
|---|------|------|
| 1 | 不确定就查，别猜 | 无法确认时明确说「不确定」，而非给出看似确定的答案 |
| 2 | 给证据 | 下肯定结论时必须附官方链接等可自证来源 |
| 3 | 区分「思路对」与「关键词错」 | 用户思路正确但搜错名字时，先给出核实过的标准入口名，不顺着错误关键词否定功能 |

## 使用

将本目录（含 `SKILL.md`）放入你所用 Agent 框架的 skills 目录，即可自动加载生效。

---

# Verify Before Claim

## About

A Skill that prevents AI hallucination: before giving any definitive conclusion, it forces fact-checking first and requires high-credibility evidence (e.g., official URLs).

## When to Use

| Scenario |
|----------|
| Answering whether a product/tool/API/path can do or support something |
| Asserting whether a feature, menu, entry, or accelerator exists |
| When the user points out a previously given unverified conclusion |

## Core Rules

| # | Rule | Description |
|---|------|-------------|
| 1 | When unsure, look it up — don't guess | Say "not sure" instead of a seemingly definitive answer |
| 2 | Provide evidence | Attach self-verifiable sources (e.g., official links) to any definitive conclusion |
| 3 | Distinguish "right idea" from "wrong keyword" | Give the verified standard entry name first — never echo a wrong keyword to deny the feature |

## Usage

Place this directory (containing `SKILL.md`) into the skills folder of the Agent framework you use, and it loads automatically.
