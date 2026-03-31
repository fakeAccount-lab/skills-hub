---
name: documentation
description: Helps generate, maintain, and improve code documentation and API docs
---

# Documentation

## When to Use

Use this skill when the user needs to:
- Generate documentation from code
- Write API documentation
- Create README files
- Document complex algorithms
- Improve existing documentation
- Add code comments

## Instructions

1. **Understand what needs documentation**
   - Identify the code or API to document
   - Determine the target audience
   - Choose appropriate documentation format

2. **Generate API documentation**
   - List all endpoints
   - Document parameters
   - Document responses
   - Include examples
   - Add authentication info

3. **Write code documentation**
   - Document functions and classes
   - Explain complex logic
   - Add parameter descriptions
   - Document return values
   - Include usage examples

4. **Create README files**
   - Explain the project purpose
   - Provide installation instructions
   - Include usage examples
   - Document configuration
   - Add contribution guidelines

5. **Maintain documentation**
   - Keep docs in sync with code
   - Update examples
   - Fix broken links
   - Clarify unclear sections

## API Documentation Template

```markdown
# API Name

## Overview
Brief description of what the API does.

## Base URL
\`\`\`
https://api.example.com/v1
\`\`\`

## Authentication
Explain authentication method.

## Endpoints

### GET /endpoint-name

**Description:** What this endpoint does.

**Parameters:**
| Name | Type | Required | Description |
|------|------|----------|-------------|
| param1 | string | Yes | Parameter description |

**Response:**
\`\`\`json
{
  "field1": "value1",
  "field2": 123
}
\`\`\`

**Example:**
\`\`\`bash
curl -X GET "https://api.example.com/v1/endpoint-name?param1=value"
\`\`\`
```

## Code Documentation Template

```javascript
/**
 * Brief description of what this function does.
 *
 * @param {Type} paramName - Description of parameter
 * @returns {Type} Description of return value
 * @throws {Error} Description of when this error is thrown
 *
 * @example
 * // Example usage
 * const result = functionName(arg1, arg2);
 */
function functionName(paramName) {
  // Implementation
}
```

## README Template

```markdown
# Project Name

## Description
Brief description of the project.

## Installation
\`\`\`bash
npm install project-name
\`\`\`

## Usage
\`\`\`javascript
const project = require('project-name');
project.method();
\`\`\`

## Configuration
Explain configuration options.

## API Reference
Link to API docs.

## Contributing
Guidelines for contributors.

## License
License information.
```

## Best Practices

1. **Keep it Simple**
   - Use clear language
   - Avoid jargon
   - Be concise

2. **Be Accurate**
   - Ensure docs match code
   - Test all examples
   - Update regularly

3. **Be Comprehensive**
   - Cover all use cases
   - Document edge cases
   - Include error handling

4. **Be Consistent**
   - Use consistent formatting
   - Follow style guide
   - Use same terminology

## Common Documentation Tools

- **JSDoc**: JavaScript documentation
- **Swagger/OpenAPI**: API documentation
- **Markdown**: General documentation
- **Doxygen**: C/C++ documentation
- **Sphinx**: Python documentation

## Notes

- Documentation is part of the code
- Write documentation as you code
- Review documentation in code reviews
- Keep examples runnable
- Update docs when code changes
