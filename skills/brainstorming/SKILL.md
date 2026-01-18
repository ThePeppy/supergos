---
name: brainstorming
description: "You MUST use this before any creative work - creating features, building components, adding functionality, or modifying behavior. Explores user intent, requirements and design before implementation."
---

# Brainstorming Ideas Into Designs

## Overview

Help turn ideas into fully formed designs and specs through natural collaborative dialogue.

Start by understanding the current project context, then ask questions one at a time to refine the idea. Once you understand what you're building, present the design in small sections (200-300 words), checking after each section whether it looks right so far.

**⚠️ Design phase MUST follow supergos:code global development standards**

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
- **When involving technology selection:** Call mcp:context-7 to get latest documentation and version info for frameworks/libraries

**Presenting the design:**
- Once you believe you understand what you're building, present the design
- Break it into sections of 200-300 words
- Ask after each section whether it looks right so far
- Cover: architecture, components, data flow, error handling, testing
- Be ready to go back and clarify if something doesn't make sense
- **When involving UI design:** Call ui/ux pro max to ensure design aesthetics and user experience
- **When involving code architecture:** Call code-simplifier to ensure clear, maintainable architecture

## After the Design

**Documentation:**
- Write the validated design to `docs/plans/YYYY-MM-DD-<topic>-design.md`
- Use elements-of-style:writing-clearly-and-concisely skill if available
- Commit the design document to git

**Implementation (if continuing):**
- Ask: "Ready to set up for implementation?"
- Use supergos:using-git-worktrees to create isolated workspace
- Use supergos:writing-plans to create detailed implementation plan

## Key Principles

- **One question at a time** - Don't overwhelm with multiple questions
- **Multiple choice preferred** - Easier to answer than open-ended when possible
- **YAGNI ruthlessly** - Remove unnecessary features from all designs
- **Explore alternatives** - Always propose 2-3 approaches before settling
- **Incremental validation** - Present design in sections, validate each
- **Be flexible** - Go back and clarify when something doesn't make sense

## Development Standards Compliance (supergos:code)

During design phase, MUST follow these standards:

**Technology Selection (mcp:context-7):**
- Before using any framework → Call context-7 to get latest documentation
- Before using any third-party library → Call context-7 to get latest version and API docs
- Do NOT finalize technology choices without retrieving latest documentation

**UI Design (ui/ux pro max):**
- When designing new interfaces → Call ui/ux pro max for design suggestions
- Ensure design meets aesthetic standards and UX requirements

**Code Architecture Design (code-simplifier):**
- When designing code architecture → Call code-simplifier to plan clear, maintainable architecture
- Ensure architecture design avoids: complex nested logic, inconsistent naming, code duplication
