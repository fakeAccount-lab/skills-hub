---
name: code-review
description: Helps perform code reviews by checking for common issues, bugs, and best practices violations
---

# Code Review

## When to Use

Use this skill when the user wants to:
- Review a pull request
- Check code for bugs or issues
- Ensure code follows best practices
- Suggest improvements
- Identify security vulnerabilities

## Instructions

1. **Understand the context**
   - Ask for the code to review
   - Understand the programming language and framework
   - Learn the purpose of the changes

2. **Review for correctness**
   - Check for bugs and logic errors
   - Verify error handling
   - Validate input handling
   - Check for edge cases

3. **Review for best practices**
   - Check code readability
   - Look for code duplication
   - Verify proper naming conventions
   - Check for proper documentation

4. **Review for performance**
   - Identify potential performance bottlenecks
   - Check for unnecessary computations
   - Suggest optimizations

5. **Review for security**
   - Check for SQL injection risks
   - Verify proper authentication/authorization
   - Check for sensitive data exposure
   - Validate input sanitization

6. **Provide constructive feedback**
   - Be specific and actionable
   - Explain why changes are needed
   - Suggest concrete improvements
   - Be respectful and professional

## Common Issues to Look For

### Bugs
- Off-by-one errors
- Null pointer dereferences
- Race conditions
- Resource leaks

### Best Practices
- Magic numbers
- Deep nesting
- Long functions
- Poor variable names

### Security
- Hardcoded credentials
- Missing input validation
- SQL injection
- XSS vulnerabilities

## Output Format

Provide feedback in this structure:

```
🔴 Critical Issues:
- [Issue description]

⚠️  Suggestions:
- [Suggestion]

💡 Improvements:
- [Improvement]

✅ Good Practices:
- [What's done well]
```

## Notes

- Be constructive, not critical
- Focus on the code, not the person
- Prioritize critical issues over style
- Suggest, don't demand
