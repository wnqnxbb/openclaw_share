# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

OpenClaw 分享演示页面 — 一个纯前端单页 HTML 项目，用于展示 OpenClaw 产品介绍/分享内容。无构建工具、无包管理器，直接在浏览器中打开 HTML 文件即可预览。

## Architecture

- **单文件 HTML 架构**：每个版本为独立的自包含 HTML 文件（CSS + JS 内联），无外部依赖管理
- `openclaw-share.html` — 当前主版本
- `openclaw-share_v1.html` / `v2.html` / `v3.html` — 历史迭代版本
- `assets/` — 图片资源（logo、头像、图标等）

## Tech Stack

- 纯 HTML/CSS/JS，无框架
- Google Fonts: Manrope + Orbitron
- CSS 变量体系管理主题色、字号、间距
- Scroll-snap 实现全屏翻页
- IntersectionObserver 驱动入场动画

## Design Conventions

- 深色主题：主背景 `#050b14`，品牌红 `#ff3e57`，电光青 `#1de8ff`
- 页面布局优先"中轴居中 + 宽内容区"，避免大面积右侧留白
- 演示页使用较大的上下留白与模块间距，保证节奏舒展
- 文案优先逐句采样源内容，非必要不做改写

## Development

直接在浏览器中打开 `openclaw-share.html` 预览，无需任何构建步骤。

## Rules from AGENTS.md

- 回复使用中文，git commit 使用简体中文
- `.npm-cache` 不可提交到 git
- 编码前先描述方案并等待审批；需求模糊时先提问澄清
- 编码后列出可能出问题的地方并建议测试方案
- 修 bug 时先写复现测试，再修复直到测试通过
- 被纠正时在 AGENTS.md 添加新规则
- 开发量超过 3 个文件时必须使用 planning-with-files skill
