---
name: code
description: "Global development standards - All projects MUST follow. Defines standardized workflows for technical documentation, UI/UX design, and code quality."
---

# Global Development Standards

## Overview

This specification defines standardized workflows that MUST be followed during development to ensure code quality, design aesthetics, and correct technology choices.

**All agents MUST follow these standards throughout the development process.**

## Technical Documentation Standards (mcp:context-7)

### When to Use

| Scenario | Trigger |
|----------|--------|
| Framework usage | Before using any framework |
| Third-party library | Before using any third-party library |
| Version upgrade | During version upgrades or migrations |
| API uncertainty | When unsure about API usage |

### What to Do

1. Get the latest version information for frameworks/libraries
2. Retrieve official API documentation
3. Get best practices and example code
4. Get changelog/migration guides (if applicable)

### How to Do It

```
Call mcp:context-7 to query documentation
- Specify framework/library name and version requirements
- Get complete API documentation before starting to code
- Record version numbers in project documentation
```

**⚠️ MANDATORY: Do NOT use any framework or third-party library without first retrieving its latest documentation**

## UI/UX Design Standards (ui/ux pro max)

### When to Use

| Scenario | Trigger |
|----------|--------|
| Interface design | When designing new interfaces |
| UI component development | When developing UI components |
| Interface modification | When modifying existing interfaces |
| UI code review | When reviewing UI-related code |

### What to Do

1. Ensure design meets aesthetic standards
2. Verify smooth user experience
3. Check component consistency
4. Review interaction design rationality

### How to Do It

```
Call ui/ux pro max skill
- Design phase: Get design suggestions and guidelines
- Development phase: Review implementation against design specs
- Modification phase: Ensure changes don't break overall aesthetics and consistency
```

## Code Quality Standards (code-simplifier)

### When to Use

| Scenario | Trigger |
|----------|--------|
| Architecture design | When designing code architecture |
| New code writing | When writing new code |
| Code refactoring | When refactoring existing code |
| Code review | When conducting code reviews |

### What to Do

Eliminate the following code issues:

| Problem | Solution |
|---------|----------|
| Maze-like nested logic | Flatten logic, early returns |
| Inconsistent naming styles | Unify naming conventions |
| Duplicate code/"temporary patches" | Abstract for reuse, eliminate patches |
| Code works but afraid to modify | Clear structure, safe to change |
| Colleagues afraid to take over | High readability, easy handover |

### How to Do It

```
Call code-simplifier plugin
- Architecture design: Plan clear, maintainable architecture
- Code writing: Generate concise, highly readable code
- Code refactoring: Simplify logic, unify style
- Code review: Check and fix quality issues
```

## Standards Execution Checklist

During development, regularly check the following:

**Technology Selection:**
- [ ] Retrieved framework documentation via context-7?
- [ ] Retrieved third-party library documentation via context-7?
- [ ] Recorded version numbers used?

**UI/UX:**
- [ ] Reviewed design via ui/ux pro max?
- [ ] Does interface meet aesthetic standards?
- [ ] Is user experience smooth?

**Code Quality:**
- [ ] Optimized code via code-simplifier?
- [ ] Is logic clear and understandable?
- [ ] Is naming consistent and standardized?
- [ ] Eliminated duplicate code?

## Remember

- **Documentation before coding** - MUST retrieve latest docs before using frameworks/libraries
- **No compromise on aesthetics** - UI/UX design MUST undergo professional review
- **Quality is the baseline** - Code MUST be clear, maintainable, and easy to hand over
- **Standards throughout** - Follow these standards from design to development
