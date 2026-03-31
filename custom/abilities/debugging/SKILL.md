---
name: debugging
description: Helps debug code issues by providing systematic debugging strategies and techniques
---

# Debugging

## When to Use

Use this skill when the user:
- Encounters a bug or error
- Needs help troubleshooting
- Wants to understand why code isn't working
- Needs to fix a failing test
- Has performance issues

## Instructions

1. **Understand the Problem**
   - Ask for the error message or behavior
   - Get the code causing the issue
   - Understand the expected vs actual behavior
   - Learn the context (when did it start?)

2. **Reproduce the Issue**
   - Try to reproduce the bug
   - Identify the exact steps
   - Note any patterns or conditions
   - Determine if it's intermittent

3. **Formulate Hypotheses**
   - Based on symptoms, propose possible causes
   - Prioritize most likely causes
   - Consider recent changes
   - Think about edge cases

4. **Test Hypotheses**
   - Add logging/print statements
   - Use debugger
   - Isolate the problematic code
   - Test with different inputs

5. **Implement Fix**
   - Fix the root cause
   - Test the fix
   - Ensure no regressions
   - Add tests to prevent recurrence

## Debugging Techniques

### Print Debugging
```javascript
console.log('Variable value:', variable);
console.log('Line number', new Error().stack.split('\n')[1]);
```

### Using Debugger
```javascript
// Set breakpoints in IDE
// Or use debugger statement
debugger;
```

### Binary Search
```javascript
// Comment out half the code
// If bug disappears, bug is in commented part
// Otherwise, bug is in active part
// Repeat until found
```

### Rubber Duck Debugging
- Explain the code line by line to someone (or rubber duck)
- Often the solution becomes clear during explanation

## Common Bug Types

### Syntax Errors
- Missing brackets, semicolons, quotes
- Typos in variable names
- Incorrect syntax for language

### Runtime Errors
- Null pointer dereference
- Undefined variable
- Type mismatch
- Out of bounds

### Logic Errors
- Incorrect condition
- Wrong loop bounds
- Off-by-one errors
- Incorrect operator

### Performance Issues
- Inefficient algorithms
- Memory leaks
- N+1 queries
- Unnecessary computations

## Debugging Checklist

- [ ] Can I reproduce the issue?
- [ ] What's the exact error message?
- [ ] When did this start happening?
- [ ] What changed recently?
- [ ] Is this isolated to a specific environment?
- [ ] Are there similar working examples?

## Tools

### Browser DevTools
- Console: For JavaScript errors
- Network: For API calls
- Debugger: For breakpoints
- Performance: For profiling

### Node.js
- `console.log()`: Print debugging
- `debugger`: Breakpoint
- `node inspect`: Node debugger

### VS Code
- Built-in debugger
- Integrated console
- Breakpoint controls

## Best Practices

1. **Start Simple**
   - Use print statements first
   - Gradually move to debugger
   - Don't overcomplicate

2. **Be Systematic**
   - Test one hypothesis at a time
   - Keep notes of what you've tried
   - Document your findings

3. **Learn from Bugs**
   - Understand why the bug occurred
   - Prevent similar bugs
   - Add tests for the fix

4. **Ask for Help**
   - Don't spend too long stuck
   - Provide context when asking
   - Share what you've tried

## Example Debugging Session

**Problem:** Function returns undefined

```javascript
function calculateTotal(items) {
  let total = 0;
  items.forEach(item => {
    total += item.price;
  });
  // Missing return statement!
}
```

**Debugging Steps:**
1. Add console.log before return
2. Notice function doesn't return
3. Add `return total;`
4. Test again - works!

## Notes

- Debugging is a skill that improves with practice
- Don't panic when you see an error
- Take breaks if stuck
- Document your debugging process
- Learn from every bug you fix
