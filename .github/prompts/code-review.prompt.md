---
description: 'Prompt for performing thorough code review with actionable feedback'
name: Code Review Prompt
---

# Code Review

Perform a comprehensive code review on the provided code.

## Input

**Language**: {{language}}
**Context**: {{context}}
**Code**: 
```{{language}}
{{code}}
```

## Review Categories

### 1. Security Analysis

Check for:
- [ ] SQL injection vulnerabilities
- [ ] XSS vulnerabilities
- [ ] Hardcoded secrets/credentials
- [ ] Insecure data handling
- [ ] Authentication/authorization issues
- [ ] Input validation gaps
- [ ] Sensitive data exposure

### 2. Performance Review

Check for:
- [ ] N+1 query problems
- [ ] Unnecessary iterations
- [ ] Memory leaks or inefficiencies
- [ ] Missing caching opportunities
- [ ] Blocking operations
- [ ] Large object allocations

### 3. Code Quality

Check for:
- [ ] Clear naming conventions
- [ ] Single Responsibility Principle
- [ ] DRY (Don't Repeat Yourself)
- [ ] Appropriate error handling
- [ ] Code complexity (cyclomatic)
- [ ] Magic numbers/strings
- [ ] Dead code

### 4. Testing

Check for:
- [ ] Testability of code
- [ ] Missing test cases
- [ ] Edge cases coverage
- [ ] Error scenario tests

### 5. Documentation

Check for:
- [ ] Public API documentation
- [ ] Complex logic comments
- [ ] README updates needed
- [ ] Changelog entries

## Output Format

```markdown
## Code Review Summary

**Overall Assessment**: ✅ Approve | ⚠️ Request Changes | ❌ Reject

### Critical Issues (Must Fix)
1. 🔴 [Issue description]
   - Location: [file:line]
   - Problem: [explanation]
   - Solution: [recommendation with code]

### Suggestions (Should Fix)
1. 🟡 [Issue description]
   - Location: [file:line]
   - Recommendation: [explanation]

### Minor/Nitpicks (Optional)
1. 🟢 [Suggestion]

### Positive Feedback
- [What was done well]

### Questions
1. ❓ [Clarification needed]
```

## Review Guidelines

- Be constructive, not critical
- Explain the "why" behind suggestions
- Provide code examples for fixes
- Acknowledge good practices
- Focus on significant issues first
