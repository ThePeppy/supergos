---
name: executing-plans
description: Use when you have a written implementation plan to execute in a separate session with review checkpoints
---

# Executing Plans

## Overview

Load plan, review critically, execute tasks in batches, report for review between batches.

**Core principle:** Batch execution with checkpoints for architect review.

**Announce at start:** "I'm using the executing-plans skill to implement this plan."

**⚠️ 开发过程中必须遵循 supergos:code 全局开发规范**

## The Process

### Step 0: 执行前检查（Pre-Execution Check）

**A. 任务连续性确认：**
1. 读取最后一次 git 提交描述，或近期与计划相关的提交记录
2. 判断上一个任务的完成情况
3. 若未找到相关提交记录（可能是上下文丢失）→ 执行代码 review 确认完成状态

**B. 设计方案对齐：**
1. Review 项目设计方案文件（`docs/plans/` 目录下的设计文档）
2. 确定当前计划应如何开发和设计
3. 确保实现方向与设计方案一致

### Step 1: Load and Review Plan
1. Read plan file
2. Review critically - identify any questions or concerns about the plan
3. If concerns: Raise them with your human partner before starting
4. If no concerns: Create TodoWrite and proceed

### Step 2: Execute Batch
**Default: First 3 tasks**

For each task:
1. Mark as in_progress
2. Follow each step exactly (plan has bite-sized steps)
3. **遵循 supergos:code 规范：**
   - 使用框架/库时 → 先调用 mcp:context-7 获取最新文档
   - 开发 UI 时 → 调用 ui/ux pro max 审查设计
   - 编写代码时 → 调用 code-simplifier 确保代码质量
4. Run verifications as specified
5. Mark as completed

### Step 3: Report
When batch complete:
- Show what was implemented
- Show verification output
- Say: "Ready for feedback."

### Step 4: Continue
Based on feedback:
- Apply changes if needed
- Execute next batch
- Repeat until complete

### Step 5: 设计符合性验证（Design Compliance Verification）

After all tasks complete and verified:

**A. 设计一致性检查：**
1. 再次 review 设计文档（`docs/plans/` 目录）
2. 对比实际实现功能与设计方案要求
3. 检查是否存在偏差或遗漏
4. 向用户展示实现与设计的对照结果

**B. 用户确认：**
1. 询问用户："实现是否符合设计预期？"
2. 根据用户反馈决定是否需要调整
3. 若用户确认符合预期 → 进入 Step 6

### Step 6: Complete Development

After user confirms implementation meets design:
- Announce: "I'm using the finishing-a-development-branch skill to complete this work."
- **REQUIRED SUB-SKILL:** Use supergos:finishing-a-development-branch
- Follow that skill to verify tests, present options, execute choice

## When to Stop and Ask for Help

**STOP executing immediately when:**
- Hit a blocker mid-batch (missing dependency, test fails, instruction unclear)
- Plan has critical gaps preventing starting
- You don't understand an instruction
- Verification fails repeatedly

**Ask for clarification rather than guessing.**

## When to Revisit Earlier Steps

**Return to Review (Step 1) when:**
- Partner updates the plan based on your feedback
- Fundamental approach needs rethinking

**Don't force through blockers** - stop and ask.

## Remember
- **执行前检查** - 先确认上次任务完成情况和设计方案
- **遵循规范** - 开发过程中始终遵循 supergos:code 规范
- Review plan critically first
- Follow plan steps exactly
- Don't skip verifications
- Reference skills when plan says to
- Between batches: just report and wait
- Stop when blocked, don't guess
- **执行后验证** - 完成后 review 设计文档并询问用户确认
