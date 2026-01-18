---
name: brainstorming
description: "You MUST use this before any creative work - creating features, building components, adding functionality, or modifying behavior. Explores user intent, requirements and design before implementation."
---

# Brainstorming Ideas Into Designs

## Overview

Help turn ideas into fully formed designs and specs through natural collaborative dialogue.

Start by understanding the current project context, then ask questions one at a time to refine the idea. Once you understand what you're building, present the design in small sections (200-300 words), checking after each section whether it looks right so far.

**⚠️ 设计阶段必须遵循 supergos:code 全局开发规范**

## The Process

**Understanding the idea:**
- Check out the current project state first (files, docs, recent commits)
- Ask questions one at a time to refine the idea
- Prefer multiple choice questions when possible, but open-ended is fine too
- Only one question per message - if a topic needs more exploration, break it into multiple questions
- Focus on understanding: purpose, constraints, success criteria

**Exploring approaches:**
- Propose 2-3 different approaches with trade-offs
- Present options conversationally with your recommendation and reasoning
- Lead with your recommended option and explain why
- **涉及技术选型时：** 调用 mcp:context-7 获取框架/库的最新文档和版本信息

**Presenting the design:**
- Once you believe you understand what you're building, present the design
- Break it into sections of 200-300 words
- Ask after each section whether it looks right so far
- Cover: architecture, components, data flow, error handling, testing
- Be ready to go back and clarify if something doesn't make sense
- **涉及界面设计时：** 调用 ui/ux pro max 确保设计美感和用户体验
- **涉及代码架构时：** 调用 code-simplifier 确保架构清晰可维护

## After the Design

**Documentation:**
- Write the validated design to `docs/plans/YYYY-MM-DD-<topic>-design.md`
- Use elements-of-style:writing-clearly-and-concisely skill if available
- Commit the design document to git

**Implementation (if continuing):**
- Ask: "Ready to set up for implementation?"
- Use superpowers:using-git-worktrees to create isolated workspace
- Use superpowers:writing-plans to create detailed implementation plan

## Key Principles

- **One question at a time** - Don't overwhelm with multiple questions
- **Multiple choice preferred** - Easier to answer than open-ended when possible
- **YAGNI ruthlessly** - Remove unnecessary features from all designs
- **Explore alternatives** - Always propose 2-3 approaches before settling
- **Incremental validation** - Present design in sections, validate each
- **Be flexible** - Go back and clarify when something doesn't make sense

## 开发规范遵循（supergos:code）

在设计阶段，必须遵循以下规范：

**技术选型时（mcp:context-7）：**
- 使用任何框架之前 → 调用 context-7 获取最新文档
- 使用任何第三方库之前 → 调用 context-7 获取最新版本和 API 文档
- 禁止在未获取最新文档前确定技术选型

**界面设计时（ui/ux pro max）：**
- 设计新界面方案时 → 调用 ui/ux pro max 获取设计建议
- 确保设计符合美学标准和用户体验要求

**代码架构设计时（code-simplifier）：**
- 设计代码架构时 → 调用 code-simplifier 规划清晰可维护的架构
- 确保架构设计不会导致：逻辑嵌套复杂、命名不一致、代码重复等问题
