---
name: api-testing
description: Helps with API testing, including creating test cases, mocking, and validating responses
---

# API Testing

## When to Use

Use this skill when the user needs to:
- Create API test cases
- Mock API responses
- Validate API responses
- Test error handling
- Set up integration tests
- Debug API issues

## Instructions

1. **Understand the API**
   - Get the API documentation
   - Understand endpoints, methods, and parameters
   - Learn the request/response format
   - Identify authentication requirements

2. **Design test cases**
   - Cover happy path scenarios
   - Test error scenarios
   - Test edge cases
   - Include boundary conditions
   - Test authentication/authorization

3. **Set up testing environment**
   - Configure test database
   - Mock external services
   - Set up test data
   - Configure test runner

4. **Write tests**
   - Use appropriate testing framework (Jest, pytest, etc.)
   - Write clear, descriptive test names
   - Use assertions properly
   - Clean up after tests

5. **Run and analyze**
   - Execute tests
   - Review test results
   - Debug failures
   - Fix issues

## Test Case Templates

### Happy Path
```javascript
test('should successfully create a user', async () => {
  const response = await api.post('/users', {
    name: 'John Doe',
    email: 'john@example.com'
  });
  
  expect(response.status).toBe(201);
  expect(response.data.name).toBe('John Doe');
});
```

### Error Path
```javascript
test('should return 400 for invalid email', async () => {
  const response = await api.post('/users', {
    name: 'John Doe',
    email: 'invalid-email'
  });
  
  expect(response.status).toBe(400);
  expect(response.data.error).toContain('email');
});
```

### Edge Case
```javascript
test('should handle empty request body', async () => {
  const response = await api.post('/users', {});
  
  expect(response.status).toBe(400);
});
```

## Best Practices

1. **Test Isolation**
   - Each test should be independent
   - Clean up test data
   - Use test fixtures

2. **Mock External Services**
   - Don't hit real APIs in tests
   - Use consistent mock responses
   - Mock success and failure scenarios

3. **Assert Properly**
   - Test both status code and body
   - Use specific assertions
   - Avoid overly broad assertions

4. **Performance**
   - Run tests in parallel when possible
   - Use test databases
   - Cache expensive operations

## Common Testing Patterns

### Authentication Testing
```javascript
beforeEach(async () => {
  const token = await loginAsAdmin();
  api.defaults.headers.common['Authorization'] = `Bearer ${token}`;
});
```

### Data Setup
```javascript
beforeEach(async () => {
  await setupTestData();
});

afterEach(async () => {
  await cleanupTestData();
});
```

### Response Validation
```javascript
test('should return correct schema', async () => {
  const response = await api.get('/users/1');
  
  expect(response.data).toMatchObject({
    id: expect.any(Number),
    name: expect.any(String),
    email: expect.stringMatching(/^.+@.+\..+$/)
  });
});
```

## Notes

- Tests should be fast
- Tests should be reliable
- Tests should be maintainable
- Test names should be descriptive
- Keep test logic simple
