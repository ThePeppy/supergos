---
name: executing-plans
description: Use when you have a written implementation plan to execute in a separate session with review checkpoints
---

# Executing Plans

## Overview

Load plan, review critically, execute tasks in batches, report for review between batches.

**Core principle:** Batch execution with checkpoints for architect review.

**Announce at start:** "I'm using the executing-plans skill to implement this plan."

**⚠️ MUST follow supergos:code global development standards during development**

## The Process

### Step 0: Pre-Execution Check

**A. Task Continuity Verification:**
1. Read the last git commit description, or recent commits related to the plan
2. Determine the completion status of the previous task
3. If no related commits found (possibly due to context loss) → Review code to confirm completion status

**B. Design Document Alignment:**
1. Review project design documents (design docs in `docs/plans/` directory)
2. Determine how the current plan should be developed and designed
3. Ensure implementation direction aligns with design documents

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
3. **Follow supergos:code standards:**
   - When using frameworks/libraries → First call mcp:context-7 to get latest docs
   - When developing UI → Call ui/ux pro max to review design
   - When writing code → Call code-simplifier to ensure code quality
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

### Step 5: Design Compliance Verification

After all tasks complete and verified:

**A. Design Consistency Check:**
1. Review design documents again (`docs/plans/` directory)
2. Compare actual implementation with design requirements
3. Check for deviations or omissions
4. Present comparison results between implementation and design to user

**B. User Confirmation:**
1. Ask user: "Does the implementation meet design expectations?"
2. Decide whether adjustments are needed based on user feedback
3. If user confirms it meets expectations → Proceed to Step 6

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
- **Pre-execution check** - First verify previous task completion and design documents
- **Follow standards** - Always follow supergos:code standards during development
- Review plan critically first
- Follow plan steps exactly
- Don't skip verifications
- Reference skills when plan says to
- Between batches: just report and wait
- Stop when blocked, don't guess
- **Post-execution verification** - Review design docs after completion and ask for user confirmation
